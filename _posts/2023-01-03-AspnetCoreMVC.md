---
layout: post
title: AspnetCoreMVCLearn
description: Asp.net core MVC 一些总结
date: 2023-01-02 15:43:01
---

## Router

### property router

> [Route("app/[controller]/actions/[action]/{id:weekday?}")]

### 设置路由中间件
```
app.UseMvc(routes =>
            {
                routes.MapRoute(
                    name: "default",
                    template: "{controller=Home}/{action=Index}/{id?}");
            });
```

> 常规路由：routes.MapRoute(name: "default",template: "{controller=Home}/{action=Index}/{id?}");  这是一个常规路由

### 多路由 

```
app.UseMvc(routes =>
            {
                routes.MapRoute("blog", "blog/{*article}",
                    defaults: new { Controller = "Blog", Action = "Index" });
                routes.MapRoute(
                    name: "default",
                    template: "{controller=Home}/{action=Index}/{id?}");
            });
```


### 高级路由

```
app.UseMvc(routes => {
                routes.MapRoute(
                    name: "areas",
                    template: "{area:exists}/{controller=Home}/{action=Index}");

                routes.Routes.Add(new LegacyRoute(
                    routes.DefaultHandler,
                    "/articles/Windows_3.1_Overview.html",
                    "/old/.NET_1.0_Class_Library"));

                routes.MapRoute(
                    name: "default",
                    template: "{controller=Home}/{action=Index}/{id?}");

                routes.MapRoute(
                    name: "out",
                    template: "outbound/{controller=Home}/{action=Index}");
            });
```


## Session

```
using System;
using Microsoft.AspNetCore.Http;
using Microsoft.Extensions.DependencyInjection;
using Newtonsoft.Json;
using SportsStore.Infrastructure;

namespace SportsStore.Models
{

    public class SessionCart : Cart
    {

        public static Cart GetCart(IServiceProvider services)
        {
            ISession session = services.GetRequiredService<IHttpContextAccessor>()?
                .HttpContext.Session;
            SessionCart cart = session?.GetJson<SessionCart>("Cart")
                ?? new SessionCart();
            cart.Session = session;
            return cart;
        }

        [JsonIgnore]
        public ISession Session { get; set; }

        public override void AddItem(Product product, int quantity)
        {
            base.AddItem(product, quantity);
            Session.SetJson("Cart", this);
        }

        public override void RemoveLine(Product product)
        {
            base.RemoveLine(product);
            Session.SetJson("Cart", this);
        }

        public override void Clear()
        {
            base.Clear();
            Session.Remove("Cart");
        }
    }
}

```


## 授权认证管理

### 认证
```
using System.Threading.Tasks;
using Microsoft.AspNetCore.Authorization;
using Microsoft.AspNetCore.Identity;
using Microsoft.AspNetCore.Mvc;
using SportsStore.Models.ViewModels;
using SportsStore.Models;

[Authorize]
public class AccountController : Controller {
    private UserManager<IdentityUser> userManager;
    private SignInManager<IdentityUser> signInManager;

    public AccountController(UserManager<IdentityUser> userMgr,
            SignInManager<IdentityUser> signInMgr) {
        userManager = userMgr;
        signInManager = signInMgr;
        IdentitySeedData.EnsurePopulated(userMgr).Wait();
    }

    [AllowAnonymous]
    public ViewResult Login(string returnUrl) {
        return View(new LoginModel {
            ReturnUrl = returnUrl
        });
    }

    [HttpPost]
    [AllowAnonymous]
    [ValidateAntiForgeryToken]
    public async Task<IActionResult> Login(LoginModel loginModel) {
        if (ModelState.IsValid) {
            IdentityUser user =
                await userManager.FindByNameAsync(loginModel.Name);
            if (user != null) {
                await signInManager.SignOutAsync();
                if ((await signInManager.PasswordSignInAsync(user,
                        loginModel.Password, false, false)).Succeeded) {
                    return Redirect(loginModel?.ReturnUrl ?? "/Admin/Index");
                }
            }
        }
        ModelState.AddModelError("", "Invalid name or password");
        return View(loginModel);
    }

    public async Task<RedirectResult> Logout(string returnUrl = "/") {
        await signInManager.SignOutAsync();
        return Redirect(returnUrl);
    }
}
```

