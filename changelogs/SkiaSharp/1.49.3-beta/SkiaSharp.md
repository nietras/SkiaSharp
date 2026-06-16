# API diff: SkiaSharp.dll

## SkiaSharp.dll

### Namespace SkiaSharp

#### Type Changed: SkiaSharp.SKCanvas

Removed methods:

```csharp
public void ClipPath (SKPath path);
public void ClipRect (SKRect rect);
```

Added methods:

```csharp
public void ClipPath (SKPath path, SKRegionOperation operation, bool antialias);
public void ClipRect (SKRect rect, SKRegionOperation operation, bool antialias);
public bool GetClipBounds (ref SKRect bounds);
public bool GetClipDeviceBounds (ref SKRectI bounds);
```


#### Type Changed: SkiaSharp.SKSurfaceProps

Added field:

```csharp
public SKPixelGeometry PixelGeometry;
```

Removed property:

```csharp
public SKPixelGeometry PixelGeometry { get; set; }
```


#### New Type: SkiaSharp.SKRegionOperation

```csharp
[Serializable]
public enum SKRegionOperation {
	Difference = 0,
	Intersect = 1,
	Replace = 5,
	ReverseDifference = 4,
	Union = 2,
	XOR = 3,
}
```


