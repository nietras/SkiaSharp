# API diff: SkiaSharp.dll

## SkiaSharp.dll

### Namespace SkiaSharp

#### Type Changed: SkiaSharp.SK3dView

Removed method:

```csharp
public void DotWithNormal (float dx, float dy, float dz);
```

Added method:

```csharp
public float DotWithNormal (float dx, float dy, float dz);
```


#### Type Changed: SkiaSharp.SKBitmap

Added methods:

```csharp
public bool ExtractAlpha (SKBitmap destination);
public bool ExtractAlpha (SKBitmap destination, SKPaint paint);
public bool ExtractAlpha (SKBitmap destination, out SKPointI offset);
public bool ExtractAlpha (SKBitmap destination, SKPaint paint, out SKPointI offset);
public bool ExtractSubset (SKBitmap destination, SKRectI subset);
public IntPtr GetAddr (int x, int y);
public ushort GetAddr16 (int x, int y);
public uint GetAddr32 (int x, int y);
public byte GetAddr8 (int x, int y);
```


#### Type Changed: SkiaSharp.SKCanvas

Obsoleted methods:

```diff
 [Obsolete ("Use DrawTextOnPath instead.")]
 public void DrawText (string text, SKPath path, float hOffset, float vOffset, SKPaint paint);
 [Obsolete ("Use DrawTextOnPath instead.")]
 public void DrawText (IntPtr buffer, int length, SKPath path, float hOffset, float vOffset, SKPaint paint);
```

Added methods:

```csharp
public void DrawPositionedText (byte[] text, SKPoint[] points, SKPaint paint);
public void DrawText (byte[] text, float x, float y, SKPaint paint);

[Obsolete ("Use DrawTextOnPath instead.")]
public void DrawText (byte[] text, SKPath path, float hOffset, float vOffset, SKPaint paint);
public void DrawTextOnPath (byte[] text, SKPath path, float hOffset, float vOffset, SKPaint paint);
public void DrawTextOnPath (string text, SKPath path, float hOffset, float vOffset, SKPaint paint);
public void DrawTextOnPath (IntPtr buffer, int length, SKPath path, float hOffset, float vOffset, SKPaint paint);
```


#### Type Changed: SkiaSharp.SKCodec

Added properties:

```csharp
public int NextScanline { get; }
public SKCodecScanlineOrder ScanlineOrder { get; }
```

Added methods:

```csharp
public int GetOutputScanline (int inputScanline);
public int GetScanlines (IntPtr dst, int countLines, int rowBytes);
public bool SkipScanlines (int countLines);
public SKCodecResult StartScanlineDecode (SKImageInfo info);
public SKCodecResult StartScanlineDecode (SKImageInfo info, SKCodecOptions options);
public SKCodecResult StartScanlineDecode (SKImageInfo info, SKCodecOptions options, SKColorTable colorTable, ref int colorTableCount);
public SKCodecResult StartScanlineDecode (SKImageInfo info, SKCodecOptions options, IntPtr colorTable, ref int colorTableCount);
```


#### Type Changed: SkiaSharp.SKMaskFilter

Added methods:

```csharp
public static SKMaskFilter CreateBlur (SKBlurStyle blurStyle, float sigma, SKBlurMaskFilterFlags flags);
public static SKMaskFilter CreateBlur (SKBlurStyle blurStyle, float sigma, SKRect occluder);
public static SKMaskFilter CreateBlur (SKBlurStyle blurStyle, float sigma, SKRect occluder, SKBlurMaskFilterFlags flags);
```


#### Type Changed: SkiaSharp.SKPaint

Added methods:

```csharp
public long BreakText (byte[] text, float maxWidth, out float measuredWidth);
public SKPath GetTextPath (byte[] text, SKPoint[] points);
public SKPath GetTextPath (byte[] text, float x, float y);
public float MeasureText (byte[] text);
public float MeasureText (byte[] text, ref SKRect bounds);
```


#### Type Changed: SkiaSharp.SKPath

Added property:

```csharp
public SKPathSegmentMask SegmentMasks { get; }
```

Added method:

```csharp
public void AddPoly (SKPoint[] points, bool close);
```


#### New Type: SkiaSharp.SKBlurMaskFilterFlags

```csharp
[Serializable]
[Flags]
public enum SKBlurMaskFilterFlags {
	All = 3,
	HighQuality = 2,
	IgnoreTransform = 1,
	None = 0,
}
```

#### New Type: SkiaSharp.SKCodecScanlineOrder

```csharp
[Serializable]
public enum SKCodecScanlineOrder {
	BottomUp = 1,
	TopDown = 0,
}
```

#### New Type: SkiaSharp.SKFontManager

```csharp
public class SKFontManager : SkiaSharp.SKObject, System.IDisposable {
	// properties
	public static SKFontManager Default { get; }
	public int FontFamilyCount { get; }
	// methods
	protected override void Dispose (bool disposing);
	public string GetFamilyName (int index);
	public string[] GetFontFamilies ();
	public SKTypeface MatchCharacter (char character);
	public SKTypeface MatchCharacter (int character);
	public SKTypeface MatchCharacter (string familyName, char character);
	public SKTypeface MatchCharacter (string familyName, int character);
	public SKTypeface MatchCharacter (string familyName, string[] bcp47, char character);
	public SKTypeface MatchCharacter (string familyName, string[] bcp47, int character);
	public SKTypeface MatchCharacter (string familyName, SKFontStyleWeight weight, SKFontStyleWidth width, SKFontStyleSlant slant, string[] bcp47, char character);
	public SKTypeface MatchCharacter (string familyName, SKFontStyleWeight weight, SKFontStyleWidth width, SKFontStyleSlant slant, string[] bcp47, int character);
	public SKTypeface MatchCharacter (string familyName, int weight, int width, SKFontStyleSlant slant, string[] bcp47, int character);
}
```

#### New Type: SkiaSharp.SKPathSegmentMask

```csharp
[Serializable]
[Flags]
public enum SKPathSegmentMask {
	Conic = 4,
	Cubic = 8,
	Line = 1,
	Quad = 2,
}
```

#### New Type: SkiaSharp.StringUtilities

```csharp
public static class StringUtilities {
	// methods
	public static byte[] GetEncodedText (string text, SKTextEncoding encoding);
	public static string GetString (byte[] data, SKTextEncoding encoding);
	public static string GetString (IntPtr data, int dataLength, SKTextEncoding encoding);
	public static int GetUnicodeCharacterCode (string character, SKTextEncoding encoding);
}
```


