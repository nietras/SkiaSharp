# API diff: SkiaSharp.dll

## SkiaSharp.dll

### Namespace SkiaSharp

#### Type Changed: SkiaSharp.GRContext

Removed method:

```csharp
public int GetMaxSurfaceSampleCountForColorType (SKColorType colorType);
```

Added method:

```csharp
public int GetMaxSurfaceSampleCount (SKColorType colorType);
```


#### Type Changed: SkiaSharp.SKBitmap

Added methods:

```csharp
public SKBitmap Resize (SKImageInfo info, SKFilterQuality quality);
public bool ScalePixels (SKBitmap destination, SKFilterQuality quality);
public bool ScalePixels (SKPixmap destination, SKFilterQuality quality);
```


#### Type Changed: SkiaSharp.SKCanvas

Added method:

```csharp
public void DrawText (SKTextBlob text, float x, float y, SKPaint paint);
```


#### Type Changed: SkiaSharp.SKCodec

Added methods:

```csharp
public static SKCodec Create (System.IO.Stream stream);
public static SKCodec Create (string filename);
public static SKCodec Create (System.IO.Stream stream, out SKCodecResult result);
public static SKCodec Create (string filename, out SKCodecResult result);
```


#### Type Changed: SkiaSharp.SKDocument

Modified methods:

```diff
 public SKDocument CreatePdf (string path, float dpi--- = 72---)
 public SKDocument CreateXps (SKWStream stream, float dpi--- = 72---)
 public SKDocument CreateXps (string path, float dpi--- = 72---)
```

Added methods:

```csharp
public static SKDocument CreatePdf (System.IO.Stream stream);
public static SKDocument CreatePdf (string path);
public static SKDocument CreatePdf (System.IO.Stream stream, SKDocumentPdfMetadata metadata);
public static SKDocument CreatePdf (System.IO.Stream stream, float dpi);
public static SKDocument CreatePdf (string path, SKDocumentPdfMetadata metadata);
public static SKDocument CreateXps (SKWStream stream);
public static SKDocument CreateXps (System.IO.Stream stream);
public static SKDocument CreateXps (string path);
public static SKDocument CreateXps (System.IO.Stream stream, float dpi);
```


#### Type Changed: SkiaSharp.SKDocumentPdfMetadata

Added constructors:

```csharp
public SKDocumentPdfMetadata (int encodingQuality);
public SKDocumentPdfMetadata (float rasterDpi);
public SKDocumentPdfMetadata (float rasterDpi, int encodingQuality);
```

Added fields:

```csharp
public static SKDocumentPdfMetadata Default;
public static const int DefaultEncodingQuality;
public static const float DefaultRasterDpi;
```

Added properties:

```csharp
public int EncodingQuality { get; set; }
public bool PdfA { get; set; }
public float RasterDpi { get; set; }
```


#### Type Changed: SkiaSharp.SKFileStream

Added property:

```csharp
public bool IsValid { get; }
```


#### Type Changed: SkiaSharp.SKFileWStream

Added property:

```csharp
public bool IsValid { get; }
```


#### Type Changed: SkiaSharp.SKImageFilter

Added method:

```csharp
public static SKImageFilter CreateAlphaThreshold (SKRegion region, float innerThreshold, float outerThreshold, SKImageFilter input);
```


#### Type Changed: SkiaSharp.SKPaint

Modified methods:

```diff
 public bool GetFillPath (SKPath src, SKPath dst, float resScale--- = 1---)
 public bool GetFillPath (SKPath src, SKPath dst, SKRect cullRect, float resScale--- = 1---)
```

Added methods:

