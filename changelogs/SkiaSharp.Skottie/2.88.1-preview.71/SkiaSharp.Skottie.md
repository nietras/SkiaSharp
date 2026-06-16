# API diff: SkiaSharp.Skottie.dll

## SkiaSharp.Skottie.dll

### Namespace SkiaSharp.Skottie

#### Type Changed: SkiaSharp.Skottie.Animation

Modified properties:

```diff
-public double Duration { get; }
+public System.TimeSpan Duration { get; }
```

Modified methods:

```diff
-public void Seek (double t, SkiaSharp.SceneGraph.InvalidationController ic = NULL)
+public void Seek (double percent, SkiaSharp.SceneGraph.InvalidationController ic = NULL)
-public void SeekFrame (double t, SkiaSharp.SceneGraph.InvalidationController ic = NULL)
+public void SeekFrame (double frame, SkiaSharp.SceneGraph.InvalidationController ic = NULL)
-public void SeekFrameTime (double t, SkiaSharp.SceneGraph.InvalidationController ic = NULL)
+public void SeekFrameTime (double seconds, SkiaSharp.SceneGraph.InvalidationController ic = NULL)
-public bool TryParse (string data, out Animation animation)
+public bool TryParse (string json, out Animation animation)
```

Added methods:

```csharp
public static Animation Create (SkiaSharp.SKStream stream);
public static Animation Create (System.IO.Stream stream);
public static Animation Create (string path);
public static Animation Parse (string json);
public void SeekFrameTime (System.TimeSpan time, SkiaSharp.SceneGraph.InvalidationController ic);
```