> rezor

```
@model LoginModel
@{
    ViewBag.Title = "Log In";
    Layout = "_AdminLayout";
}

<div class="text-danger" asp-validation-summary="All"></div>

<form asp-action="Login" asp-controller="Account" method="post">
    <input type="hidden" asp-for="ReturnUrl" />
    <div class="form-group">
        <label asp-for="Name"></label>
        <div><span asp-validation-for="Name" class="text-danger"></span></div>
        <input asp-for="Name" class="form-control" />
    </div>
    <div class="form-group">
        <label asp-for="Password"></label>
        <div><span asp-validation-for="Password" class="text-danger"></span></div>
        <input asp-for="Password" class="form-control" />
    </div>
    <button class="btn btn-primary" type="submit">Log In</button>
</form>

```

## DI

> services.AddSingleton<IRepository, MemoryRepository>();

> services.AddTransient<IModelStorage, DictionaryStorage>();

> services.AddScoped

## Filters

### 子类Controller拦截器要先于父类Controller拦截器执行

> 最先执行的是全局声明的MyActionOneAttribute拦截器

> 然后执行的是声明在子Controller类HomeController上的MyActionThreeAttribute拦截器

> 接着执行的是声明在父Controller类BaseController上的MyActionTwoAttribute拦截器

> 最后执行的是声明在子Controller类HomeController的Index方法上的MyActionFourAttribute拦截器

```
public class MyFilterAttribute : ResultFilterAttribute {
    private string message;

    public MyFilterAttribute(string msg) {
        message = msg;
    }

    public override void OnResultExecuting(ResultExecutingContext context) {
        WriteMessage(context, $"<div>Before Result:{message}</div>");
    }

    public override void OnResultExecuted(ResultExecutedContext context) {
        WriteMessage(context, $"<div>After Result:{message}</div>");
    }

    private void WriteMessage(FilterContext context, string msg) {
        byte[] bytes = Encoding.ASCII
            .GetBytes($"<div>{msg}</div>");

        // Synchronous operations are disallowed. Call WriteAsync or set AllowSynchronousIO to true instead.
        context.HttpContext.Response
            .Body.WriteAsync(bytes, 0, bytes.Length);
    }
}
```

> Usage:

```
    [MyFilter("This is the Controller-Scoped Filter", Order = 10)]
    public class HomeController : Controller {

        [MyFilter("This is the First Action-Scoped Filter", Order = 1)]
        [MyFilter("This is the Second Action-Scoped Filter", Order = -1)]
        public ViewResult Index() => View("Message",
            "This is the Index action on the Home controller");
    }
```


### 授权过滤器 AuthorizeAttribute

```
 public class HttpsOnlyAttribute : Attribute, IAuthorizationFilter {

        public void OnAuthorization(AuthorizationFilterContext context) {
            if (!context.HttpContext.Request.IsHttps) {
                context.Result =
                    new StatusCodeResult(StatusCodes.Status403Forbidden);
            }
        }
    }
```

### 资源过滤器 IResourceFilter

```
public class CustomerResourceFilterAttribute : Attribute, IResourceFilter
    {
        private static Dictionary<string,object> cacheDic=new Dictionary<string, object>();
        public void OnResourceExecuting(ResourceExecutingContext context)
        {
            var path=context.HttpContext.Request.Path; 
            if (cacheDic.ContainsKey(path))
            {
                context.Result = (IActionResult)cacheDic[path];
            }
            Console.WriteLine("CustomerResourceFilterAttribute.OnResourceExecuting");
        }
        public void OnResourceExecuted(ResourceExecutedContext context)
        {
            var path = context.HttpContext.Request.Path;
            cacheDic[path] = context.Result;
            Console.WriteLine("CustomerResourceFilterAttribute.OnResourceExecuted");
        }
 
         
    }
```

### 异常过滤器 IExceptionFilter

