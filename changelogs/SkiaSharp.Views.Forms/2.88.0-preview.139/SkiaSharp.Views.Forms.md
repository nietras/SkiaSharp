# API diff: SkiaSharp.Views.Forms.dll

## SkiaSharp.Views.Forms.dll

### Namespace SkiaSharp.Views.Forms

#### Type Changed: SkiaSharp.Views.Forms.Resource

#### Type Changed: SkiaSharp.Views.Forms.Resource.Attribute

Added field:

```csharp
public static int ignorePixelScaling;
```


#### Type Changed: SkiaSharp.Views.Forms.Resource.Styleable

Added fields:

```csharp
public static int[] SKCanvasView;
public static int SKCanvasView_ignorePixelScaling;
```



#### Type Changed: SkiaSharp.Views.Forms.SKPaintSurfaceEventArgs

Added constructor:

```csharp
public SKPaintSurfaceEventArgs (SkiaSharp.SKSurface surface, SkiaSharp.SKImageInfo info, SkiaSharp.SKImageInfo rawInfo);
```

Added property:

```csharp
public SkiaSharp.SKImageInfo RawInfo { get; }
```



