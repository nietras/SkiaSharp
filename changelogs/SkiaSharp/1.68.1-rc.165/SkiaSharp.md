# API diff: SkiaSharp.dll

## SkiaSharp.dll

### Namespace SkiaSharp

#### Type Changed: SkiaSharp.GRBackendRenderTarget

Added method:

```csharp
protected override void Dispose (bool disposing);
```


#### Type Changed: SkiaSharp.GRBackendTexture

Added method:

```csharp
protected override void Dispose (bool disposing);
```


#### Type Changed: SkiaSharp.GRContext

Added method:

```csharp
protected override void Dispose (bool disposing);
```


#### Type Changed: SkiaSharp.GRGlInterface

Added method:

```csharp
protected override void Dispose (bool disposing);
```


#### Type Changed: SkiaSharp.SK3dView

Added method:

```csharp
protected override void Dispose (bool disposing);
```


#### Type Changed: SkiaSharp.SKAbstractManagedStream

Added method:

```csharp
protected override void Dispose (bool disposing);
```


#### Type Changed: SkiaSharp.SKAbstractManagedWStream

Added method:

```csharp
protected override void Dispose (bool disposing);
```


#### Type Changed: SkiaSharp.SKBitmap

Added method:

```csharp
protected override void Dispose (bool disposing);
```


#### Type Changed: SkiaSharp.SKCanvas

Added methods:

```csharp
public void Discard ();
protected override void Dispose (bool disposing);
```


#### Type Changed: SkiaSharp.SKCodec

Added method:

```csharp
protected override void Dispose (bool disposing);
```


#### Type Changed: SkiaSharp.SKColorFilter

Added method:

```csharp
protected override void Dispose (bool disposing);
```


#### Type Changed: SkiaSharp.SKColorSpace

Added method:

```csharp
protected override void Dispose (bool disposing);
```


#### Type Changed: SkiaSharp.SKColorTable

Added method:

```csharp
protected override void Dispose (bool disposing);
```


#### Type Changed: SkiaSharp.SKData

Added method:

```csharp
protected override void Dispose (bool disposing);
```


#### Type Changed: SkiaSharp.SKDocument

Added method:

```csharp
protected override void Dispose (bool disposing);
```


#### Type Changed: SkiaSharp.SKDrawable

Added method:

```csharp
protected override void Dispose (bool disposing);
```


#### Type Changed: SkiaSharp.SKDynamicMemoryWStream

Added method:

```csharp
protected override void Dispose (bool disposing);
```


#### Type Changed: SkiaSharp.SKEncodedImageFormat

Added value:

```csharp
Heif = 11,
```


#### Type Changed: SkiaSharp.SKFileStream

Added method:

```csharp
protected override void Dispose (bool disposing);
```


#### Type Changed: SkiaSharp.SKFileWStream

Added method:

```csharp
protected override void Dispose (bool disposing);
```


#### Type Changed: SkiaSharp.SKFontManager

Added method:

```csharp
protected override void Dispose (bool disposing);
```


#### Type Changed: SkiaSharp.SKFontStyle

Added method:

```csharp
protected override void Dispose (bool disposing);
```


#### Type Changed: SkiaSharp.SKFontStyleSet

Added method:

```csharp
protected override void Dispose (bool disposing);
```


#### Type Changed: SkiaSharp.SKFrontBufferedManagedStream

Added method:

```csharp
protected override void Dispose (bool disposing);
```


#### Type Changed: SkiaSharp.SKImage

Added methods:

```csharp
public SKImage ApplyImageFilter (SKImageFilter filter, SKRectI subset, SKRectI clipBounds, out SKRectI outSubset, out SKPointI outOffset);
protected override void Dispose (bool disposing);
```


#### Type Changed: SkiaSharp.SKImageFilter

Added method:

```csharp
protected override void Dispose (bool disposing);
```

#### Type Changed: SkiaSharp.SKImageFilter.CropRect

Added method:

```csharp
protected override void Dispose (bool disposing);
```



#### Type Changed: SkiaSharp.SKManagedStream

Added method:

```csharp
protected override void Dispose (bool disposing);
```


#### Type Changed: SkiaSharp.SKManagedWStream

Added method:

