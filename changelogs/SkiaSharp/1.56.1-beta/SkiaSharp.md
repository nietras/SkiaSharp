# API diff: SkiaSharp.dll

## SkiaSharp.dll

### Namespace SkiaSharp

#### Type Changed: SkiaSharp.SKBitmap

Added method:

```csharp
public bool InstallMaskPixels (SKMask mask);
```


#### Type Changed: SkiaSharp.SKCanvas

Added methods:

```csharp
public void DrawAnnotation (SKRect rect, string key, SKData value);
public void DrawLinkDestinationAnnotation (SKRect rect, SKData value);
public SKData DrawLinkDestinationAnnotation (SKRect rect, string value);
public void DrawNamedDestinationAnnotation (SKPoint point, SKData value);
public SKData DrawNamedDestinationAnnotation (SKPoint point, string value);
public void DrawUrlAnnotation (SKRect rect, SKData value);
public SKData DrawUrlAnnotation (SKRect rect, string value);
```


#### Type Changed: SkiaSharp.SKData

Added constructor:

```csharp
public SKData (byte[] bytes, ulong length);
```


#### Type Changed: SkiaSharp.SKDocument

Added method:

```csharp
public static SKDocument CreatePdf (SKWStream stream, SKDocumentPdfMetadata metadata, float dpi);
```


#### Type Changed: SkiaSharp.SKStrokeJoin

Obsoleted fields:

```diff
 [Obsolete ("Use SKStrokeJoin.Miter instead.")]
 Mitter = 0,
```

Added value:

```csharp
Miter = 0,
```


#### Type Changed: SkiaSharp.SKWStream

Modified properties:

```diff
 public ---virtual--- int BytesWritten { get; }
```

Modified methods:

```diff
 public ---virtual--- void Flush ()
 public ---virtual--- bool Write (byte[] buffer, int size)
```


#### New Type: SkiaSharp.SK3dView

```csharp
public class SK3dView : SkiaSharp.SKObject, System.IDisposable {
	// constructors
	public SK3dView ();
	// properties
	public SKMatrix Matrix { get; }
	// methods
	public void ApplyToCanvas (SKCanvas canvas);
	protected override void Dispose (bool disposing);
	public void DotWithNormal (float dx, float dy, float dz);
	public void GetMatrix (ref SKMatrix matrix);
	public void Restore ();
	public void RotateXDegrees (float degrees);
	public void RotateXRadians (float radians);
	public void RotateYDegrees (float degrees);
	public void RotateYRadians (float radians);
	public void RotateZDegrees (float degrees);
	public void RotateZRadians (float radians);
	public void Save ();
	public void Translate (float x, float y, float z);
	public void TranslateX (float x);
	public void TranslateY (float y);
	public void TranslateZ (float z);
}
```

#### New Type: SkiaSharp.SKAutoMaskFreeImage

```csharp
public class SKAutoMaskFreeImage : System.IDisposable {
	// constructors
	public SKAutoMaskFreeImage (IntPtr maskImage);
	// methods
	public virtual void Dispose ();
}
```

#### New Type: SkiaSharp.SKDocumentPdfMetadata

```csharp
public struct SKDocumentPdfMetadata {
	// properties
	public string Author { get; set; }
	public System.DateTime? Creation { get; set; }
	public string Creator { get; set; }
	public string Keywords { get; set; }
	public System.DateTime? Modified { get; set; }
	public string Producer { get; set; }
	public string Subject { get; set; }
	public string Title { get; set; }
}
```

#### New Type: SkiaSharp.SKManagedWStream

```csharp
public class SKManagedWStream : SkiaSharp.SKWStream, System.IDisposable {
	// constructors
	public SKManagedWStream (System.IO.Stream managedStream);
	public SKManagedWStream (System.IO.Stream managedStream, bool disposeManagedStream);
	// methods
	protected override void Dispose (bool disposing);
}
```

#### New Type: SkiaSharp.SKMask

```csharp
public struct SKMask {
	// constructors
	public SKMask (SKRectI bounds, uint rowBytes, SKMaskFormat format);
	public SKMask (IntPtr image, SKRectI bounds, uint rowBytes, SKMaskFormat format);
	// properties
	public SKRectI Bounds { get; }
	public SKMaskFormat Format { get; }
	public IntPtr Image { get; }
	public bool IsEmpty { get; }
	public uint RowBytes { get; }
	// methods
	public long AllocateImage ();
	public static IntPtr AllocateImage (long size);
	public long ComputeImageSize ();
	public long ComputeTotalImageSize ();
	public static SKMask Create (byte[] image, SKRectI bounds, uint rowBytes, SKMaskFormat format);
	public void FreeImage ();
	public static void FreeImage (IntPtr image);
	public IntPtr GetAddr (int x, int y);
	public byte GetAddr1 (int x, int y);
	public ushort GetAddr16 (int x, int y);
	public uint GetAddr32 (int x, int y);
	public byte GetAddr8 (int x, int y);
}
```

#### New Type: SkiaSharp.SKMaskFormat

```csharp
[Serializable]
public enum SKMaskFormat {
	A8 = 1,
	Argb32 = 3,
	BW = 0,
	Lcd16 = 4,
	ThreeD = 2,
}
```

#### New Type: SkiaSharp.SKSvgCanvas

```csharp
public class SKSvgCanvas {
	// methods
	public static SKCanvas Create (SKRect bounds, SKXmlWriter writer);
}
```

#### New Type: SkiaSharp.SKXmlStreamWriter

```csharp
public class SKXmlStreamWriter : SkiaSharp.SKXmlWriter, System.IDisposable {
	// constructors
	public SKXmlStreamWriter (SKWStream stream);
	// methods
	protected override void Dispose (bool disposing);
}
```

#### New Type: SkiaSharp.SKXmlWriter

```csharp
public abstract class SKXmlWriter : SkiaSharp.SKObject, System.IDisposable {
}
```


