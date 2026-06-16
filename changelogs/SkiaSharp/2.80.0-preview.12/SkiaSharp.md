# API diff: SkiaSharp.dll

## SkiaSharp.dll

### Namespace SkiaSharp

#### Type Changed: SkiaSharp.SKPaint

Added property:

```csharp
public SKColorF ColorF { get; set; }
```

Added method:

```csharp
public void SetColor (SKColorF color, SKColorSpace colorspace);
```


#### Type Changed: SkiaSharp.SKPath

Added methods:

```csharp
public SKPath ToWinding ();
public bool ToWinding (SKPath result);
```



