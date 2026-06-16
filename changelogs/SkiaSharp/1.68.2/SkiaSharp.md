# API diff: SkiaSharp.dll

## SkiaSharp.dll

### Namespace SkiaSharp

#### Type Changed: SkiaSharp.SKPixmap

Added method:

```csharp
public System.Span<T> GetPixelSpan<T> ();
```


#### Type Changed: SkiaSharp.SKRotationScaleMatrix

Removed methods:

```csharp
public static SKRotationScaleMatrix FromDegrees (float scale, float degrees, float tx, float ty, float anchorX, float anchorY);
public static SKRotationScaleMatrix FromRadians (float scale, float radians, float tx, float ty, float anchorX, float anchorY);
```

Added methods:

```csharp
public static SKRotationScaleMatrix Create (float scale, float radians, float tx, float ty, float anchorX, float anchorY);
public static SKRotationScaleMatrix CreateDegrees (float scale, float degrees, float tx, float ty, float anchorX, float anchorY);
```



