---
layout: post
title:  ComputerScienceLearn
description: 计算机科学相关学习内容总结
date: 2022-10-01 09:01:01
---



## LinuxAndOpenSource

### OpenSource主流开源协议

#### GPL

> 最开放，只要引用GPL协议的软件必须开源免费，不适合商业软件 有5大自由 使用，复制，修改，衍生，收费。

#### LGPL

> 较GPL 宽松

#### BSD  

> 发布带源代码 则源代码必须遵循BSD

> 发布只有二进制则必须声明遵循了BSD协议

#### Apache 

> 软件以及衍生品必须继续使用Apache许可。

> 修改了源代码则必须声明

> 基于他人源代码则必须保留原始代码的许可商标声明等。

> 类库保护，只正对引用的类库，而无须适用整个软件系统。

> 发布软件中有声明软件则需在此文件中注明基于Apache 和其他协议。

#### MIT(MITL)

> 修改后的源代码需要保留作者的许可信息即可。

#### Mozilla(MPL)

> 后续只开源使用的特定代码

> 多种协议可以混合使用

> 发布软件附带专门说明文件有原始的代码的修改时间和方式。

### Git in linux 

#### Download and Install GithubCli

> https://github.com/cli/cli/releases

#### Login 

> $ gh auth login (config use ssh,need your token from github config)

#### Git helper 

> $ git clone git@github.com:devgis/MyWriting.git  //need your private key
> 提交修改 上传修改的代码后执行增加修改： 
> $ git add . 
> 增加修改信息： 
> $ git commit -m ‘修改lol清晰增加口径’ 
> 推送分支： 
> $ git push origin main



## Asp.net core MVC 一些总结

### Router

#### property router

> [Route("app/[controller]/actions/[action]/{id:weekday?}")]

#### 设置路由中间件
```
app.UseMvc(routes =>
            {
                routes.MapRoute(
                    name: "default",
                    template: "{controller=Home}/{action=Index}/{id?}");
            });
```

> 常规路由：routes.MapRoute(name: "default",template: "{controller=Home}/{action=Index}/{id?}");  这是一个常规路由

#### 多路由 

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


#### 高级路由

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


### Session

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


### 授权认证管理

#### 认证
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

### DI

> services.AddSingleton<IRepository, MemoryRepository>(); 单实例

> services.AddTransient<IModelStorage, DictionaryStorage>(); 每一次获取的对象都不是同一个

> services.AddScoped 请求开始-请求结束 在这次请求中获取的对象都是同一个；不用申明静态类；

### Filters

#### 子类Controller拦截器要先于父类Controller拦截器执行

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


#### 授权过滤器 AuthorizeAttribute

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

#### 资源过滤器 IResourceFilter

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

#### 异常过滤器 IExceptionFilter

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

#### 操作过滤器 ActionFilterAttribute

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

#### 结果过滤器 ResultFilterAttribute

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

#### 结果过滤器 IFilterDiagnostics

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

#### IAsyncResultFilter

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


### Controllers

> [HttpGet("object/{format?}")]
>        [FormatFilter]

#### WebAPI
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

#### Controller

##### 所有的动作结果都继承自ActionResult基类 ASP.NET MVC框架支持六种标准类型的动作结果：

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

#### Rezor View
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


### ViewComponent

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


### Taghelper 可以扩展一些自定义的标记 其实就是后台生成html代码的一种形式

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


## Bootstrap学习总结

### Bootstrap 基础

#### 媒体查询（css3特性）

> @media not|only 媒体类型 and (媒体特性) {css 代码样式}

> css3中的媒体类型和媒体特性与bootsrap不太一样。

> 可以实现依据最小最大宽度（媒体类型）等设置不同css样式。

##### 媒体类型

> all	用于所有多媒体类型设备
> print	用于打印机
> screen	用于电脑屏幕，平板，智能手机等。
> speech	用于屏幕阅读器

##### 媒体特性

