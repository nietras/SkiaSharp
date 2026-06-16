# API diff: SkiaSharp.Views.Maui.Core.dll

## SkiaSharp.Views.Maui.Core.dll

### Namespace SkiaSharp.Views.Maui

#### Type Changed: SkiaSharp.Views.Maui.Extensions

Removed methods:

```csharp
public static Microsoft.Maui.Graphics.Rectangle ToMauiRectangle (this SkiaSharp.SKRect rect);
public static Microsoft.Maui.Graphics.Rectangle ToMauiRectangle (this SkiaSharp.SKRectI rect);
public static Microsoft.Maui.Graphics.RectangleF ToMauiRectangleF (this SkiaSharp.SKRect rect);
public static Microsoft.Maui.Graphics.RectangleF ToMauiRectangleF (this SkiaSharp.SKRectI rect);
public static SkiaSharp.SKRect ToSKRect (this Microsoft.Maui.Graphics.Rectangle rect);
public static SkiaSharp.SKRect ToSKRect (this Microsoft.Maui.Graphics.RectangleF rect);
```

Added methods:

```csharp
public static Microsoft.Maui.Graphics.Rect ToMauiRectangle (this SkiaSharp.SKRect rect);
public static Microsoft.Maui.Graphics.Rect ToMauiRectangle (this SkiaSharp.SKRectI rect);
public static Microsoft.Maui.Graphics.RectF ToMauiRectangleF (this SkiaSharp.SKRect rect);
public static Microsoft.Maui.Graphics.RectF ToMauiRectangleF (this SkiaSharp.SKRectI rect);
public static SkiaSharp.SKRect ToSKRect (this Microsoft.Maui.Graphics.Rect rect);
public static SkiaSharp.SKRect ToSKRect (this Microsoft.Maui.Graphics.RectF rect);
```



### Namespace SkiaSharp.Views.Maui.Handlers

#### Type Changed: SkiaSharp.Views.Maui.Handlers.SKCanvasViewHandler

Removed method:

```csharp
protected override object CreateNativeView ();
```

Added method:

```csharp
protected override object CreatePlatformView ();
```



