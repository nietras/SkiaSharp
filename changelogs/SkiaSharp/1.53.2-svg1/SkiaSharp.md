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


#### Type Changed: SkiaSharp.SKWStream

Modified properties:

```diff
 public ---virtual--- int BytesWritten { get; }
```

Modified methods:

```diff
 public ---virtual--- void Flush ()
 public ---virtual--- bool Write (byte[] buffer, int size)
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
#### New Type: SkiaSharp.SKManagedWStream

```csharp
public class SKManagedWStream : SkiaSharp.SKWStream, System.IDisposable {
	// constructors
	public SKManagedWStream (System.IO.Stream managedStream);
	public SKManagedWStream (System.IO.Stream managedStream, bool disposeManagedStream);
	// methods
	protected override void Dispose (bool disposing);
}
```

#### New Type: SkiaSharp.SKSvgCanvas

```csharp
public class SKSvgCanvas {
	// methods
	public static SKCanvas Create (SKRect bounds, SKXmlWriter writer);
}
```

#### New Type: SkiaSharp.SKXmlStreamWriter

```csharp
public class SKXmlStreamWriter : SkiaSharp.SKXmlWriter, System.IDisposable {
	// constructors
	public SKXmlStreamWriter (SKWStream stream);
	// methods
	protected override void Dispose (bool disposing);
}
```

#### New Type: SkiaSharp.SKXmlWriter

```csharp
public abstract class SKXmlWriter : SkiaSharp.SKObject, System.IDisposable {
}
```