> aspect-ratio	定义输出设备中的页面可见区域宽度与高度的比率
> color	定义输出设备每一组彩色原件的个数。如果不是彩色设备，则值等于0
> color-index	定义在输出设备的彩色查询表中的条目数。如果没有使用彩色查询表，则值等于0
> device-aspect-ratio	定义输出设备的屏幕可见宽度与高度的比率。
> device-height	定义输出设备的屏幕可见高度。
> device-width	定义输出设备的屏幕可见宽度。
> grid	用来查询输出设备是否使用栅格或点阵。
> height	定义输出设备中的页面可见区域高度。
> max-aspect-ratio	定义输出设备的屏幕可见宽度与高度的最大比率。
> max-color	定义输出设备每一组彩色原件的最大个数。
> max-color-index	定义在输出设备的彩色查询表中的最大条目数。
> max-device-aspect-ratio	定义输出设备的屏幕可见宽度与高度的最大比率。
> max-device-height	定义输出设备的屏幕可见的最大高度。
> max-device-width	定义输出设备的屏幕最大可见宽度。
> max-height	定义输出设备中的页面最大可见区域高度。
> max-monochrome	定义在一个单色框架缓冲区中每像素包含的最大单色原件个数。
> max-resolution	定义设备的最大分辨率。
> max-width	定义输出设备中的页面最大可见区域宽度。
> min-aspect-ratio	定义输出设备中的页面可见区域宽度与高度的最小比率。
> min-color	定义输出设备每一组彩色原件的最小个数。
> min-color-index	定义在输出设备的彩色查询表中的最小条目数。
> min-device-aspect-ratio	定义输出设备的屏幕可见宽度与高度的最小比率。
> min-device-width	定义输出设备的屏幕最小可见宽度。
> min-device-height	定义输出设备的屏幕的最小可见高度。
> min-height	定义输出设备中的页面最小可见区域高度。
> min-monochrome	定义在一个单色框架缓冲区中每像素包含的最小单色原件个数
> min-resolution	定义设备的最小分辨率。
> min-width	定义输出设备中的页面最小可见区域宽度。
> monochrome	定义在一个单色框架缓冲区中每像素包含的单色原件个数。如果不是单色设备，则值等于0
> orientation	定义输出设备中的页面可见区域高度是否大于或等于宽度。
> resolution	定义设备的分辨率。如：96dpi, 300dpi, 118dpcm
> scan	定义电视类设备的扫描工序。
> width	定义输出设备中的页面可见区域宽度。


### Bootstrap 布局

#### 包装容器

> .container .container -{breakpoint} .container-fluid

#### 响应断点

> 当你须要搞定响应式布局时，一堆堆的媒体查询、大量的属性、属性值往往能够把你搞颠，SASS（或者诸如此类的预处理器）被觉得是处理响应式断点的最佳利器。

> 1.使用变量(With variables)
Bootstrap和Foundation採用这样的方式，首先定义变量，然后在媒体查询中使用变量。换句话说，你能够在配置文件或者其它地方定义变量以备使用。我们来看看Bootstrap怎么干的。
// Defining values
$screen-sm-min: 768px;
$screen-xs-max: ($screen-sm-min - 1);
$screen-md-min: 992px;
$screen-sm-max: ($screen-md-min - 1);
$screen-lg-min: 1200px;
$screen-md-max: ($screen-lg-min - 1);
 
// Usage
@media (max-width: $screen-xs-max) { ... }
@media (min-width: $screen-sm-min) { ... }
@media (max-width: $screen-sm-max) { ... }
@media (min-width: $screen-md-min) { ... }
@media (max-width: $screen-md-max) { ... }
@media (min-width: $screen-lg-min) { ... }
Foudation更进一步，使用跨范围的媒体查询，避免使用过多的max-width和min-width。
// Defining values
$small-range:   (0em, 40em);       /* 0, 640px */
$medium-range:  (40.063em, 64em);  /* 641px, 1024px */
$large-range:   (64.063em, 90em);  /* 1025px, 1440px */
$xlarge-range:  (90.063em, 120em); /* 1441px, 1920px */
$xxlarge-range: (120.063em);       /* 1921px */
 
