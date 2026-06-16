# API diff: SkiaSharp.Views.Android.dll

## SkiaSharp.Views.Android.dll

### Namespace SkiaSharp.Views.Android

#### Type Changed: SkiaSharp.Views.Android.Resource

#### Type Changed: SkiaSharp.Views.Android.Resource.Attribute

Added field:

```csharp
public static int ignorePixelScaling;
```


#### New Type: SkiaSharp.Views.Android.Resource.Styleable

```csharp
public class Styleable {
	// fields
	public static int[] SKCanvasView;
	public static int SKCanvasView_ignorePixelScaling;
}
```


#### Type Changed: SkiaSharp.Views.Android.SKPaintSurfaceEventArgs

Added constructor:

```csharp
public SKPaintSurfaceEventArgs (SkiaSharp.SKSurface surface, SkiaSharp.SKImageInfo info, SkiaSharp.SKImageInfo rawInfo);
```

Added property:

```csharp
public SkiaSharp.SKImageInfo RawInfo { get; }
```