```csharp
public bool ContainsGlyphs (byte[] text);
public bool ContainsGlyphs (string text);
public bool ContainsGlyphs (IntPtr text, int length);
public int CountGlyphs (byte[] text);
public int CountGlyphs (string text);
public int CountGlyphs (IntPtr text, int length);
public SKPath GetFillPath (SKPath src);
public bool GetFillPath (SKPath src, SKPath dst);
public SKPath GetFillPath (SKPath src, SKRect cullRect);
public SKPath GetFillPath (SKPath src, float resScale);
public bool GetFillPath (SKPath src, SKPath dst, SKRect cullRect);
public SKPath GetFillPath (SKPath src, SKRect cullRect, float resScale);
public float[] GetGlyphWidths (byte[] text);
public float[] GetGlyphWidths (string text);
public float[] GetGlyphWidths (byte[] text, out SKRect[] bounds);
public float[] GetGlyphWidths (IntPtr text, int length);
public float[] GetGlyphWidths (string text, out SKRect[] bounds);
public float[] GetGlyphWidths (IntPtr text, int length, out SKRect[] bounds);
public ushort[] GetGlyphs (byte[] text);
public ushort[] GetGlyphs (string text);
public ushort[] GetGlyphs (IntPtr text, int length);
public float[] GetHorizontalTextIntercepts (byte[] text, float[] xpositions, float y, float upperBounds, float lowerBounds);
public float[] GetHorizontalTextIntercepts (string text, float[] xpositions, float y, float upperBounds, float lowerBounds);
public float[] GetHorizontalTextIntercepts (IntPtr text, int length, float[] xpositions, float y, float upperBounds, float lowerBounds);
public float[] GetPositionedTextIntercepts (byte[] text, SKPoint[] positions, float upperBounds, float lowerBounds);
public float[] GetPositionedTextIntercepts (string text, SKPoint[] positions, float upperBounds, float lowerBounds);
public float[] GetPositionedTextIntercepts (IntPtr text, int length, SKPoint[] positions, float upperBounds, float lowerBounds);
public float[] GetTextIntercepts (SKTextBlob text, float upperBounds, float lowerBounds);
public float[] GetTextIntercepts (byte[] text, float x, float y, float upperBounds, float lowerBounds);
public float[] GetTextIntercepts (string text, float x, float y, float upperBounds, float lowerBounds);
public float[] GetTextIntercepts (IntPtr text, int length, float x, float y, float upperBounds, float lowerBounds);
```


#### Type Changed: SkiaSharp.SKPath

Added method:

```csharp
public SKRect GetRect ();
```


#### Type Changed: SkiaSharp.SKPoint

Added properties:

```csharp
public float Length { get; }
public float LengthSquared { get; }
```

Added methods:

```csharp
public static float Distance (SKPoint point, SKPoint other);
public static float DistanceSquared (SKPoint point, SKPoint other);
public static SKPoint Normalize (SKPoint point);
public static SKPoint Reflect (SKPoint point, SKPoint normal);
```


#### Type Changed: SkiaSharp.SKPointI

Added properties:

```csharp
public int Length { get; }
public int LengthSquared { get; }
```

Added methods:

```csharp
public static float Distance (SKPointI point, SKPointI other);
public static float DistanceSquared (SKPointI point, SKPointI other);
public static SKPointI Normalize (SKPointI point);
public static SKPointI Reflect (SKPointI point, SKPointI normal);
```


#### Type Changed: SkiaSharp.SKRectI

Added method:

```csharp
public bool IntersectsWithInclusive (SKRectI rect);
```


#### Type Changed: SkiaSharp.SKSurface

Obsoleted properties:

```diff
 [Obsolete ("Use SurfaceProperties instead.")]
 public SKSurfaceProps SurfaceProps { get; }
```

Added property:

```csharp
public SKSurfaceProperties SurfaceProperties { get; }
```

Removed methods:

```csharp
public static SKSurface Create (SKImageInfo info, int rowBytes, SKSurfaceProps props);
public static SKSurface Create (SKImageInfo info, IntPtr pixels, SKSurfaceProps props);
public static SKSurface Create (GRContext context, GRBackendRenderTarget renderTarget, SKColorType colorType, SKSurfaceProps props);
public static SKSurface Create (GRContext context, GRBackendTexture texture, SKColorType colorType, SKSurfaceProps props);
public static SKSurface Create (GRContext context, bool budgeted, SKImageInfo info, SKSurfaceProps props);
public static SKSurface Create (GRContext context, GRBackendRenderTarget renderTarget, GRSurfaceOrigin origin, SKColorType colorType, SKSurfaceProps props);
public static SKSurface Create (GRContext context, GRBackendTexture texture, GRSurfaceOrigin origin, SKColorType colorType, SKSurfaceProps props);
public static SKSurface Create (GRContext context, GRBackendRenderTarget renderTarget, GRSurfaceOrigin origin, SKColorType colorType, SKColorSpace colorspace, SKSurfaceProps props);
public static SKSurface Create (GRContext context, GRBackendTexture texture, GRSurfaceOrigin origin, int sampleCount, SKColorType colorType, SKSurfaceProps props);
public static SKSurface Create (SKImageInfo info, IntPtr pixels, int rowBytes, SKSurfaceReleaseDelegate releaseProc, object context, SKSurfaceProps props);
public static SKSurface Create (GRContext context, GRBackendTexture texture, GRSurfaceOrigin origin, int sampleCount, SKColorType colorType, SKColorSpace colorspace, SKSurfaceProps props);
public static SKSurface Create (GRContext context, bool budgeted, SKImageInfo info, int sampleCount, GRSurfaceOrigin origin, SKSurfaceProps props, bool shouldCreateWithMips);
public static SKSurface CreateAsRenderTarget (GRContext context, GRBackendTexture texture, SKColorType colorType, SKSurfaceProps props);
public static SKSurface CreateAsRenderTarget (GRContext context, GRBackendTexture texture, GRSurfaceOrigin origin, SKColorType colorType, SKSurfaceProps props);
public static SKSurface CreateAsRenderTarget (GRContext context, GRBackendTexture texture, GRSurfaceOrigin origin, int sampleCount, SKColorType colorType, SKSurfaceProps props);
public static SKSurface CreateAsRenderTarget (GRContext context, GRBackendTexture texture, GRSurfaceOrigin origin, int sampleCount, SKColorType colorType, SKColorSpace colorspace, SKSurfaceProps props);
```