```
public class RangeExceptionAttribute : ExceptionFilterAttribute {

        public override void OnException(ExceptionContext context) {
            if (context.Exception is ArgumentOutOfRangeException) {
                context.Result = new ViewResult() {
                    ViewName = "Message",
                    ViewData = new ViewDataDictionary(
                        new EmptyModelMetadataProvider(),
                        new ModelStateDictionary()) {
                        Model = @"The data received by the
                                application cannot be processed"
                    }
                };
            }
        }
    }
```

### 操作过滤器 ActionFilterAttribute

```
public class ProfileAttribute : ActionFilterAttribute {
        private Stopwatch timer;
        private double actionTime;

        public override async Task OnActionExecutionAsync(
                ActionExecutingContext context,
                ActionExecutionDelegate next) {

            timer = Stopwatch.StartNew();

            await next();

            actionTime = timer.Elapsed.TotalMilliseconds;
        }

        public override async Task OnResultExecutionAsync(
                ResultExecutingContext context,
                ResultExecutionDelegate next) {

            await next();

            timer.Stop();
            string result = "<div>Action time: "
                + $"{actionTime} ms</div><div>Total time: "
                + $"{timer.Elapsed.TotalMilliseconds} ms</div>";
            byte[] bytes = Encoding.ASCII.GetBytes(result);

            await context.HttpContext.Response.Body.WriteAsync(bytes,
                0, bytes.Length);
        }
    }
```

```
public class ViewResultDiagnostics : IActionFilter {
        private IFilterDiagnostics diagnostics;

        public ViewResultDiagnostics(IFilterDiagnostics diags) {
            diagnostics = diags;
        }

        public void OnActionExecuting(ActionExecutingContext context) {
            // do nothing - not used in this filter
        }

        public void OnActionExecuted(ActionExecutedContext context) {
            ViewResult vr;
            if ((vr = context.Result as ViewResult) != null) {
                diagnostics.AddMessage($"View name: {vr.ViewName}");
                diagnostics.AddMessage($@"Model type: 
                    {vr.ViewData.Model.GetType().Name}");
            }
        }
    }
```

### 结果过滤器 ResultFilterAttribute

```
     public class MessageAttribute : ResultFilterAttribute {
        private string message;

        public MessageAttribute(string msg) {
            message = msg;
        }

        public override void OnResultExecuting(ResultExecutingContext context) {
            WriteMessage(context, $"<div>Before Result:{message}</div>");
        }

        public override void OnResultExecuted(ResultExecutedContext context) {
            WriteMessage(context, $"<div>After Result:{message}</div>");
        }

        private void WriteMessage(FilterContext context, string msg) {
            byte[] bytes = Encoding.ASCII
                .GetBytes($"<div>{msg}</div>");

            // Synchronous operations are disallowed. Call WriteAsync or set AllowSynchronousIO to true instead.
            context.HttpContext.Response
                .Body.WriteAsync(bytes, 0, bytes.Length);
        }
    }
```

```
 public class ViewResultDetailsAttribute : ResultFilterAttribute {

        public override async Task OnResultExecutionAsync(
                ResultExecutingContext context,
                ResultExecutionDelegate next) {

            Dictionary<string, string> dict = new Dictionary<string, string> {
                ["Result Type"] = context.Result.GetType().Name,
            };

            ViewResult vr;
            if ((vr = context.Result as ViewResult) != null) {
                dict["View Name"] = vr.ViewName;
                dict["Model Type"] = vr.ViewData.Model.GetType().Name;
                dict["Model Data"] = vr.ViewData.Model.ToString();
            }

            context.Result = new ViewResult {
                ViewName = "Message",
                ViewData = new ViewDataDictionary(
                        new EmptyModelMetadataProvider(),
                        new ModelStateDictionary()) {
                    Model = dict
                }
            };

            await next();
        }
    }
```

### 结果过滤器 IFilterDiagnostics

