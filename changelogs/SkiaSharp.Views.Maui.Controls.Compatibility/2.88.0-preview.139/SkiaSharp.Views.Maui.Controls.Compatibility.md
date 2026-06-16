# API diff: SkiaSharp.Views.Maui.Controls.Compatibility.dll

## SkiaSharp.Views.Maui.Controls.Compatibility.dll

### Namespace SkiaSharp.Views.Maui.Controls.Compatibility

#### Type Changed: SkiaSharp.Views.Maui.Controls.Compatibility.AppHostBuilderExtensions

Removed method:

```csharp
public static Microsoft.Maui.Hosting.IAppHostBuilder UseSkiaSharpCompatibilityRenderers (this Microsoft.Maui.Hosting.IAppHostBuilder builder);
```

Added method:

```csharp

[Obsolete ("Use SkiaSharp.Views.Maui.Controls.Hosting.UseSkiaSharp(bool, bool) instead.")]
public static Microsoft.Maui.MauiAppBuilder UseSkiaSharpCompatibilityRenderers (this Microsoft.Maui.MauiAppBuilder builder);
```



### New Namespace SkiaSharp.Views.Maui.Controls.Hosting

#### New Type: SkiaSharp.Views.Maui.Controls.Hosting.AppHostBuilderExtensions

```csharp
public static class AppHostBuilderExtensions {
	// methods
	public static Microsoft.Maui.MauiAppBuilder UseSkiaSharp (this Microsoft.Maui.MauiAppBuilder builder, bool registerRenderers, bool replaceHandlers);
}
```

