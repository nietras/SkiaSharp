# API diff: SkiaSharp.dll

## SkiaSharp.dll

### Namespace SkiaSharp

#### Type Changed: SkiaSharp.GRContext

Modified base type:

```diff
-SkiaSharp.SKObject
+SkiaSharp.GRRecordingContext
```

Added methods:

```csharp
public void Flush (bool submit, bool synchronous);
public void Submit (bool synchronous);
```


#### Type Changed: SkiaSharp.SKCanvas

Added methods:

```csharp
public void Clear (SKColorF color);
public void DrawColor (SKColorF color, SKBlendMode mode);
```


#### Type Changed: SkiaSharp.SKImage

Added methods:

```csharp
public SKImage ApplyImageFilter (GRRecordingContext context, SKImageFilter filter, SKRectI subset, SKRectI clipBounds, out SKRectI outSubset, out SKPointI outOffset);
public static SKImage FromAdoptedTexture (GRRecordingContext context, GRBackendTexture texture, SKColorType colorType);
public static SKImage FromAdoptedTexture (GRRecordingContext context, GRBackendTexture texture, GRSurfaceOrigin origin, SKColorType colorType);
public static SKImage FromAdoptedTexture (GRRecordingContext context, GRBackendTexture texture, GRSurfaceOrigin origin, SKColorType colorType, SKAlphaType alpha);
public static SKImage FromAdoptedTexture (GRRecordingContext context, GRBackendTexture texture, GRSurfaceOrigin origin, SKColorType colorType, SKAlphaType alpha, SKColorSpace colorspace);
public static SKImage FromTexture (GRRecordingContext context, GRBackendTexture texture, SKColorType colorType);
public static SKImage FromTexture (GRRecordingContext context, GRBackendTexture texture, GRSurfaceOrigin origin, SKColorType colorType);
public static SKImage FromTexture (GRRecordingContext context, GRBackendTexture texture, GRSurfaceOrigin origin, SKColorType colorType, SKAlphaType alpha);
public static SKImage FromTexture (GRRecordingContext context, GRBackendTexture texture, GRSurfaceOrigin origin, SKColorType colorType, SKAlphaType alpha, SKColorSpace colorspace);
public static SKImage FromTexture (GRRecordingContext context, GRBackendTexture texture, GRSurfaceOrigin origin, SKColorType colorType, SKAlphaType alpha, SKColorSpace colorspace, SKImageTextureReleaseDelegate releaseProc);
public static SKImage FromTexture (GRRecordingContext context, GRBackendTexture texture, GRSurfaceOrigin origin, SKColorType colorType, SKAlphaType alpha, SKColorSpace colorspace, SKImageTextureReleaseDelegate releaseProc, object releaseContext);
public bool IsValid (GRRecordingContext context);
```


#### Type Changed: SkiaSharp.SKImageFilter

Added methods:

```csharp
public static SKImageFilter CreateDilate (float radiusX, float radiusY, SKImageFilter input, SKImageFilter.CropRect cropRect);
public static SKImageFilter CreateErode (float radiusX, float radiusY, SKImageFilter input, SKImageFilter.CropRect cropRect);
```


#### Type Changed: SkiaSharp.SKPixmap

Added method:

```csharp
public bool Erase (SKColorF color, SKColorSpace colorspace, SKRectI subset);
```


#### Type Changed: SkiaSharp.SKSurface

Added property:

```csharp
public GRRecordingContext Context { get; }
```

Added methods:

```csharp
public static SKSurface Create (GRRecordingContext context, GRBackendRenderTarget renderTarget, SKColorType colorType);
public static SKSurface Create (GRRecordingContext context, GRBackendTexture texture, SKColorType colorType);
public static SKSurface Create (GRRecordingContext context, bool budgeted, SKImageInfo info);
public static SKSurface Create (GRRecordingContext context, GRBackendRenderTarget renderTarget, GRSurfaceOrigin origin, SKColorType colorType);
public static SKSurface Create (GRRecordingContext context, GRBackendRenderTarget renderTarget, SKColorType colorType, SKSurfaceProperties props);
public static SKSurface Create (GRRecordingContext context, GRBackendTexture texture, GRSurfaceOrigin origin, SKColorType colorType);
public static SKSurface Create (GRRecordingContext context, GRBackendTexture texture, SKColorType colorType, SKSurfaceProperties props);
public static SKSurface Create (GRRecordingContext context, bool budgeted, SKImageInfo info, SKSurfaceProperties props);
public static SKSurface Create (GRRecordingContext context, bool budgeted, SKImageInfo info, int sampleCount);
public static SKSurface Create (GRRecordingContext context, GRBackendRenderTarget renderTarget, GRSurfaceOrigin origin, SKColorType colorType, SKColorSpace colorspace);
public static SKSurface Create (GRRecordingContext context, GRBackendRenderTarget renderTarget, GRSurfaceOrigin origin, SKColorType colorType, SKSurfaceProperties props);
public static SKSurface Create (GRRecordingContext context, GRBackendTexture texture, GRSurfaceOrigin origin, SKColorType colorType, SKSurfaceProperties props);
public static SKSurface Create (GRRecordingContext context, GRBackendTexture texture, GRSurfaceOrigin origin, int sampleCount, SKColorType colorType);
public static SKSurface Create (GRRecordingContext context, bool budgeted, SKImageInfo info, int sampleCount, GRSurfaceOrigin origin);
public static SKSurface Create (GRRecordingContext context, bool budgeted, SKImageInfo info, int sampleCount, SKSurfaceProperties props);
public static SKSurface Create (GRRecordingContext context, GRBackendRenderTarget renderTarget, GRSurfaceOrigin origin, SKColorType colorType, SKColorSpace colorspace, SKSurfaceProperties props);
public static SKSurface Create (GRRecordingContext context, GRBackendTexture texture, GRSurfaceOrigin origin, int sampleCount, SKColorType colorType, SKColorSpace colorspace);
public static SKSurface Create (GRRecordingContext context, GRBackendTexture texture, GRSurfaceOrigin origin, int sampleCount, SKColorType colorType, SKSurfaceProperties props);
public static SKSurface Create (GRRecordingContext context, GRBackendTexture texture, GRSurfaceOrigin origin, int sampleCount, SKColorType colorType, SKColorSpace colorspace, SKSurfaceProperties props);
public static SKSurface Create (GRRecordingContext context, bool budgeted, SKImageInfo info, int sampleCount, GRSurfaceOrigin origin, SKSurfaceProperties props, bool shouldCreateWithMips);
public void Flush (bool submit, bool synchronous);
```


#### New Type: SkiaSharp.GRRecordingContext

```csharp
public class GRRecordingContext : SkiaSharp.SKObject, System.IDisposable {
	// properties
	public GRBackend Backend { get; }
	// methods
	public int GetMaxSurfaceSampleCount (SKColorType colorType);
}
```


