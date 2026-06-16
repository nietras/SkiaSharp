# API diff: SkiaSharp.dll

## SkiaSharp.dll

### Namespace SkiaSharp

#### Type Changed: SkiaSharp.SKCanvas

Removed constructor:

```csharp
public SKCanvas (SKBitmap bitmap);
```

Added method:

```csharp
public void Flush ();
```


#### Type Changed: SkiaSharp.SKColor

Removed methods:

```csharp
public static uint op_Explicit (SKColor color);
public static SKColor op_Implicit (uint color);
```


#### Type Changed: SkiaSharp.SKPaint

Removed properties:

```csharp
public bool DeviceKerningEnabled { get; set; }
public bool FakeBoldText { get; set; }
public SKPaintHinting HintingLevel { get; set; }
public bool IsAutohinted { get; set; }
public bool IsEmbeddedBitmapText { get; set; }
public bool IsLinearText { get; set; }
public bool LcdRenderText { get; set; }
public bool StrikeThruText { get; set; }
public bool SubpixelText { get; set; }
public bool UnderlineText { get; set; }
```


#### Type Changed: SkiaSharp.SKPath

Removed properties:

```csharp
public SKPoint Item { get; }
public int PointCount { get; }
public SKPoint[] Points { get; }
```

Removed methods:

```csharp
public SKPoint GetPoint (int index);
public SKPoint[] GetPoints (int max);
public int GetPoints (SKPoint[] points, int max);
```


#### Type Changed: SkiaSharp.SKRect

Added properties:

```csharp
public float Height { get; }
public float Width { get; }
```


#### Type Changed: SkiaSharp.SKRectI

Added properties:

```csharp
public float Height { get; }
public float Width { get; }
```


#### Type Changed: SkiaSharp.SKSurface

Added methods:

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

Added field:

```csharp
public SKSurfacePropsFlags Flags;
```


#### Removed Type SkiaSharp.SKPaintHinting
#### New Type: SkiaSharp.GRBackend

```csharp
[Serializable]
public enum GRBackend {
	OpenGL = 0,
	Vulkan = 1,
}
```

#### New Type: SkiaSharp.GRBackendRenderTargetDesc

```csharp
public struct GRBackendRenderTargetDesc {
	// fields
	public GRPixelConfig Config;
	public int Height;
	public GRSurfaceOrigin Origin;
	public IntPtr RenderTargetHandle;
	public int SampleCount;
	public int StencilBits;
	public int Width;
}
```

#### New Type: SkiaSharp.GRBackendTextureDesc

```csharp
public struct GRBackendTextureDesc {
	// fields
	public GRPixelConfig Config;
	public GRBackendTextureDescFlags Flags;
	public int Height;
	public GRSurfaceOrigin Origin;
	public int SampleCount;
	public IntPtr TextureHandle;
	public int Width;
}
```

#### New Type: SkiaSharp.GRBackendTextureDescFlags

```csharp
[Serializable]
[Flags]
public enum GRBackendTextureDescFlags {
	None = 0,
	RenderTarget = 1,
}
```

#### New Type: SkiaSharp.GRContext

```csharp
public class GRContext : SkiaSharp.SKObject, System.IDisposable {
	// methods
	public void AbandonContext (bool releaseResources);
	public static GRContext Create (GRBackend backend);
	public static GRContext Create (GRBackend backend, GRGlInterface backendContext);
	public static GRContext Create (GRBackend backend, IntPtr backendContext);
	public static GRContext Create (GRBackend backend, GRGlInterface backendContext, GRContextOptions options);
	public static GRContext Create (GRBackend backend, IntPtr backendContext, GRContextOptions options);
	protected override void Dispose (bool disposing);
	public int GetRecommendedSampleCount (GRPixelConfig config, float dpi);
	public void GetResourceCacheLimits (out int maxResources, out long maxResourceBytes);
	public void GetResourceCacheUsage (out int maxResources, out long maxResourceBytes);
	public void SetResourceCacheLimits (int maxResources, long maxResourceBytes);
}
```

#### New Type: SkiaSharp.GRContextOptions

```csharp
public struct GRContextOptions {
	// fields
	public int BufferMapThreshold;
	public bool ClipBatchToBounds;
	public bool DoManualMipmapping;
	public bool DrawBatchBounds;
	public bool ImmediateMode;
	public int MaxBatchLookahead;
	public int MaxBatchLookback;
	public int MaxTextureSizeOverride;
	public int MaxTileSizeOverride;
	public bool SuppressDualSourceBlending;
	public bool SuppressPrints;
	public bool UseDrawInsteadOfPartialRenderTargetWrite;
	public bool UseShaderSwizzling;
}
```

#### New Type: SkiaSharp.GRGlInterface

```csharp
public class GRGlInterface : SkiaSharp.SKObject, System.IDisposable {
	// methods
	public GRGlInterface Clone ();
	public static GRGlInterface CreateDefaultInterface ();
	public static GRGlInterface CreateNativeInterface ();
	protected override void Dispose (bool disposing);
	public bool HasExtension (string extension);
	public bool Validate ();
}
```

#### New Type: SkiaSharp.GRPixelConfig

```csharp
[Serializable]
public enum GRPixelConfig {
	Alpha8 = 1,
	AlphaHalf = 14,
	Astc12x12 = 12,
	Bgra8888 = 6,
	Etc1 = 9,
	Index8 = 2,
	Latc = 10,
	R11Eac = 11,
	Rgb565 = 3,
	Rgba4444 = 4,
	Rgba8888 = 5,
	RgbaFloat = 13,
	RgbaHalf = 15,
	Sbgra8888 = 8,
	Srgba8888 = 7,
	Unknown = 0,
}
```

#### New Type: SkiaSharp.GRSurfaceOrigin

```csharp
[Serializable]
public enum GRSurfaceOrigin {
	BottomLeft = 1,
	TopLeft = 0,
}
```

#### New Type: SkiaSharp.SKSurfacePropsFlags

```csharp
[Serializable]
[Flags]
public enum SKSurfacePropsFlags {
	DisallowAntiAlias = 1,
	DisallowDither = 2,
	GammaCorrect = 8,
	UseDeviceIndependentFonts = 4,
}
```


