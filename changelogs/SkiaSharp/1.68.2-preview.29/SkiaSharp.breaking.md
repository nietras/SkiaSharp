# API diff: SkiaSharp.dll

## SkiaSharp.dll

### Namespace SkiaSharp

#### Type Changed: SkiaSharp.SKCanvas

Removed methods:

```csharp
public void DrawAtlas (SKImage atlas, SKRect[] sprites, SKRotationScaleMatrix[] transforms, SKBlendMode mode, SKPaint paint);
public void DrawAtlas (SKImage atlas, SKRect[] sprites, SKRotationScaleMatrix[] transforms, SKRect cullRect, SKPaint paint);
public void DrawAtlas (SKImage atlas, SKRect[] sprites, SKRotationScaleMatrix[] transforms, SKBlendMode mode, SKRect cullRect, SKPaint paint);
public void DrawPatch (SKPoint[] cubics, SKColor[] colors, SKPaint paint);
public void DrawPatch (SKPoint[] cubics, SKPoint[] texCoords, SKPaint paint);
public void DrawPatch (SKPoint[] cubics, SKColor[] colors, SKBlendMode mode, SKPaint paint);
public void DrawPatch (SKPoint[] cubics, SKPoint[] texCoords, SKBlendMode mode, SKPaint paint);
```


#### Type Changed: SkiaSharp.SKColor

Modified methods:

```diff
-public override bool Equals (object other)
+public override bool Equals (object obj)
```


#### Type Changed: SkiaSharp.SKPMColor

Modified methods:

```diff
-public override bool Equals (object other)
+public override bool Equals (object obj)
```


#### Type Changed: SkiaSharp.SKRotationScaleMatrix

Removed method:

```csharp
public static SKRotationScaleMatrix CreateTranslate (float x, float y);
```


#### Type Changed: SkiaSharp.SKSize

Modified methods:

```diff
-public bool op_Equality (SKSize sz1, SKSize sz2---right---)
+public bool op_Equality (SKSize left, SKSize +++sz2+++right)
-public bool op_Inequality (SKSize sz1, SKSize sz2---right---)
+public bool op_Inequality (SKSize left, SKSize +++sz2+++right)
```


#### Type Changed: SkiaSharp.SKSizeI

Modified methods:

```diff
-public bool op_Equality (SKSizeI sz1, SKSizeI sz2---right---)
+public bool op_Equality (SKSizeI left, SKSizeI +++sz2+++right)
-public bool op_Inequality (SKSizeI sz1, SKSizeI sz2---right---)
+public bool op_Inequality (SKSizeI left, SKSizeI +++sz2+++right)
```