```
     public interface IFilterDiagnostics {
        IEnumerable<string> Messages { get; }
        void AddMessage(string message);
    }

    public class DefaultFilterDiagnostics : IFilterDiagnostics {
        private List<string> messages = new List<string>();

        public IEnumerable<string> Messages => messages;

        public void AddMessage(string message) =>
            messages.Add(message);
    }
```

### IAsyncResultFilter

```
    public class DiagnosticsFilter : IAsyncResultFilter {
        private IFilterDiagnostics diagnostics;

        public DiagnosticsFilter(IFilterDiagnostics diags) {
            diagnostics = diags;
        }

        public async Task OnResultExecutionAsync(
                ResultExecutingContext context,
                ResultExecutionDelegate next) {

            await next();

            foreach (string message in diagnostics?.Messages) {
                byte[] bytes = Encoding.ASCII
                    .GetBytes($"<div>{message}</div>");
                await context.HttpContext.Response.Body
                    .WriteAsync(bytes, 0, bytes.Length);
            }
        }
    }
```


```
 public class TimeFilter : IAsyncActionFilter, IAsyncResultFilter {
        private ConcurrentQueue<double> actionTimes = new ConcurrentQueue<double>();
        private ConcurrentQueue<double> resultTimes = new ConcurrentQueue<double>();
        private IFilterDiagnostics diagnostics;

        public TimeFilter(IFilterDiagnostics diags) {
            diagnostics = diags;
        }

        public async Task OnActionExecutionAsync(
                ActionExecutingContext context, ActionExecutionDelegate next) {

            Stopwatch timer = Stopwatch.StartNew();
            await next();
            timer.Stop();
            actionTimes.Enqueue(timer.Elapsed.TotalMilliseconds);
            diagnostics.AddMessage($@"Action time: 
                {timer.Elapsed.TotalMilliseconds} 
                Average: {actionTimes.Average():F2}");
        }

        public async Task OnResultExecutionAsync(
                ResultExecutingContext context, ResultExecutionDelegate next) {

            Stopwatch timer = Stopwatch.StartNew();
            await next();
            timer.Stop();
            resultTimes.Enqueue(timer.Elapsed.TotalMilliseconds);
            diagnostics.AddMessage($@"Result time: 
                {timer.Elapsed.TotalMilliseconds}
                Average: {resultTimes.Average():F2}");
        }
    }
```


## Controllers

> [HttpGet("object/{format?}")]
>        [FormatFilter]

### WebAPI
```
    [Route("api/[controller]")]
    public class ContentController : Controller {

        [HttpGet("string")]
        public string GetString() => "This is a string response";

        [HttpGet("object/{format?}")]
        [FormatFilter]
        //[Produces("application/json", "application/xml")]
        public Reservation GetObject() => new Reservation {
            ReservationId = 100,
            ClientName = "Joe",
            Location = "Board Room"
        };

        [HttpPost]
        [Consumes("application/json")]
        public Reservation ReceiveJson([FromBody] Reservation reservation) {
            reservation.ClientName = "Json";
            return reservation;
        }

        [HttpPost]
        [Consumes("application/xml")]
        public Reservation ReceiveXml([FromBody] Reservation reservation) {
            reservation.ClientName = "Xml";
            return reservation;
        }
    }
```

### Controller

#### 所有的动作结果都继承自ActionResult基类 ASP.NET MVC框架支持六种标准类型的动作结果：

> 动作名称 概述 方法名

> ViewResult 视图内容，HTML或标记 View

> EmptyResult 空内容

> RedirectResult 重定向到新的URL

> Redirect RedirectToRouteResult 重定向到新的控制器

> RedirectToAction/RedirectToRoute JsonResult 返回一个JSON（Javascript Object Notation）内容 Json ContentResult 返回文本内容 Content

