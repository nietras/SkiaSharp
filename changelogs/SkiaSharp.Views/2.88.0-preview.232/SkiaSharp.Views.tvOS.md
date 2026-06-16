# API diff: SkiaSharp.Views.tvOS.dll

## SkiaSharp.Views.tvOS.dll

### Namespace SkiaSharp.Views.tvOS

#### Type Changed: SkiaSharp.Views.tvOS.SKCanvasView

Added interface:

```csharp
UIKit.IUITraitChangeObservable
```


#### Type Changed: SkiaSharp.Views.tvOS.SKGLView

Added interface:

```csharp
UIKit.IUITraitChangeObservable
```


#### Type Changed: SkiaSharp.Views.tvOS.iOSExtensions

Removed methods:

```csharp
public static UIKit.UIImage ToUIImage (this SkiaSharp.SKBitmap skiaBitmap, ObjCRuntime.nfloat scale, UIKit.UIImageOrientation orientation);
public static UIKit.UIImage ToUIImage (this SkiaSharp.SKPixmap skiaPixmap, ObjCRuntime.nfloat scale, UIKit.UIImageOrientation orientation);
public static UIKit.UIImage ToUIImage (this SkiaSharp.SKPicture skiaPicture, SkiaSharp.SKSizeI dimensions, ObjCRuntime.nfloat scale, UIKit.UIImageOrientation orientation);
```

Added methods:

```csharp
public static UIKit.UIImage ToUIImage (this SkiaSharp.SKBitmap skiaBitmap, System.Runtime.InteropServices.NFloat scale, UIKit.UIImageOrientation orientation);
public static UIKit.UIImage ToUIImage (this SkiaSharp.SKPixmap skiaPixmap, System.Runtime.InteropServices.NFloat scale, UIKit.UIImageOrientation orientation);
public static UIKit.UIImage ToUIImage (this SkiaSharp.SKPicture skiaPicture, SkiaSharp.SKSizeI dimensions, System.Runtime.InteropServices.NFloat scale, UIKit.UIImageOrientation orientation);
```



