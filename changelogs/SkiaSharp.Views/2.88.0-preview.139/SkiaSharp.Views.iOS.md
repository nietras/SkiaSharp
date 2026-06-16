# API diff: SkiaSharp.Views.iOS.dll

## SkiaSharp.Views.iOS.dll

### Namespace SkiaSharp.Views.iOS

#### Type Changed: SkiaSharp.Views.iOS.SKCanvasView

Added method:

```csharp
public override void WillMoveToWindow (UIKit.UIWindow window);
```


#### Type Changed: SkiaSharp.Views.iOS.SKPaintSurfaceEventArgs

Added constructor:

```csharp
public SKPaintSurfaceEventArgs (SkiaSharp.SKSurface surface, SkiaSharp.SKImageInfo info, SkiaSharp.SKImageInfo rawInfo);
```

Added property:

```csharp
public SkiaSharp.SKImageInfo RawInfo { get; }
```



