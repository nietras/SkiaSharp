# API diff: SkiaSharp.Skottie.dll

## SkiaSharp.Skottie.dll

> Assembly Version Changed: 2.88.0.0 vs 0.0.0.0

### New Namespace SkiaSharp.Skottie

#### New Type: SkiaSharp.Skottie.Animation

```csharp
public class Animation : SkiaSharp.SKObject, SkiaSharp.ISKNonVirtualReferenceCounted, SkiaSharp.ISKReferenceCounted, SkiaSharp.ISKSkipObjectRegistration {
	// properties
	public double Duration { get; }
	public double Fps { get; }
	public double InPoint { get; }
	public double OutPoint { get; }
	public SkiaSharp.SKSize Size { get; }
	public string Version { get; }
	// methods
	protected override void DisposeNative ();
	public void Render (SkiaSharp.SKCanvas canvas, SkiaSharp.SKRect dst);
	public void Render (SkiaSharp.SKCanvas canvas, SkiaSharp.SKRect dst, AnimationRenderFlags flags);
	public void Seek (double t, SkiaSharp.SceneGraph.InvalidationController ic);
	public void SeekFrame (double t, SkiaSharp.SceneGraph.InvalidationController ic);
	public void SeekFrameTime (double t, SkiaSharp.SceneGraph.InvalidationController ic);
	public static bool TryCreate (SkiaSharp.SKStream stream, out Animation animation);
	public static bool TryCreate (System.IO.Stream stream, out Animation animation);
	public static bool TryCreate (string path, out Animation animation);
	public static bool TryParse (string data, out Animation animation);
}
```

#### New Type: SkiaSharp.Skottie.AnimationRenderFlags

```csharp
[Serializable]
[Flags]
public enum AnimationRenderFlags {
	DisableTopLevelClipping = 2,
	SkipTopLevelIsolation = 1,
}
```

