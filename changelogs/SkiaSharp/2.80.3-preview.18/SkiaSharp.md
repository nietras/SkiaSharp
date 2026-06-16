# API diff: SkiaSharp.dll

## SkiaSharp.dll

### Namespace SkiaSharp

#### Type Changed: SkiaSharp.GRGlInterface

Added method:

```csharp
public static GRGlInterface CreateAngle ();
```


#### Type Changed: SkiaSharp.SKPicture

Added methods:

```csharp
public static SKPicture Deserialize (SKData data);
public static SKPicture Deserialize (SKStream stream);
public static SKPicture Deserialize (System.IO.Stream stream);
public static SKPicture Deserialize (System.ReadOnlySpan<byte> data);
public static SKPicture Deserialize (IntPtr data, int length);
public SKData Serialize ();
public void Serialize (SKWStream stream);
public void Serialize (System.IO.Stream stream);
```



