# API diff: SkiaSharp.dll

## SkiaSharp.dll

### Namespace SkiaSharp

#### Type Changed: SkiaSharp.SKCanvas

Removed methods:

```csharp
public void Save ();
public void SaveLayer (SKPaint paint);
public void SaveLayer (SKRect limit, SKPaint paint);
```

Added methods:

```csharp
public int Save ();
public int SaveLayer (SKPaint paint);
public int SaveLayer (SKRect limit, SKPaint paint);
```


#### Type Changed: SkiaSharp.SKPaint

Added properties:

```csharp
public SKFilterQuality FilterQuality { get; set; }
public SKFontMetrics FontMetrics { get; }
public bool IsDither { get; set; }
public bool IsVerticalText { get; set; }
```

Added methods:

```csharp
public SKPath GetTextPath (string text, SKPoint[] points);
public SKPath GetTextPath (IntPtr buffer, IntPtr length, SKPoint[] points);
public SKPath GetTextPath (string text, float x, float y);
public SKPath GetTextPath (IntPtr buffer, IntPtr length, float x, float y);
```


#### Type Changed: SkiaSharp.SKPath

Added property:

```csharp
public SKPathFillType FillType { get; set; }
```

Added methods:

```csharp
public void AddArc (SKRect oval, float startAngle, float sweepAngle);
public void AddRect (SKRect rect, SKPathDirection direction, uint startIndex);
public void RConicTo (float dx0, float dy0, float dx1, float dy1, float w);
public void RCubicTo (float dx0, float dy0, float dx1, float dy1, float dx2, float dy2);
public void RLineTo (float dx, float dy);
public void RMoveTo (float dx, float dy);
public void RQuadTo (float dx0, float dy0, float dx1, float dy1);
```


#### New Type: SkiaSharp.SKFontMetrics

```csharp
public struct SKFontMetrics {
	// properties
	public float Ascent { get; }
	public float AverageCharacterWidth { get; }
	public float Bottom { get; }
	public float CapHeight { get; }
	public float Descent { get; }
	public float Leading { get; }
	public float MaxCharacterWidth { get; }
	public float Top { get; }
	public float? UnderlinePosition { get; }
	public float? UnderlineThickness { get; }
	public float XHeight { get; }
	public float XMax { get; }
	public float XMin { get; }
}
```

#### New Type: SkiaSharp.SKPathFillType

```csharp
[Serializable]
public enum SKPathFillType {
	EvenOdd = 1,
	InverseEvenOdd = 3,
	InverseWinding = 2,
	Winding = 0,
}
```


