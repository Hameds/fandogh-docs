---
layout: fandogh
id: static
title: Static WebSite
sidebar_label: وب سایت‌های ایستا 
---
دیپلوی کردن سرویس‌ها بر روی فندق برای کاربرانی که با docker کار نکرده‌اند ممکن است مقداری مبهم باشد٬ همینطور معمولا آماده سازی پروژه‌ها برای اجرا در محیط واقعی نیاز به تنظیماتی دارد که باعث پیچیده شدن کار برنامه‌نویس می‌شوند. 


> اگر هنوز CLI  فندق بر روی کامپیوتر شما نصب نیست از طریق این [مستند](https://docs.fandogh.cloud/docs/getting-started.html) می‌توانید CLI را بر روی کامپیوتر خود نصب کنید.


در پوشه اصلی پروژه٬ بعد از اینکه در فندق لاگین کردید دستور fandogh source init را اجرا کنید. در اولین مرحله شما می‌بایست اسم سرویس رو انتخاب نمایید.

```
Service Name: mystaticweb

```

 بعد از وارد کردن نام Service  برای شما گزینه هایی که بدون نیاز به دانش docker قابل اجرا هستند نمایش داده می شود. از بین گزینه های نمایش داده گزینه Static Website را انتخاب کنید.


```
-[1] Static Website
-[2] Django Project
Please choose one of the project types above:

```
> توجه داشته باشید شماره گزینه مورد نظر را وارد کنید.


در قسمت بعدی شما باید context را وارد کنید. context همان پوشه‌ای است که خروجی برنامه شما در آن قراره گرفته است. اگر در حال حاضر در پوشه اصلی نیستید می توانید آدرس آن را وارد کنید یا در غیر این صورت خالی بگذارید و دکمه enter را فشار دهید. 
```
The context directory [.]:
```

 بعد از اینکه گزینه مورد نظر را انتخاب کردید فایلی با نام fandogh.yml حاوی اطلاعات مورد نیاز برای دیپلوی سرویس شما به پوشه‌ای که در آن قرار دارید اضافه خواهد شد. 
 
حالا  شما با دستور ```fandogh source run‍‍‍``` میتونید سرویس خودتون رو روی  فندق دیپلوی کنید. بعد از اجرای این دستور مراحل بیلد و دیپلوی آغاز خواهد شد و در کمتر از یک دقیقه وب سایت شما بر روی فندق قابل دسترس خواهد بود. 

> پس از هر بار تغییر در پروژه تنها کافیست که دستور fandogh source run را مجددا اجرا کنید. 
> فایل ```fandogh.yml``` می‌تواند شامل تمام بخش‌هایی که در [مانیفست](https://docs.fandogh.cloud/docs/service-manifest.html) فندق است باشد٬ شما به صورت دستی قادر هستید بخش‌های مورد نیاز این فایل را تغییر دهید.