// Defining media queries
$screen:       "only screen" !default;
$landscape:    "#{$screen} and (orientation: landscape)" !default;
$portrait:     "#{$screen} and (orientation: portrait)" !default;
$small-up:     $screen !default;
$small-only:   "#{$screen} and (max-width: #{upper-bound($small-range)})" !default;
$medium-up:    "#{$screen} and (min-width:#{lower-bound($medium-range)})" !default;
$medium-only:  "#{$screen} and (min-width:#{lower-bound($medium-range)}) and (max-width:#{upper-bound($medium-range)})" !default;
$large-up:     "#{$screen} and (min-width:#{lower-bound($large-range)})" !default;
$large-only:   "#{$screen} and (min-width:#{lower-bound($large-range)}) and (max-width:#{upper-bound($large-range)})" !default;
$xlarge-up:    "#{$screen} and (min-width:#{lower-bound($xlarge-range)})" !default;
$xlarge-only:  "#{$screen} and (min-width:#{lower-bound($xlarge-range)}) and (max-width:#{upper-bound($xlarge-range)})" !default;
$xxlarge-up:   "#{$screen} and (min-width:#{lower-bound($xxlarge-range)})" !default;
$xxlarge-only: "#{$screen} and (min-width:#{lower-bound($xxlarge-range)}) and (max-width:#{upper-bound($xxlarge-range)})" !default;
 
// Usage
@media #{$small-up}     { ... }
@media #{$small-only}   { ... }
@media #{$medium-up}    { ... }
@media #{$medium-only}  { ... }
@media #{$large-up}     { ... }
@media #{$large-only}   { ... }
@media #{$xlarge-up}    { ... }
@media #{$xlarge-only}  { ... }
@media #{$xxlarge-up}   { ... }
@media #{$xxlarge-only} { ... }
两种方法各有一个不爽的地方，在Bootstrap里每次都要使用max-width，在Foundation里我们须要使用插值变量这样的又丑又烦的方式。显示我们须要想办法解决这些问题。

> 2.使用独立Mixin(With a standalone mixin)《media queries in Sass 3.2》是CSS-Tricks里最火的文章之中的一个，在这篇文章里Chris Coyier在借鉴a former idea by Mason Wendell和a former idea by Jeff Croft两文的基础上，怎样使用sass实现响应式布局的断点管理。

命名断点是非常重要的，由于能够为抽象的数字赋予意义（你知道767px是什么意思吗，我不知道，直到我去使用小屏幕的时候才知道）。为什么Bootstrap和Foundation要使用变量呢，不也是为了给抽象的数字起个名字吗？
所以我们定义个mixin，接收断点名作唯一的參数，返回媒体查询的内容。准备好了吗？走起。
@mixin respond-to($breakpoint) {
  @if $breakpoint == "small" {
    @media (min-width: 767px) {
      @content;
    }
  }
 
  @else if $breakpoint == "medium" {
    @media (min-width: 992px) {
      @content;
    }
  }
 
  @else if $breakpoint == "large" {
    @media (min-width: 1200px) {
      @content;
    }
  }
}
然后，我们这样使用mixin。
@include respond-to(small) { ... }
@include respond-to(medium) { ... }
@include respond-to(large) { ... }
这种方法是极好的（甄嬛体，老外也看？），原因有二：抽象数据有意义，大量断点集中管理。假设你想把“992px”改成“970px”，你不须要爬过每个css文件，而仅仅需更新mixin，然后所有更新。
可是也还有两个问题：
a.断点不easy从mixin里拿出来，放到配置文件中去。
b.冗余太多。

> 3. 可配置的mixin(With a configurable mixin  )

<为了解决上面的两个问题，我们须要从断点mixin中抽出一个列表，仅仅剩下mixin核心，然后这个列表就能够随便移动，或者扔到配置文件中。
然后，使用sass 3.3+中的maps，我们能够方便的使用关联的属性和属性值。
$breakpoints: (
  'small'  : 767px,
  'medium' : 992px,
  'large'  : 1200px
);
然后原来的mixin进行相应的改动
@mixin respond-to($breakpoint) {
  // Retrieves the value from the key
  $value: map-get($breakpoints, $breakpoint);
 
  // If the key exists in the map
  @if $value != null {
    // Prints a media query based on the value
    @media (min-width: $value) {
      @content;
    }
  }
 
  // If the key doesn't exist in the map
  @else {
    @warn "Unfortunately, no value could be retrieved from `#{$breakpoint}`. "
        + "Please make sure it is defined in `$breakpoints` map.";
  }
}
我们在改动mixin的同一时候也进行了一些提高，不要小看这些提高，我们加上了错误处理，假设在maps中没有找到断点值，将会弹出一个错误提示，这将便于我们开发过程中的调试。
我们让mixin变得更加精简，能非常好的处理错误，同一时候我们去掉了一个功能——推断属性是否是你想要的（min-width,max-width,min-height等），这在移动优先的网页中没问题，由于我们仅仅须要min-width。可是，假设须要查询其它属性，我们须要把这个功能加回来。为了达到这个目的，我想到了一个非常优雅的解决方式，同一时候并不添加复杂性。
$breakpoints: (
  'small'  : ( min-width:  767px ),
  'medium' : ( min-width:  992px ),
  'large'  : ( min-width: 1200px )
);
  
