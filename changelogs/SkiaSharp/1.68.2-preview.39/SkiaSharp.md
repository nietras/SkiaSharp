# API diff: SkiaSharp.dll

## SkiaSharp.dll

### Namespace SkiaSharp

#### Type Changed: SkiaSharp.SKBitmap

Added methods:

```csharp
public static SKBitmap Decode (System.ReadOnlySpan<byte> buffer);
public static SKBitmap Decode (System.ReadOnlySpan<byte> buffer, SKImageInfo bitmapInfo);
public static SKImageInfo DecodeBounds (System.ReadOnlySpan<byte> buffer);
public SKData Encode (SKEncodedImageFormat format, int quality);
public bool Encode (System.IO.Stream dst, SKEncodedImageFormat format, int quality);
public SKBitmap Resize (SKSizeI size, SKFilterQuality quality);
```


#### Type Changed: SkiaSharp.SKCanvas

Added method:

```csharp
public int SaveLayer ();
```


#### Type Changed: SkiaSharp.SKColor

Modified methods:

```diff
-public override bool Equals (object obj)
+public override bool Equals (object other)
```


#### Type Changed: SkiaSharp.SKDynamicMemoryWStream

Added methods:

```csharp
public bool CopyTo (System.IO.Stream dst);
public void CopyTo (System.Span<byte> data);
```


#### Type Changed: SkiaSharp.SKImage

Obsoleted methods:

```diff
 [Obsolete ("Use FromPixels (SKImageInfo, SKData, int) instead.")]
 public static SKImage FromPixelData (SKImageInfo info, SKData data, int rowBytes);
```

Added method:

```csharp
public static SKImage FromPixels (SKImageInfo info, SKData data);
```


#### Type Changed: SkiaSharp.SKImageInfo

Added method:

```csharp
public SKImageInfo WithSize (SKSizeI size);
```


#### Type Changed: SkiaSharp.SKMask

Added methods:

```csharp
public static SKMask Create (System.ReadOnlySpan<byte> image, SKRectI bounds, uint rowBytes, SKMaskFormat format);
public System.Span<byte> GetImageSpan ();
```


#### Type Changed: SkiaSharp.SKMatrix

Added constructor:

```csharp
public SKMatrix (float[] values);
```

Added property:

```csharp
public bool IsIdentity { get; }
```

Added method:

```csharp
public SKPoint MapVector (SKPoint vector);
```


#### Type Changed: SkiaSharp.SKMatrix44

Added methods:

```csharp
public void Set3x3ColumnMajor (float[] src);
public void Set3x3RowMajor (float[] src);
```


#### Type Changed: SkiaSharp.SKPMColor

Modified methods:

```diff
-public override bool Equals (object obj)
+public override bool Equals (object other)
```


#### Type Changed: SkiaSharp.SKPath

Added method:

```csharp
public void Transform (SKMatrix matrix, SKPath destination);
```


#### Type Changed: SkiaSharp.SKPathMeasure

Added methods:

```csharp
public SKMatrix GetMatrix (float distance, SKPathMeasureMatrixFlags flags);
public SKPoint GetPosition (float distance);
public SKPath GetSegment (float start, float stop, bool startWithMoveTo);
public SKPoint GetTangent (float distance);
public void SetPath (SKPath path);
```


#### Type Changed: SkiaSharp.SKPixmap

Obsoleted methods:

```diff
 [Obsolete ("Use Encode(SKWStream, SKJpegEncoderOptions) instead.")]
 public static bool Encode (SKWStream dst, SKPixmap src, SKJpegEncoderOptions options);
 [Obsolete ("Use Encode(SKWStream, SKPngEncoderOptions) instead.")]
 public static bool Encode (SKWStream dst, SKPixmap src, SKPngEncoderOptions options);
 [Obsolete ("Use Encode(SKWStream, SKWebpEncoderOptions) instead.")]
 public static bool Encode (SKWStream dst, SKPixmap src, SKWebpEncoderOptions options);
 [Obsolete ("Use Encode(SKWStream, SKEncodedImageFormat, int) instead.")]
 public static bool Encode (SKWStream dst, SKBitmap src, SKEncodedImageFormat format, int quality);
 [Obsolete ("Use Encode(SKWStream, SKEncodedImageFormat, int) instead.")]
 public static bool Encode (SKWStream dst, SKPixmap src, SKEncodedImageFormat encoder, int quality);
```

Added methods:

```csharp
public bool Encode (System.IO.Stream dst, SKJpegEncoderOptions options);
public bool Encode (System.IO.Stream dst, SKPngEncoderOptions options);
public bool Encode (System.IO.Stream dst, SKWebpEncoderOptions options);
public bool Encode (System.IO.Stream dst, SKEncodedImageFormat encoder, int quality);
```


#### Type Changed: SkiaSharp.SKSvgCanvas

Obsoleted methods:

```diff
 [Obsolete ("Use Create(SKRect, Stream) instead.")]
 public static SKCanvas Create (SKRect bounds, SKXmlWriter writer);
```