Obsoleted methods:

```diff
 [Obsolete ("Use Create(SKImageInfo, SKSurfaceProperties) instead.")]
 public static SKSurface Create (SKImageInfo info, SKSurfaceProps props);
 [Obsolete ("Use Create(SKPixmap, SKSurfaceProperties) instead.")]
 public static SKSurface Create (SKPixmap pixmap, SKSurfaceProps props);
 [Obsolete ("Use Create(SKImageInfo, IntPtr, rowBytes, SKSurfaceProperties) instead.")]
 public static SKSurface Create (SKImageInfo info, IntPtr pixels, int rowBytes, SKSurfaceProps props);
 [Obsolete ("Use Create(GRContext, bool, SKImageInfo, int, SKSurfaceProperties) instead.")]
 public static SKSurface Create (GRContext context, bool budgeted, SKImageInfo info, int sampleCount, SKSurfaceProps props);
```

Added methods:

```csharp
public static SKSurface Create (SKImageInfo info, SKSurfaceProperties props);
public static SKSurface Create (SKPixmap pixmap, SKSurfaceProperties props);
public static SKSurface Create (SKImageInfo info, int rowBytes, SKSurfaceProperties props);
public static SKSurface Create (SKImageInfo info, IntPtr pixels, SKSurfaceProperties props);
public static SKSurface Create (GRContext context, GRBackendRenderTarget renderTarget, SKColorType colorType, SKSurfaceProperties props);
public static SKSurface Create (GRContext context, GRBackendTexture texture, SKColorType colorType, SKSurfaceProperties props);
public static SKSurface Create (GRContext context, bool budgeted, SKImageInfo info, SKSurfaceProperties props);
public static SKSurface Create (SKImageInfo info, IntPtr pixels, int rowBytes, SKSurfaceProperties props);
public static SKSurface Create (GRContext context, GRBackendRenderTarget renderTarget, GRSurfaceOrigin origin, SKColorType colorType, SKSurfaceProperties props);
public static SKSurface Create (GRContext context, GRBackendTexture texture, GRSurfaceOrigin origin, SKColorType colorType, SKSurfaceProperties props);
public static SKSurface Create (GRContext context, bool budgeted, SKImageInfo info, int sampleCount, SKSurfaceProperties props);
public static SKSurface Create (GRContext context, GRBackendRenderTarget renderTarget, GRSurfaceOrigin origin, SKColorType colorType, SKColorSpace colorspace, SKSurfaceProperties props);
public static SKSurface Create (GRContext context, GRBackendTexture texture, GRSurfaceOrigin origin, int sampleCount, SKColorType colorType, SKSurfaceProperties props);
public static SKSurface Create (SKImageInfo info, IntPtr pixels, int rowBytes, SKSurfaceReleaseDelegate releaseProc, object context, SKSurfaceProperties props);
public static SKSurface Create (GRContext context, GRBackendTexture texture, GRSurfaceOrigin origin, int sampleCount, SKColorType colorType, SKColorSpace colorspace, SKSurfaceProperties props);
public static SKSurface Create (GRContext context, bool budgeted, SKImageInfo info, int sampleCount, GRSurfaceOrigin origin, SKSurfaceProperties props, bool shouldCreateWithMips);
public static SKSurface CreateAsRenderTarget (GRContext context, GRBackendTexture texture, SKColorType colorType, SKSurfaceProperties props);
public static SKSurface CreateAsRenderTarget (GRContext context, GRBackendTexture texture, GRSurfaceOrigin origin, SKColorType colorType, SKSurfaceProperties props);
public static SKSurface CreateAsRenderTarget (GRContext context, GRBackendTexture texture, GRSurfaceOrigin origin, int sampleCount, SKColorType colorType, SKSurfaceProperties props);
public static SKSurface CreateAsRenderTarget (GRContext context, GRBackendTexture texture, GRSurfaceOrigin origin, int sampleCount, SKColorType colorType, SKColorSpace colorspace, SKSurfaceProperties props);
```


#### Type Changed: SkiaSharp.SKTypeface

Obsoleted methods:

```diff
 [Obsolete ("Use GetGlyphs(string, out ushort[]) instead.")]
 public int CharsToGlyphs (string chars, out ushort[] glyphs);
 [Obsolete ("Use GetGlyphs(IntPtr, int, SKEncoding, out ushort[]) instead.")]
 public int CharsToGlyphs (IntPtr str, int strlen, SKEncoding encoding, out ushort[] glyphs);
```

