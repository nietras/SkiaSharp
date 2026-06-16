# API diff: SkiaSharp.Views.Maui.Controls.Compatibility.dll

## SkiaSharp.Views.Maui.Controls.Compatibility.dll

### Namespace SkiaSharp.Views.Maui.Controls.Compatibility

#### Type Changed: SkiaSharp.Views.Maui.Controls.Compatibility.AppHostBuilderExtensions

Removed method:

```csharp
[Obsolete ("Use SkiaSharp.Views.Maui.Controls.Hosting.UseSkiaSharp(bool, bool) instead.")]
public static Microsoft.Maui.MauiAppBuilder UseSkiaSharpCompatibilityRenderers (this Microsoft.Maui.MauiAppBuilder builder);
```

Added method:

```csharp

[Obsolete ("Use SkiaSharp.Views.Maui.Controls.Hosting.UseSkiaSharp(bool, bool) instead.")]
public static Microsoft.Maui.Hosting.MauiAppBuilder UseSkiaSharpCompatibilityRenderers (this Microsoft.Maui.Hosting.MauiAppBuilder builder);
```



### Namespace SkiaSharp.Views.Maui.Controls.Hosting

#### Type Changed: SkiaSharp.Views.Maui.Controls.Hosting.AppHostBuilderExtensions

Removed method:

```csharp
public static Microsoft.Maui.MauiAppBuilder UseSkiaSharp (this Microsoft.Maui.MauiAppBuilder builder, bool registerRenderers, bool replaceHandlers);
```

Added method:

```csharp
public static Microsoft.Maui.Hosting.MauiAppBuilder UseSkiaSharp (this Microsoft.Maui.Hosting.MauiAppBuilder builder, bool registerRenderers, bool replaceHandlers);
```



