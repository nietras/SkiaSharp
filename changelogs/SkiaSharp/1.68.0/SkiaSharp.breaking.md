# API diff: SkiaSharp.dll

## SkiaSharp.dll

### Namespace SkiaSharp

#### Type Changed: SkiaSharp.GRContext

Removed method:

```csharp
public int GetMaxSurfaceSampleCountForColorType (SKColorType colorType);
```


#### Type Changed: SkiaSharp.SKDocument

Modified methods:

```diff
 public SKDocument CreatePdf (string path, float dpi--- = 72---)
 public SKDocument CreateXps (SKWStream stream, float dpi--- = 72---)
 public SKDocument CreateXps (string path, float dpi--- = 72---)
```


#### Type Changed: SkiaSharp.SKPaint

Modified methods:

```diff
 public bool GetFillPath (SKPath src, SKPath dst, float resScale--- = 1---)
 public bool GetFillPath (SKPath src, SKPath dst, SKRect cullRect, float resScale--- = 1---)
```


#### Type Changed: SkiaSharp.SKSurface

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



