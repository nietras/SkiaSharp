# API diff: SkiaSharp.dll

## SkiaSharp.dll

### Namespace SkiaSharp

#### Type Changed: SkiaSharp.SKCanvas

Added properties:

```csharp
public bool IsClipEmpty { get; }
public bool IsClipRect { get; }
```

Added methods:

```csharp
public void DrawArc (SKRect oval, float startAngle, float sweepAngle, bool useCenter, SKPaint paint);
public void DrawAtlas (SKImage atlas, SKRect[] sprites, SKRotationScaleMatrix[] transforms, SKPaint paint);
public void DrawAtlas (SKImage atlas, SKRect[] sprites, SKRotationScaleMatrix[] transforms, SKBlendMode mode, SKPaint paint);
public void DrawAtlas (SKImage atlas, SKRect[] sprites, SKRotationScaleMatrix[] transforms, SKRect cullRect, SKPaint paint);
public void DrawAtlas (SKImage atlas, SKRect[] sprites, SKRotationScaleMatrix[] transforms, SKBlendMode mode, SKRect cullRect, SKPaint paint);
public void DrawAtlas (SKImage atlas, SKRect[] sprites, SKRotationScaleMatrix[] transforms, SKColor[] colors, SKBlendMode mode, SKPaint paint);
public void DrawAtlas (SKImage atlas, SKRect[] sprites, SKRotationScaleMatrix[] transforms, SKColor[] colors, SKBlendMode mode, SKRect cullRect, SKPaint paint);
public void DrawPatch (SKPoint[] cubics, SKColor[] colors, SKPaint paint);
public void DrawPatch (SKPoint[] cubics, SKPoint[] texCoords, SKPaint paint);
public void DrawPatch (SKPoint[] cubics, SKColor[] colors, SKBlendMode mode, SKPaint paint);
public void DrawPatch (SKPoint[] cubics, SKColor[] colors, SKPoint[] texCoords, SKPaint paint);
public void DrawPatch (SKPoint[] cubics, SKPoint[] texCoords, SKBlendMode mode, SKPaint paint);
public void DrawPatch (SKPoint[] cubics, SKColor[] colors, SKPoint[] texCoords, SKBlendMode mode, SKPaint paint);
public void DrawRoundRectDifference (SKRoundRect outer, SKRoundRect inner, SKPaint paint);
```


#### Type Changed: SkiaSharp.SKImage

Added method:

```csharp
public SKShader ToShader ();
```


#### Type Changed: SkiaSharp.SKRoundRect

Added constructor:

```csharp
public SKRoundRect (SKRect rect, float radius);
```


#### Type Changed: SkiaSharp.SKShader

Added method:

```csharp
public static SKShader CreatePerlinNoiseImprovedNoise (float baseFrequencyX, float baseFrequencyY, int numOctaves, float z);
```


#### New Type: SkiaSharp.SKRotationScaleMatrix

```csharp
public struct SKRotationScaleMatrix {
	// constructors
	public SKRotationScaleMatrix (float scos, float ssin, float tx, float ty);
	// fields
	public static SKRotationScaleMatrix Empty;
	// properties
	public float SCos { get; set; }
	public float SSin { get; set; }
	public float TX { get; set; }
	public float TY { get; set; }
	// methods
	public static SKRotationScaleMatrix CreateIdentity ();
	public static SKRotationScaleMatrix CreateRotation (float radians, float anchorX, float anchorY);
	public static SKRotationScaleMatrix CreateRotationDegrees (float degrees, float anchorX, float anchorY);
	public static SKRotationScaleMatrix CreateScale (float s);
	public static SKRotationScaleMatrix CreateTranslate (float x, float y);
	public static SKRotationScaleMatrix FromDegrees (float scale, float degrees, float tx, float ty, float anchorX, float anchorY);
	public static SKRotationScaleMatrix FromRadians (float scale, float radians, float tx, float ty, float anchorX, float anchorY);
	public SKMatrix ToMatrix ();
}
```


