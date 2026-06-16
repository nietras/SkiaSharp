# API diff: SkiaSharp.Views.Maui.Controls.dll

## SkiaSharp.Views.Maui.Controls.dll

### Namespace SkiaSharp.Views.Maui.Controls

#### Type Changed: SkiaSharp.Views.Maui.Controls.AppHostBuilderExtensions

Removed method:

```csharp
[Obsolete ("Use SkiaSharp.Views.Maui.Controls.Hosting.UseSkiaSharp() instead.")]
public static Microsoft.Maui.MauiAppBuilder UseSkiaSharpHandlers (this Microsoft.Maui.MauiAppBuilder builder);
```

Added method:

```csharp

[Obsolete ("Use SkiaSharp.Views.Maui.Controls.Hosting.UseSkiaSharp() instead.")]
public static Microsoft.Maui.Hosting.MauiAppBuilder UseSkiaSharpHandlers (this Microsoft.Maui.Hosting.MauiAppBuilder builder);
```



### Namespace SkiaSharp.Views.Maui.Controls.Hosting

#### Type Changed: SkiaSharp.Views.Maui.Controls.Hosting.AppHostBuilderExtensions

Removed method:

```csharp
public static Microsoft.Maui.MauiAppBuilder UseSkiaSharp (this Microsoft.Maui.MauiAppBuilder builder);
```

Added method:

```csharp
public static Microsoft.Maui.Hosting.MauiAppBuilder UseSkiaSharp (this Microsoft.Maui.Hosting.MauiAppBuilder builder);
```



