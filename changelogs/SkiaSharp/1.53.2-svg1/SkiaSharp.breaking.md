# API diff: SkiaSharp.dll

## SkiaSharp.dll

### Namespace SkiaSharp

#### Type Changed: SkiaSharp.SKCanvas

Removed method:

```csharp
public void Flush ();
```


#### Type Changed: SkiaSharp.SKRect

Removed properties:

```csharp
public float Height { get; }
public float Width { get; }
```


#### Type Changed: SkiaSharp.SKRectI

Removed properties:

```csharp
public float Height { get; }
public float Width { get; }
```


#### Type Changed: SkiaSharp.SKSurface

Removed methods:

```csharp
public static SKSurface Create (GRContext context, GRBackendRenderTargetDesc desc);
public static SKSurface Create (GRContext context, GRBackendTextureDesc desc);
public static SKSurface Create (GRContext context, GRBackendRenderTargetDesc desc, SKSurfaceProps props);
public static SKSurface Create (GRContext context, GRBackendTextureDesc desc, SKSurfaceProps props);
public static SKSurface Create (GRContext context, bool budgeted, SKImageInfo info);
public static SKSurface Create (GRContext context, bool budgeted, SKImageInfo info, int sampleCount);
public static SKSurface Create (GRContext context, bool budgeted, SKImageInfo info, int sampleCount, SKSurfaceProps props);
public static SKSurface CreateAsRenderTarget (GRContext context, GRBackendTextureDesc desc);
public static SKSurface CreateAsRenderTarget (GRContext context, GRBackendTextureDesc desc, SKSurfaceProps props);
```


#### Type Changed: SkiaSharp.SKSurfaceProps

Removed field:

```csharp
public SKSurfacePropsFlags Flags;
```


#### Removed Type SkiaSharp.GRBackend
#### Removed Type SkiaSharp.GRBackendRenderTargetDesc
#### Removed Type SkiaSharp.GRBackendTextureDesc
#### Removed Type SkiaSharp.GRBackendTextureDescFlags
#### Removed Type SkiaSharp.GRContext
#### Removed Type SkiaSharp.GRContextOptions
#### Removed Type SkiaSharp.GRGlGetProcDelegate
#### Removed Type SkiaSharp.GRGlInterface
#### Removed Type SkiaSharp.GRPixelConfig
#### Removed Type SkiaSharp.GRSurfaceOrigin
#### Removed Type SkiaSharp.SKSurfacePropsFlags