```csharp
protected override void Dispose (bool disposing);
```


#### Type Changed: SkiaSharp.SKMaskFilter

Added method:

```csharp
protected override void Dispose (bool disposing);
```


#### Type Changed: SkiaSharp.SKMatrix44

Added method:

```csharp
protected override void Dispose (bool disposing);
```


#### Type Changed: SkiaSharp.SKMemoryStream

Added method:

```csharp
protected override void Dispose (bool disposing);
```


#### Type Changed: SkiaSharp.SKObject

Added method:

```csharp
protected override void Dispose (bool disposing);
```


#### Type Changed: SkiaSharp.SKPaint

Added method:

```csharp
protected override void Dispose (bool disposing);
```


#### Type Changed: SkiaSharp.SKPath

Added method:

```csharp
protected override void Dispose (bool disposing);
```

#### Type Changed: SkiaSharp.SKPath.Iterator

Added method:

```csharp
protected override void Dispose (bool disposing);
```


#### Type Changed: SkiaSharp.SKPath.OpBuilder

Added method:

```csharp
protected override void Dispose (bool disposing);
```


#### Type Changed: SkiaSharp.SKPath.RawIterator

Added method:

```csharp
protected override void Dispose (bool disposing);
```



#### Type Changed: SkiaSharp.SKPathEffect

Added method:

```csharp
protected override void Dispose (bool disposing);
```


#### Type Changed: SkiaSharp.SKPathMeasure

Added method:

```csharp
protected override void Dispose (bool disposing);
```


#### Type Changed: SkiaSharp.SKPicture

Added method:

```csharp
protected override void Dispose (bool disposing);
```


#### Type Changed: SkiaSharp.SKPictureRecorder

Added method:

```csharp
protected override void Dispose (bool disposing);
```


#### Type Changed: SkiaSharp.SKPixmap

Added method:

```csharp
protected override void Dispose (bool disposing);
```


#### Type Changed: SkiaSharp.SKRegion

Added method:

```csharp
protected override void Dispose (bool disposing);
```


#### Type Changed: SkiaSharp.SKRoundRect

Added methods:

```csharp
protected override void Dispose (bool disposing);
public bool TryTransform (SKMatrix matrix, out SKRoundRect transformed);
```


#### Type Changed: SkiaSharp.SKShader

Added methods:

```csharp
public static SKShader CreateLinearGradient (SKPoint start, SKPoint end, SKColor[] colors, SKShaderTileMode mode);
public static SKShader CreatePicture (SKPicture src, SKShaderTileMode tmx, SKShaderTileMode tmy, SKMatrix localMatrix, SKRect tile);
public static SKShader CreateRadialGradient (SKPoint center, float radius, SKColor[] colors, SKShaderTileMode mode);
public static SKShader CreateSweepGradient (SKPoint center, SKColor[] colors);
public static SKShader CreateSweepGradient (SKPoint center, SKColor[] colors, SKShaderTileMode tileMode, float startAngle, float endAngle);
public static SKShader CreateTwoPointConicalGradient (SKPoint start, float startRadius, SKPoint end, float endRadius, SKColor[] colors, SKShaderTileMode mode);
protected override void Dispose (bool disposing);
```


#### Type Changed: SkiaSharp.SKStream

Added method:

```csharp
public bool Move (int offset);
```


#### Type Changed: SkiaSharp.SKSurface

Added method:

```csharp
protected override void Dispose (bool disposing);
```


#### Type Changed: SkiaSharp.SKSurfaceProperties

Added method:

```csharp
protected override void Dispose (bool disposing);
```


#### Type Changed: SkiaSharp.SKTextBlob

Added method:

```csharp
protected override void Dispose (bool disposing);
```


#### Type Changed: SkiaSharp.SKTextBlobBuilder

Added method:

```csharp
protected override void Dispose (bool disposing);
```


#### Type Changed: SkiaSharp.SKTypeface

Added method:

```csharp
protected override void Dispose (bool disposing);
```


#### Type Changed: SkiaSharp.SKVertices

Added method:

```csharp
protected override void Dispose (bool disposing);
```


#### Type Changed: SkiaSharp.SKXmlStreamWriter

Added method:

```csharp
protected override void Dispose (bool disposing);
```