Added methods:

```csharp
public int CountGlyphs (byte[] str, SKEncoding encoding);
public int CountGlyphs (string str, SKEncoding encoding);
public ushort[] GetGlyphs (string text);
public ushort[] GetGlyphs (byte[] text, SKEncoding encoding);
public ushort[] GetGlyphs (string text, SKEncoding encoding);
public int GetGlyphs (string text, out ushort[] glyphs);
public int GetGlyphs (byte[] text, SKEncoding encoding, out ushort[] glyphs);
public ushort[] GetGlyphs (IntPtr text, int length, SKEncoding encoding);
public int GetGlyphs (string text, SKEncoding encoding, out ushort[] glyphs);
public int GetGlyphs (IntPtr text, int length, SKEncoding encoding, out ushort[] glyphs);
```


#### Type Changed: SkiaSharp.StringUtilities

Added method:

```csharp
public static byte[] GetEncodedText (string text, SKEncoding encoding);
```


#### New Type: SkiaSharp.SKSurfaceProperties

```csharp
public class SKSurfaceProperties : SkiaSharp.SKObject, System.IDisposable {
	// constructors
	public SKSurfaceProperties (SKPixelGeometry pixelGeometry);

	[Obsolete]
public SKSurfaceProperties (SKSurfaceProps props);
	public SKSurfaceProperties (SKSurfacePropsFlags flags, SKPixelGeometry pixelGeometry);
	public SKSurfaceProperties (uint flags, SKPixelGeometry pixelGeometry);
	// properties
	public SKSurfacePropsFlags Flags { get; }
	public bool IsUseDeviceIndependentFonts { get; }
	public SKPixelGeometry PixelGeometry { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

#### New Type: SkiaSharp.SKTextBlob

```csharp
public class SKTextBlob : SkiaSharp.SKObject, System.IDisposable {
	// properties
	public SKRect Bounds { get; }
	public uint UniqueId { get; }
	// methods
	protected override void Dispose (bool disposing);
}
```

#### New Type: SkiaSharp.SKTextBlobBuilder

```csharp
public class SKTextBlobBuilder : SkiaSharp.SKObject, System.IDisposable {
	// constructors
	public SKTextBlobBuilder ();
	// methods
	public void AddHorizontalRun (SKPaint font, float y, ushort[] glyphs, float[] positions);
	public void AddHorizontalRun (SKPaint font, float y, ushort[] glyphs, float[] positions, SKRect bounds);
	public void AddHorizontalRun (SKPaint font, float y, ushort[] glyphs, float[] positions, byte[] utf8Text, uint[] clusters);
	public void AddHorizontalRun (SKPaint font, float y, ushort[] glyphs, float[] positions, string text, uint[] clusters);
	public void AddHorizontalRun (SKPaint font, float y, ushort[] glyphs, float[] positions, byte[] utf8Text, uint[] clusters, SKRect bounds);
	public void AddHorizontalRun (SKPaint font, float y, ushort[] glyphs, float[] positions, string text, uint[] clusters, SKRect bounds);
	public void AddPositionedRun (SKPaint font, ushort[] glyphs, SKPoint[] positions);
	public void AddPositionedRun (SKPaint font, ushort[] glyphs, SKPoint[] positions, SKRect bounds);
	public void AddPositionedRun (SKPaint font, ushort[] glyphs, SKPoint[] positions, byte[] utf8Text, uint[] clusters);
	public void AddPositionedRun (SKPaint font, ushort[] glyphs, SKPoint[] positions, string text, uint[] clusters);
	public void AddPositionedRun (SKPaint font, ushort[] glyphs, SKPoint[] positions, byte[] utf8Text, uint[] clusters, SKRect bounds);
	public void AddPositionedRun (SKPaint font, ushort[] glyphs, SKPoint[] positions, string text, uint[] clusters, SKRect bounds);
	public void AddRun (SKPaint font, float x, float y, ushort[] glyphs);
	public void AddRun (SKPaint font, float x, float y, ushort[] glyphs, SKRect bounds);
	public void AddRun (SKPaint font, float x, float y, ushort[] glyphs, byte[] utf8Text, uint[] clusters);
	public void AddRun (SKPaint font, float x, float y, ushort[] glyphs, string text, uint[] clusters);
	public void AddRun (SKPaint font, float x, float y, ushort[] glyphs, byte[] utf8Text, uint[] clusters, SKRect bounds);
	public void AddRun (SKPaint font, float x, float y, ushort[] glyphs, string text, uint[] clusters, SKRect bounds);
	public SKTextBlob Build ();
	protected override void Dispose (bool disposing);
}
```


