﻿# .NET Standard / .NET Core Support

Starting on version [2.1.0](changelog.md#v2-1-0), [PKI SDK](index.md) now supports **[.NET Standard](https://docs.microsoft.com/pt-br/dotnet/standard/net-standard) 2.0**,
besides .NET Frameworks 4.5 and 4.0 Client Profile. This means that PKI SDK can be used on applications written in [.NET Core](https://docs.microsoft.com/pt-br/dotnet/core/index).

> [!TIP]
> Applications written in .NET Core have the big advantage of being **compatible with Linux servers**, increasing the
> platforms supported by your application.

To demonstrate the possibilities that this opens up, our development team performed successfully a digital signature on
our laboratory on a Raspberry Pi 3 on a .NET Core console application using PKI SDK.

Besides .NET Core, you can also use PKI SDK on mobile apps written in [Xamarin](https://visualstudio.microsoft.com/xamarin/).