Added methods:

```csharp
public static SKCanvas Create (SKRect bounds, SKWStream stream);
public static SKCanvas Create (SKRect bounds, System.IO.Stream stream);
```


#### Type Changed: SkiaSharp.SKSwizzle

Added method:

```csharp
public static void SwapRedBlue (System.Span<byte> pixels);
```


#### Type Changed: SkiaSharp.SKTypeface

Added property:

```csharp
public int GlyphCount { get; }
```

Obsoleted methods:

```diff
 [Obsolete ("Use CountGlyphs(byte[], SKTextEncoding) instead.")]
 public int CountGlyphs (byte[] str, SKEncoding encoding);
 [Obsolete ("Use CountGlyphs(ReadOnlySpan<byte>, SKTextEncoding) instead.")]
 public int CountGlyphs (System.ReadOnlySpan<byte> str, SKEncoding encoding);
 [Obsolete ("Use CountGlyphs(string) instead.")]
 public int CountGlyphs (string str, SKEncoding encoding);
 [Obsolete ("Use CountGlyphs(ReadOnlySpan<byte>, SKTextEncoding) instead.")]
 public int CountGlyphs (IntPtr str, int strLen, SKEncoding encoding);
 [Obsolete ("Use GetGlyphs(ReadOnlySpan<byte>, SKTextEncoding) instead.")]
 public ushort[] GetGlyphs (byte[] text, SKEncoding encoding);
 [Obsolete ("Use GetGlyphs(ReadOnlySpan<byte>, SKTextEncoding) instead.")]
 public ushort[] GetGlyphs (System.ReadOnlySpan<byte> text, SKEncoding encoding);
 [Obsolete ("Use GetGlyphs(string) instead.")]
 public ushort[] GetGlyphs (string text, SKEncoding encoding);
 [Obsolete ("Use GetGlyphs(string) instead.")]
 public int GetGlyphs (string text, out ushort[] glyphs);
 [Obsolete ("Use GetGlyphs(byte[], SKTextEncoding) instead.")]
 public int GetGlyphs (byte[] text, SKEncoding encoding, out ushort[] glyphs);
 [Obsolete ("Use GetGlyphs(IntPtr, int, SKTextEncoding) instead.")]
 public ushort[] GetGlyphs (IntPtr text, int length, SKEncoding encoding);
 [Obsolete ("Use GetGlyphs(ReadOnlySpan<byte>, SKTextEncoding) instead.")]
 public int GetGlyphs (System.ReadOnlySpan<byte> text, SKEncoding encoding, out ushort[] glyphs);
 [Obsolete ("Use GetGlyphs(string) instead.")]
 public int GetGlyphs (string text, SKEncoding encoding, out ushort[] glyphs);
 [Obsolete ("Use GetGlyphs(IntPtr, int, SKTextEncoding) instead.")]
 public int GetGlyphs (IntPtr text, int length, SKEncoding encoding, out ushort[] glyphs);
```

Added methods:

```csharp
public bool ContainsGlyphs (System.ReadOnlySpan<char> text);
public bool ContainsGlyphs (string text);
public bool ContainsGlyphs (System.ReadOnlySpan<byte> text, SKTextEncoding encoding);
public bool ContainsGlyphs (IntPtr text, int length, SKTextEncoding encoding);
public int CountGlyphs (System.ReadOnlySpan<char> str);
public int CountGlyphs (byte[] str, SKTextEncoding encoding);
public int CountGlyphs (System.ReadOnlySpan<byte> str, SKTextEncoding encoding);
public int CountGlyphs (IntPtr str, int strLen, SKTextEncoding encoding);
public ushort[] GetGlyphs (System.ReadOnlySpan<char> text);
public ushort[] GetGlyphs (System.ReadOnlySpan<byte> text, SKTextEncoding encoding);
public ushort[] GetGlyphs (IntPtr text, int length, SKTextEncoding encoding);
public int[] GetKerningPairAdjustments (System.ReadOnlySpan<ushort> glyphs);
```


#### Type Changed: SkiaSharp.SkiaExtensions

Added methods:

```csharp
public static SKAlphaType GetAlphaType (this SKColorType colorType, SKAlphaType alphaType);
public static int GetBytesPerPixel (this SKColorType colorType);
public static SKTextEncoding ToTextEncoding (this SKEncoding encoding);
```


#### Type Changed: SkiaSharp.StringUtilities

Obsoleted methods:

```diff
 [Obsolete ("Use GetEncodedText(string, SKTextEncoding) instead.")]
 public static byte[] GetEncodedText (string text, SKEncoding encoding);
```

Added methods:

```csharp
public static byte[] GetEncodedText (System.ReadOnlySpan<char> text, SKTextEncoding encoding);
public static string GetString (System.ReadOnlySpan<byte> data, SKTextEncoding encoding);
public static string GetString (System.ReadOnlySpan<byte> data, int index, int count, SKTextEncoding encoding);
```