@mixin respond-to($name) {
  // If the key exists in the map
  @if map-has-key($breakpoints, $name) {
    // Prints a media query based on the value
    @media #{inspect(map-get($breakpoints, $name))} {
      @content;
    }
  }
 
  // If the key doesn't exist in the map
  @else {
    @warn "Unfortunately, no value could be retrieved from `#{$breakpoint}`. "
        + "Please make sure it is defined in `$breakpoints` map.";
  }
}
在这里，我们主要做了三个事情
a. 检查查询的断点在map中存在不存在
b.假设存在，打印相应的媒体查询。
c.假设不在，进行错误提示。
简单吧，假设我们回想前面的两个缺陷，已经不再有WET(Write Everything Twice))问题，也不再有不灵活的媒体查询。可是另一个问题，不支持复杂的媒体查询。复杂指的是涉及多个组件的查询（e.g. screen and (min-width: 767px)）。我们上面这些方案除了第一种变量之外都不能非常好的解决问题。

> 4. 使用外部工具(With an external tool)

```
最后一个相同重要的是，假设不想创建自己的mixin，你能够使用外部的工具处理响应式布局的断点，有非常多sass的扩展在这个方面做得非常好。
SassMQ by Kaelig
Breakpoint by Mason Wendell and Sam Richard
Breakup by Ben Scott
 	SassMQ	Breakpoint	Breakup
MQ type	*-width	any	any
No Query fallback	yep	yep	yep
API complexity	simple	very simple	medium
Code complexity	very simple	complexe	simple
Extra	Debug mode	Singularity.gs	—
基本上是这样，假设发现有没有涉及的，记得一定告诉我。
SassMQ
// Configuration
$mq-responsive: true;
$mq-static-breakpoint: desktop;
$mq-breakpoints: (
  mobile:  320px,
  tablet:  740px,
  desktop: 980px,
  wide:    1300px
);
 
// Example
selector {
  @include mq($from: mobile) {
    property: value;
  }
}
BreakPoints
$high-tide: 500px;
$ex-presidents: 600px 800px;
$surfboard-width: max-width 1000px;
$surfboard-height: (min-height 1000px) (orientation portrait);
 
selector {
  @include breakpoint($high-tide) {
    property: value;
  }
}
Breakup
$breakup-breakpoints: (
  'thin' '(max-width: 35.999em)',
  'wide' '(min-width: 36em)',
  'full' '(min-width: 61em)'
);
 
selector {
  @include breakup-block('thin') {
    property: value;
  }
}
```

#### 堆叠顺序 z-index


#### 网格系统

> 12列的网格 col-2 列占用2/12的宽度 



### Bootstrap 版式

#### 文档案

#### 图片

#### 表格

#### 代码


### Bootstrap 通用样式

#### 文本

#### 颜色

#### 边框

#### 定位浮动

#### 代码弹性盒子

#### 其它 对齐等


### Bootstrap 组件

#### 按钮

#### 按钮组

#### 下拉

#### 媒体对象

#### 表单

#### 进度条

#### 导航栏

#### 列表组

#### 面包屑 

> 显示导航层次位置 如 “首页-> 文学-> 中国文学”

#### 分页

#### 加载指示器（转圈圈）

#### 按钮卡片

###  Sass

#### 变量

#### 嵌套归斥责

#### 导入

#### SASS 混合器 混合器继承

> 混合器 Sass中的混合器类似于js的函数，将一段代码定义成混合器以实现代码的重用  编译后其实会转换成正常的css

> 声明混合器：@mixin mixName 

> 调用混合器  @include minName 如

@mixin border-round{
    -moz-border:1px solid red;
    -webkit-border:1px solid red;
    border:1px solid red
}
#top{
    @include border-round;
}

//编译后
#top {
  -moz-border: 1px solid red;
  -webkit-border: 1px solid red;
  border: 1px solid red; }

> 混合器css规则 混合器中也可以包含css规则

@mixin testmix{
    list-style:none;
    li{
        color:red;
        padding:30px;
    }
    >.top{
        background:red
    }
}

