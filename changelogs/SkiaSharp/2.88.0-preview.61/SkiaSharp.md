# API diff: SkiaSharp.dll

## SkiaSharp.dll

> Assembly Version Changed: 2.88.0.0 vs 2.80.0.0

### Namespace SkiaSharp

#### Type Changed: SkiaSharp.GRBackend

Added value:

```csharp
Direct3D = 4,
```


#### Type Changed: SkiaSharp.GRContext

Added method:

```csharp
protected override void DisposeNative ();
```


#### Type Changed: SkiaSharp.GRVkImageInfo

Added properties:

```csharp
public uint ImageUsageFlags { get; set; }
public uint SampleCount { get; set; }
public uint SharingMode { get; set; }
```


#### Type Changed: SkiaSharp.SKBitmap

Obsoleted properties:

```diff
 [Obsolete ()]
 public bool IsVolatile { get; set; }
```


#### Type Changed: SkiaSharp.SKColorSpaceXyz

Obsoleted properties:

```diff
 [Obsolete ("Use DisplayP3 instead.")]
 public static SKColorSpaceXyz Dcip3 { get; }
```

Added property:

```csharp
public static SKColorSpaceXyz DisplayP3 { get; }
```


#### Type Changed: SkiaSharp.SKColorType

Added values:

```csharp
Bgr101010x = 20,
Bgra1010102 = 19,
```


#### Type Changed: SkiaSharp.SKImage

Added method:

```csharp
public SKImage ApplyImageFilter (GRContext context, SKImageFilter filter, SKRectI subset, SKRectI clipBounds, out SKRectI outSubset, out SKPointI outOffset);
```


#### Type Changed: SkiaSharp.SKSurface

Obsoleted methods:

```diff
 [Obsolete ("Use Create(GRContext, GRBackendTexture, SKColorType) instead.")]
 public static SKSurface CreateAsRenderTarget (GRContext context, GRBackendTexture texture, SKColorType colorType);
 [Obsolete ("Use Create(GRContext, GRBackendTexture, GRSurfaceOrigin, SKColorType) instead.")]
 public static SKSurface CreateAsRenderTarget (GRContext context, GRBackendTexture texture, GRSurfaceOrigin origin, SKColorType colorType);
 [Obsolete ("Use Create(GRContext, GRBackendTexture, SKColorType, SKSurfaceProperties) instead.")]
 public static SKSurface CreateAsRenderTarget (GRContext context, GRBackendTexture texture, SKColorType colorType, SKSurfaceProperties props);
 [Obsolete ("Use Create(GRContext, GRBackendTexture, GRSurfaceOrigin, SKColorType, SKSurfaceProperties) instead.")]
 public static SKSurface CreateAsRenderTarget (GRContext context, GRBackendTexture texture, GRSurfaceOrigin origin, SKColorType colorType, SKSurfaceProperties props);
 [Obsolete ("Use Create(GRContext, GRBackendTexture, GRSurfaceOrigin, int, SKColorType) instead.")]
 public static SKSurface CreateAsRenderTarget (GRContext context, GRBackendTexture texture, GRSurfaceOrigin origin, int sampleCount, SKColorType colorType);
 [Obsolete ("Use Create(GRContext, GRBackendTexture, GRSurfaceOrigin, int, SKColorType, SKColorSpace) instead.")]
 public static SKSurface CreateAsRenderTarget (GRContext context, GRBackendTexture texture, GRSurfaceOrigin origin, int sampleCount, SKColorType colorType, SKColorSpace colorspace);
 [Obsolete ("Use Create(GRContext, GRBackendTexture, GRSurfaceOrigin, int, SKColorType, SKSurfaceProperties) instead.")]
 public static SKSurface CreateAsRenderTarget (GRContext context, GRBackendTexture texture, GRSurfaceOrigin origin, int sampleCount, SKColorType colorType, SKSurfaceProperties props);
 [Obsolete ("Use Create(GRContext, GRBackendTexture, GRSurfaceOrigin, int, SKColorType, SKColorSpace, SKSurfaceProperties) instead.")]
 public static SKSurface CreateAsRenderTarget (GRContext context, GRBackendTexture texture, GRSurfaceOrigin origin, int sampleCount, SKColorType colorType, SKColorSpace colorspace, SKSurfaceProperties props);
```


#### New Type: SkiaSharp.SKRuntimeEffect

```csharp
public class SKRuntimeEffect : SkiaSharp.SKObject, System.IDisposable {
	// properties
	public System.Collections.Generic.IReadOnlyList<string> Children { get; }
	public int UniformSize { get; }
	public System.Collections.Generic.IReadOnlyList<string> Uniforms { get; }
	// methods
	public static SKRuntimeEffect Create (string sksl, out string errors);
	public SKColorFilter ToColorFilter ();
	public SKColorFilter ToColorFilter (SKRuntimeEffectUniforms uniforms);
	public SKColorFilter ToColorFilter (SKRuntimeEffectUniforms uniforms, SKRuntimeEffectChildren children);
	public SKShader ToShader (bool isOpaque);
	public SKShader ToShader (bool isOpaque, SKRuntimeEffectUniforms uniforms);
	public SKShader ToShader (bool isOpaque, SKRuntimeEffectUniforms uniforms, SKRuntimeEffectChildren children);
	public SKShader ToShader (bool isOpaque, SKRuntimeEffectUniforms uniforms, SKRuntimeEffectChildren children, SKMatrix localMatrix);
}
```

#### New Type: SkiaSharp.SKRuntimeEffectChildren

```csharp
public class SKRuntimeEffectChildren : System.Collections.Generic.IEnumerable<string>, System.Collections.IEnumerable {
	// constructors
	public SKRuntimeEffectChildren (SKRuntimeEffect effect);
	// properties
	public int Count { get; }
	public SKShader Item { set; }
	public System.Collections.Generic.IReadOnlyList<string> Names { get; }
	// methods
	public void Add (string name, SKShader value);
	public bool Contains (string name);
	public virtual System.Collections.Generic.IEnumerator<string> GetEnumerator ();
	public void Reset ();
	public SKShader[] ToArray ();
}
```

#### New Type: SkiaSharp.SKRuntimeEffectUniform

```csharp
public struct SKRuntimeEffectUniform {
	// properties
	public static SKRuntimeEffectUniform Empty { get; }
	public bool IsEmpty { get; }
	public int Size { get; }
	// methods
	public void WriteTo (System.Span<byte> data);
	public static SKRuntimeEffectUniform op_Implicit (SKMatrix value);
	public static SKRuntimeEffectUniform op_Implicit (System.ReadOnlySpan<float> value);
	public static SKRuntimeEffectUniform op_Implicit (float value);
	public static SKRuntimeEffectUniform op_Implicit (float[] value);
	public static SKRuntimeEffectUniform op_Implicit (float[][] value);
	public static SKRuntimeEffectUniform op_Implicit (System.Span<float> value);
}
```

#### New Type: SkiaSharp.SKRuntimeEffectUniforms

```csharp
public class SKRuntimeEffectUniforms : System.Collections.Generic.IEnumerable<string>, System.Collections.IEnumerable {
	// constructors
	public SKRuntimeEffectUniforms (SKRuntimeEffect effect);
	// properties
	public int Count { get; }
	public SKRuntimeEffectUniform Item { set; }
	public System.Collections.Generic.IReadOnlyList<string> Names { get; }
	// methods
	public void Add (string name, SKRuntimeEffectUniform value);
	public bool Contains (string name);
	public virtual System.Collections.Generic.IEnumerator<string> GetEnumerator ();
	public void Reset ();
	public SKData ToData ();
}
```


