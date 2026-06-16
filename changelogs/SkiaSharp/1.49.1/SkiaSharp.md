# API diff: SkiaSharp.dll

## SkiaSharp.dll

> Assembly Version Changed: 1.49.0.0 vs 1.0.0.0

### Namespace SkiaSharp

#### Type Changed: SkiaSharp.SKBitmap

Added methods:

```csharp
public IntPtr GetPixels (out IntPtr length);
public void LockPixels ();
public void UnlockPixels ();
```


#### Type Changed: SkiaSharp.SKCanvas

Added methods:

```csharp
public void DrawText (IntPtr buffer, int length, SKPoint[] points, SKPaint paint);
public void DrawText (IntPtr buffer, int length, float x, float y, SKPaint paint);
public void DrawText (IntPtr buffer, int length, SKPath path, float hOffset, float vOffset, SKPaint paint);
```


#### Type Changed: SkiaSharp.SKColorFilter

Removed fields:

```csharp
public static const int MAX_CUBE_SIZE;
public static const int MIN_CUBE_SIZE;
```

Added fields:

```csharp
public static const int MaxCubeSize;
public static const int MinCubeSize;
```


#### Type Changed: SkiaSharp.SKData

Removed method:

```csharp
public static SKData FromMallocMemory (byte[] bytes);
```

Added method:

```csharp
public System.IO.Stream AsStream ();
```


#### Type Changed: SkiaSharp.SKDropShadowImageFilterShadowMode

Removed value:

```csharp
DawShadowOnly = 1,
```

Added value:

```csharp
DrawShadowOnly = 1,
```


#### Type Changed: SkiaSharp.SKImage

Added methods:

```csharp
public SKData Encode (SKImageEncodeFormat format, int quality);
public static SKImage FromData (SKData data);
```


#### Type Changed: SkiaSharp.SKPaint

Added methods:

```csharp
public long BreakText (string text, float maxWidth);
public long BreakText (string text, float maxWidth, out float measuredWidth);
public long BreakText (IntPtr buffer, IntPtr length, float maxWidth, out float measuredWidth);
public float MeasureText (string text);
public float MeasureText (IntPtr buffer, IntPtr length);
public float MeasureText (string text, ref SKRect bounds);
public float MeasureText (IntPtr buffer, IntPtr length, ref SKRect bounds);
```


#### Type Changed: SkiaSharp.SKPoint

Removed fields:

```csharp
public float X;
public float Y;
```

Added field:

```csharp
public static SKPoint Empty;
```

Added properties:

```csharp
public bool IsEmpty { get; }
public float X { get; set; }
public float Y { get; set; }
```

Added methods:

```csharp
public static SKPoint Add (SKPoint pt, SKSize sz);
public static SKPoint Add (SKPoint pt, SKSizeI sz);
public override bool Equals (object obj);
public override int GetHashCode ();
public static SKPoint Subtract (SKPoint pt, SKSize sz);
public static SKPoint Subtract (SKPoint pt, SKSizeI sz);
public override string ToString ();
public static SKPoint op_Addition (SKPoint pt, SKSize sz);
public static SKPoint op_Addition (SKPoint pt, SKSizeI sz);
public static bool op_Equality (SKPoint left, SKPoint right);
public static bool op_Inequality (SKPoint left, SKPoint right);
public static SKPoint op_Subtraction (SKPoint pt, SKSize sz);
public static SKPoint op_Subtraction (SKPoint pt, SKSizeI sz);
```


#### Type Changed: SkiaSharp.SKPoint3

Removed fields:

```csharp
public float X;
public float Y;
public float Z;
```

Added field:

```csharp
public static SKPoint3 Empty;
```

Added properties:

```csharp
public bool IsEmpty { get; }
public float X { get; set; }
public float Y { get; set; }
public float Z { get; set; }
```

Added methods:

```csharp
public override bool Equals (object obj);
public override int GetHashCode ();
public override string ToString ();
public static bool op_Equality (SKPoint3 left, SKPoint3 right);
public static bool op_Inequality (SKPoint3 left, SKPoint3 right);
```


#### Type Changed: SkiaSharp.SKPointI

Added constructor:

```csharp
public SKPointI (SKSizeI sz);
```

Removed fields:

```csharp
public int X;
public int Y;
```

Added field:

```csharp
public static SKPointI Empty;
```

Added properties:

```csharp
public bool IsEmpty { get; }
public int X { get; set; }
public int Y { get; set; }
```

Added methods:

```csharp
public static SKPointI Add (SKPointI pt, SKSizeI sz);
public static SKPointI Ceiling (SKPoint value);
public override bool Equals (object obj);
public override int GetHashCode ();
public void Offset (SKPointI p);
public void Offset (int dx, int dy);
public static SKPointI Round (SKPoint value);
public static SKPointI Subtract (SKPointI pt, SKSizeI sz);
public override string ToString ();
public static SKPointI Truncate (SKPoint value);
public static SKPointI op_Addition (SKPointI pt, SKSizeI sz);
public static bool op_Equality (SKPointI left, SKPointI right);
public static SKSizeI op_Explicit (SKPointI p);
public static SKPoint op_Implicit (SKPointI p);
public static bool op_Inequality (SKPointI left, SKPointI right);
public static SKPointI op_Subtraction (SKPointI pt, SKSizeI sz);
```


#### New Type: SkiaSharp.SKImageEncodeFormat

```csharp
[Serializable]
public enum SKImageEncodeFormat {
	Bmp = 1,
	Gif = 2,
	Ico = 3,
	Jpeg = 4,
	Ktx = 8,
	Png = 5,
	Unknown = 0,
	Wbmp = 6,
	Webp = 7,
}
```


