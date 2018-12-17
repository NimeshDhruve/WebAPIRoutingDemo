# WebAPIRoutingDemo
Generate Web API url using Url.RouteUrl

After upgrading to Asp.Net 2.2, Url.RouteURL seems to be broken.

This repo has code to demonstrate the issue. 

In file [Startup.cs](https://github.com/nimeshdhruve/WebAPIRoutingDemo/blob/master/WebApiDemo/Startup.cs) if you uncomment [line ](https://github.com/nimeshdhruve/WebAPIRoutingDemo/blob/master/WebApiDemo/Startup.cs#L30) `setupAction.EnableEndpointRouting = false` the URL will get correctly generated other wise URL won't generated. 

The code for generating URL uses Url.RouteUrl:
```
Example: 
Url.RouteUrl("ControllerOnlyRouteName", new { controller= "MyApi"})
```
