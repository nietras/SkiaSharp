# API diff: SkiaSharp.Views.Maui.Controls.dll

## SkiaSharp.Views.Maui.Controls.dll

### Namespace SkiaSharp.Views.Maui.Controls

#### Type Changed: SkiaSharp.Views.Maui.Controls.AppHostBuilderExtensions

Removed method:

```csharp
public static Microsoft.Maui.Hosting.IAppHostBuilder UseSkiaSharpHandlers (this Microsoft.Maui.Hosting.IAppHostBuilder builder);
```

Added method:

```csharp

[Obsolete ("Use SkiaSharp.Views.Maui.Controls.Hosting.UseSkiaSharp() instead.")]
public static Microsoft.Maui.MauiAppBuilder UseSkiaSharpHandlers (this Microsoft.Maui.MauiAppBuilder builder);
```



### New Namespace SkiaSharp.Views.Maui.Controls.Hosting

#### New Type: SkiaSharp.Views.Maui.Controls.Hosting.AppHostBuilderExtensions

```csharp
public static class AppHostBuilderExtensions {
	// methods
	public static Microsoft.Maui.MauiAppBuilder UseSkiaSharp (this Microsoft.Maui.MauiAppBuilder builder);
}
```