ul.parent{
    border:1px solid red;
    @include testmix;
}
//编译后
ul.parent {
  border: 1px solid red;
  list-style: none; 
}
  ul.parent li {
    color: red;
    padding: 30px; 
}
  ul.parent > .top {
    background: red;
 }

> 混合器传参 混合器可以像函数一样传递参数 混合器传参数

@mixin test($color,$size,$hoverColor){
    color:$color;
    border:$size solid red;
    &:hover{
        color:$hoverColor
    }
}

#top{
    @include test(red,1px,blue);
}
//编译后
#top {
  color: red;
  border: 1px solid red; 
}
  #top:hover {
    color: blue; 
}

/*# 

当然这里有个问题，混合器里面的参数不允许颠倒位置，如果你记不清他们什么位置可以使用键值的方式明确指定

@mixin test($color,$size,$hoverColor){
    color:$color;
    border:$size solid red;
    &:hover{
        color:$hoverColor
    }
}

#top{
    @include test($size:1px,$hoverColor:blue,$color:red);
}
//编译后
#top {
  color: red;
  border: 1px solid red;
  }
#top:hover {
    color: blue;
  }

> 参数默认值 混合器允许你定义参数默认值 如下

@mixin test($normal,$hover:red){
    color:$normal;
    background-color:$hover
}
#top{
    @include test(skyblue,orange);
}
//编译后
#top {
  color: skyblue;
  background-color: orange;
  }
  //不指定color
@mixin test($normal,$hover:red){
    color:$normal;
    background-color:$hover
}
#top{
    @include test(skyblue);
}
//编译后
  
#top {
  color: skyblue;
  background-color: red; }

> Sass继承 Sass中也可实现继承类似面向对象思想子类继承父类，sass可以继承多个父类 这个”父类“可以是类，id 标签 状态等。 继承语法 @extend name 如

.error{
    color:red;
    font-size:15px;
}
.danger-error{
    @extend .error;
    font-size:20px;
}
//编译后
.error, .danger-error {
  color: red;
  font-size: 15px;
}

.danger-error {
  font-size: 20px; 
}

当然父类也可包含css规则

.error{
    color:red;
    font-size:15px;
    >.te{
        padding:10px
    }
}
.danger-error{
    @extend .error;
    font-size:20px;
}
//编译后
.error, .danger-error {
  color: red;
  font-size: 15px; 
}
.error > .te, .danger-error > .te {
    padding: 10px;
  }

.danger-error {
  font-size: 20px; 
 }

> 组合继承

.error a{
    color:red;
    font-size:10px;
}
.danger{
    @extend .error;
    color:orange;
}
//编译后
.error a, .danger a {
  color: red;
  font-size: 10px; 
}

.danger {
  color: orange; 
}


> 继承多个

.one{
    color:red;
}
.two{

    border:1px solid red;
}
.three{
    @extend .one;
    @extend .two;
    //或者这样写@extend .one,.two
    //
    background:blue;
}
//编译后
.one, .three {
  color: red; 
}
.two, .three {
  border: 1px solid red;
}
.three {
  background: blue;
}


> 继承局限性 继承不支持组合 很多选择器不支持继承如包选择器 .one tow 相邻选择器 .one+.two

%继承 有些时候我们希望被用来继承的代码不要渲染到页面上只作为继承使用。 定义方法 父类名前+%

%test{
    border:1px solid red;
}
#main{
    @extend %test;
}
//编译后
#main {
  border: 1px solid red; 
}


#meng a%long{
    color:blue;
    border:1px solid red;
}

.notice{
    @extend %long;
}
//编译后
#meng a.notice {
  color: blue;
  border: 1px solid red; 
}

继承在指令的作用域如（@media） 在指令内部无法继承到指令外部的类，指令外部继承指令内部的类无法达到预期效果

.one{
    height:400px;
}

@media print{
    .two{
        @extend .one
    }
    width:300px;
}

> 编译时报错 继承注意事项

> 不能过量使用继承，因为所有类继承了父类，父类改变就会影响子类
 
继承只会在生成css时复制选择器，而不会复制大段的css属性  如果不小心会让生成css中包含大量的选择器复制  避免这种情况的最好办法：  不要在继承css规则中使用后代选择器如
 
 .dsf{}
 .foo .bar {
 @extend dsf //不推荐
 }

### JQuery 