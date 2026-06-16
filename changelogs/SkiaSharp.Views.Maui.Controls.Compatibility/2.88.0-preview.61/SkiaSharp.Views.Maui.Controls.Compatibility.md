# API diff: SkiaSharp.Views.Maui.Controls.Compatibility.dll

## SkiaSharp.Views.Maui.Controls.Compatibility.dll

> Assembly Version Changed: 2.88.0.0 vs 0.0.0.0

### New Namespace SkiaSharp.Views.Maui.Controls.Compatibility

#### New Type: SkiaSharp.Views.Maui.Controls.Compatibility.AppHostBuilderExtensions

```csharp
public static class AppHostBuilderExtensions {
	// methods
	public static Microsoft.Maui.Hosting.IAppHostBuilder UseSkiaSharpCompatibilityRenderers (this Microsoft.Maui.Hosting.IAppHostBuilder builder);
}
```

#### New Type: SkiaSharp.Views.Maui.Controls.Compatibility.SKCanvasViewRenderer

```csharp
public class SKCanvasViewRenderer : SkiaSharp.Views.Maui.Controls.Compatibility.SKCanvasViewRendererBase`2[SkiaSharp.Views.Maui.Controls.SKCanvasView,SkiaSharp.Views.iOS.SKCanvasView] {
	// constructors
	public SKCanvasViewRenderer ();
	// methods
	protected override SkiaSharp.Views.iOS.SKCanvasView CreateNativeControl ();
}
```

#### New Type: SkiaSharp.Views.Maui.Controls.Compatibility.SKCanvasViewRendererBase`2

```csharp
public abstract class SKCanvasViewRendererBase`2 : Microsoft.Maui.Controls.Compatibility.Platform.iOS.ViewRenderer`2[TFormsView,TNativeView] {
	// constructors
	protected SKCanvasViewRendererBase`2 ();
	// methods
	protected override TNativeView CreateNativeControl ();
	protected override void Dispose (bool disposing);
	protected override void OnElementChanged (Microsoft.Maui.Controls.Platform.ElementChangedEventArgs<TFormsView> e);
	protected override void OnElementPropertyChanged (object sender, System.ComponentModel.PropertyChangedEventArgs e);
	protected void SetDisablesUserInteraction (bool disablesUserInteraction);
}
```

#### New Type: SkiaSharp.Views.Maui.Controls.Compatibility.SKGLViewRenderer

```csharp
public class SKGLViewRenderer : SkiaSharp.Views.Maui.Controls.Compatibility.SKGLViewRendererBase`2[SkiaSharp.Views.Maui.Controls.SKGLView,SkiaSharp.Views.iOS.SKGLView] {
	// constructors
	public SKGLViewRenderer ();
	// methods
	protected override SkiaSharp.Views.iOS.SKGLView CreateNativeControl ();
	protected override void Dispose (bool disposing);
	protected override void SetupRenderLoop (bool oneShot);
}
```

#### New Type: SkiaSharp.Views.Maui.Controls.Compatibility.SKGLViewRendererBase`2

```csharp
public abstract class SKGLViewRendererBase`2 : Microsoft.Maui.Controls.Compatibility.Platform.iOS.ViewRenderer`2[TFormsView,TNativeView] {
	// constructors
	protected SKGLViewRendererBase`2 ();
	// properties
	public SkiaSharp.GRContext GRContext { get; }
	// methods
	protected override TNativeView CreateNativeControl ();
	protected override void Dispose (bool disposing);
	protected override void OnElementChanged (Microsoft.Maui.Controls.Platform.ElementChangedEventArgs<TFormsView> e);
	protected override void OnElementPropertyChanged (object sender, System.ComponentModel.PropertyChangedEventArgs e);
	protected void SetDisablesUserInteraction (bool disablesUserInteraction);
	protected virtual void SetupRenderLoop (bool oneShot);
}
```

#### New Type: SkiaSharp.Views.Maui.Controls.Compatibility.SKImageSourceHandler

```csharp
public sealed class SKImageSourceHandler : Microsoft.Maui.Controls.Compatibility.Platform.iOS.IImageSourceHandler, Microsoft.Maui.Controls.IRegisterable {
	// constructors
	public SKImageSourceHandler ();
	// methods
	public virtual System.Threading.Tasks.Task<UIKit.UIImage> LoadImageAsync (Microsoft.Maui.Controls.ImageSource imagesource, System.Threading.CancellationToken cancelationToken, float scale);
}
```

