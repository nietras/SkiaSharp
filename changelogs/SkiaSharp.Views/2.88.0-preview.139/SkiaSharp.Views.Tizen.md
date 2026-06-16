# API diff: SkiaSharp.Views.Tizen.dll

## SkiaSharp.Views.Tizen.dll

### Namespace SkiaSharp.Views.Tizen

#### Type Changed: SkiaSharp.Views.Tizen.CustomRenderingView

Added method:

```csharp
protected virtual SkiaSharp.SKSizeI GetRawSurfaceSize ();
```


#### Type Changed: SkiaSharp.Views.Tizen.SKCanvasView

Added method:

```csharp
protected override SkiaSharp.SKSizeI GetRawSurfaceSize ();
```


#### Type Changed: SkiaSharp.Views.Tizen.SKPaintSurfaceEventArgs

Added constructor:

```csharp
public SKPaintSurfaceEventArgs (SkiaSharp.SKSurface surface, SkiaSharp.SKImageInfo info, SkiaSharp.SKImageInfo rawInfo);
```

Added property:

```csharp
public SkiaSharp.SKImageInfo RawInfo { get; }
```


#### Type Changed: SkiaSharp.Views.Tizen.ScalingInfo

Added method:

```csharp
public static void SetScalingFactor (double? scalingFactor);
```