```
[Route("api/[controller]")]
    public class ReservationController : Controller {
        private IRepository repository;

        public ReservationController(IRepository repo) => repository = repo;

        [HttpGet]
        public IEnumerable<Reservation> Get() => repository.Reservations;

        [HttpGet("{id}")]
        public Reservation Get(int id) => repository[id];

        [HttpPost]
        public Reservation Post([FromBody] Reservation res) =>
            repository.AddReservation(new Reservation {
                ClientName = res.ClientName,
                Location = res.Location
            });

        [HttpPut]
        public Reservation Put([FromBody] Reservation res) =>
            repository.UpdateReservation(res);

        [HttpPatch("{id}")]
        public StatusCodeResult Patch(int id,
                [FromBody]JsonPatchDocument<Reservation> patch) {
            Reservation res = Get(id);
            if (res != null) {
                patch.ApplyTo(res);
                return Ok();
            }
            return NotFound();
        }

        [HttpDelete("{id}")]
        public void Delete(int id) => repository.DeleteReservation(id);
    }
```

### Rezor View
```
@model IEnumerable<Reservation>
@{  Layout = "_Layout"; }

<form id="addform" asp-action="AddReservation" method="post">
    <div class="form-group">
        <label for="ClientName">Name:</label>
        <input class="form-control" name="ClientName" />
    </div>
    <div class="form-group">
        <label for="Location">Location:</label>
        <input class="form-control" name="Location" />
    </div>
    <div class="text-center panel-body">
        <button type="submit" class="btn btn-sm btn-primary">Add</button>
    </div>
</form>

<table class="table table-sm table-striped table-bordered m-2">
    <thead><tr><th>ID</th><th>Client</th><th>Location</th></tr></thead>
    <tbody>
        @foreach (var r in Model) {
            <tr>
                <td>@r.ReservationId</td>
                <td>@r.ClientName</td>
                <td>@r.Location</td>
            </tr>
        }
    </tbody>
</table>

```

```
services.AddMvc()
    .AddXmlDataContractSerializerFormatters()
    .AddMvcOptions(opts => {
        opts.EnableEndpointRouting = false;
        opts.FormatterMappings.SetMediaTypeMappingForFormat("xml",
            new MediaTypeHeaderValue("application/xml"));
        opts.RespectBrowserAcceptHeader = true;
        opts.ReturnHttpNotAcceptable = true;
    });
```


## ViewComponent

```
 public class PageSize : ViewComponent {

        public async Task<IViewComponentResult> InvokeAsync() {
            HttpClient client = new HttpClient();
            HttpResponseMessage response
                = await client.GetAsync("http://apress.com");
            return View(response.Content.Headers.ContentLength);
        }
    }
```


## Taghelper 可以扩展一些自定义的标记 其实就是后台生成html代码的一种形式

> 扩展标记，可以从后台进行前端Html的配置

> HtmlTargetElement 属性中配置那些html元素，那些样式起作用

> 定义一个Taghelper  formbutton 设置其属性
```
    [HtmlTargetElement("button", Attributes = "bs-button-color", ParentTag = "div")]
    [HtmlTargetElement("a", Attributes = "bs-button-color", ParentTag = "div")]
    [HtmlTargetElement("formbutton")]
    public class LYFButtonTagHelper : TagHelper {

        public string BsButtonColor { get; set; } = "primary";

        public override void Process(TagHelperContext context,
                                     TagHelperOutput output) {

            output.Attributes.SetAttribute("class", $"btn btn-{BsButtonColor}");
        }
    }
```

> View中用法

```
<formbutton>hello</formbutton>
```

> 本质上所有的mvc视图元素都是来自Taghelper 比如form

```
<form method="post" asp-controller="Home" asp-action="Create"
      asp-antiforgery="true">
    <div class="form-group">
        <label asp-for="Name"></label>
        <input class="form-control" asp-for="Name" />
    </div>
    <div class="form-group">
        <label asp-for="Country"></label>
        <select class="form-control" asp-for="Country" asp-items="ViewBag.Countries">
            <option disabled selected value="">Select a Country</option>
        </select>
    </div>
    <div class="form-group">
        <label asp-for="Population"></label>
        <input class="form-control" asp-for="Population" />
    </div>
    <div class="form-group">
        <label asp-for="Notes"></label>
        <textarea class="form-control" asp-for="Notes"></textarea>
    </div>
    <button type="submit" class="btn btn-primary">Add</button>
    <a class="btn btn-primary" href="/Home/Index">Cancel</a>
</form>

```