## Cross origin resource sharing(CORS) in Web Api

### 1.use CORS middleware
``` C#
        public void ConfigureServices(IServiceCollection services)
        {
            ...
            services.AddCors(options =>
            {
                options.AddPolicy("HeroPolicy", policy =>
                {
                    policy.WithOrigins("http://localhost:4200");
                });
            });
        } 
        public void Configure(IApplicationBuilder app, IWebHostEnvironment env)
        {
            ...
            app.UseCors("HeroPolicy");
            ...
        }
    }

```

### 2.use default policy

``` c#
        public void ConfigureServices(IServiceCollection services)
        {
            ...
            services.AddCors(options =>
            {
                options.AddDefaultPolicy(
                    builder =>
                    {
                        builder.WithOrigins("http://localhost:4200");
                    });
            });
        }
        public void Configure(IApplicationBuilder app, IWebHostEnvironment env)
        {
            ...
            app.UseCors();
            ...
        }
    }

```

### 3.use EnableCors Attribute
``` c#
        public void ConfigureServices(IServiceCollection services)
        {
            ...
            services.AddCors(options =>
            {
                options.AddPolicy("HeroPolicy", policy =>
                {
                    policy.WithOrigins("http://localhost:4200");
                });
            });
        } 

        public void Configure(IApplicationBuilder app, IWebHostEnvironment env)
        {
            ...
            app.UseCors();
            ...
        }

    [EnableCors("HeroPolicy")]
    public class WeatherForecastController : ControllerBase
    {
        ...
    }
```

[Check out this link for more details about CORS in asp.net core!](https://docs.microsoft.com/en-us/aspnet/core/security/cors?view=aspnetcore-5.0)