# API diff: SkiaSharp.dll

## SkiaSharp.dll

### Namespace SkiaSharp

#### Type Changed: SkiaSharp.GRContext

Obsoleted methods:

```diff
 [Obsolete ("Use GetResourceCacheLimit() instead.")]
 public void GetResourceCacheLimits (out int maxResources, out long maxResourceBytes);
 [Obsolete ("Use SetResourceCacheLimit(long) instead.")]
 public void SetResourceCacheLimits (int maxResources, long maxResourceBytes);
```

Added methods:

```csharp
public long GetResourceCacheLimit ();
public void SetResourceCacheLimit (long maxResourceBytes);
```


#### Type Changed: SkiaSharp.SKColorSpacePrimaries

Removed methods:

```csharp
public SKMatrix44 ToMatrix44 ();
public bool ToMatrix44 (out SKMatrix44 toXyzD50);
```


#### Type Changed: SkiaSharp.SKColorSpaceXyz

Removed method:

```csharp
public SKMatrix44 ToMatrix44 ();
```


#### Type Changed: SkiaSharp.SKImageFilter

Obsoleted methods:

```diff
 [Obsolete ("Use CreateDisplacementMapEffect(SKColorChannel, SKColorChannel, float, SKImageFilter, SKImageFilter, SKImageFilter.CropRect) instead.")]
 public static SKImageFilter CreateDisplacementMapEffect (SKDisplacementMapEffectChannelSelectorType xChannelSelector, SKDisplacementMapEffectChannelSelectorType yChannelSelector, float scale, SKImageFilter displacement, SKImageFilter input, SKImageFilter.CropRect cropRect);
 [Obsolete ("Use CreateDropShadow or CreateDropShadowOnly instead.")]
 public static SKImageFilter CreateDropShadow (float dx, float dy, float sigmaX, float sigmaY, SKColor color, SKDropShadowImageFilterShadowMode shadowMode, SKImageFilter input, SKImageFilter.CropRect cropRect);
 [Obsolete ("Use CreateMatrixConvolution(SKSizeI, float[], float, float, SKPointI, SKShaderTileMode, bool, SKImageFilter, SKImageFilter.CropRect) instead.")]
 public static SKImageFilter CreateMatrixConvolution (SKSizeI kernelSize, float[] kernel, float gain, float bias, SKPointI kernelOffset, SKMatrixConvolutionTileMode tileMode, bool convolveAlpha, SKImageFilter input, SKImageFilter.CropRect cropRect);
```

Added methods:

```csharp
public static SKImageFilter CreateBlur (float sigmaX, float sigmaY, SKShaderTileMode tileMode, SKImageFilter input, SKImageFilter.CropRect cropRect);
public static SKImageFilter CreateDisplacementMapEffect (SKColorChannel xChannelSelector, SKColorChannel yChannelSelector, float scale, SKImageFilter displacement, SKImageFilter input, SKImageFilter.CropRect cropRect);
public static SKImageFilter CreateDropShadow (float dx, float dy, float sigmaX, float sigmaY, SKColor color, SKImageFilter input, SKImageFilter.CropRect cropRect);
public static SKImageFilter CreateDropShadowOnly (float dx, float dy, float sigmaX, float sigmaY, SKColor color, SKImageFilter input, SKImageFilter.CropRect cropRect);
public static SKImageFilter CreateMatrixConvolution (SKSizeI kernelSize, float[] kernel, float gain, float bias, SKPointI kernelOffset, SKShaderTileMode tileMode, bool convolveAlpha, SKImageFilter input, SKImageFilter.CropRect cropRect);
```


#### Type Changed: SkiaSharp.SKNativeObject

Added method:

```csharp
protected virtual void DisposeUnownedManaged ();
```


#### Type Changed: SkiaSharp.SKObject

Added method:

```csharp
protected override void DisposeUnownedManaged ();
```


#### Type Changed: SkiaSharp.SKSurface

Added method:

```csharp
public SKImage Snapshot (SKRectI bounds);
```


#### Type Changed: SkiaSharp.SkiaExtensions

Added methods:

```csharp

[Obsolete ("Use SKColorChannel instead.")]
public static SKColorChannel ToColorChannel (this SKDisplacementMapEffectChannelSelectorType channelSelectorType);

[Obsolete ("Use SKShaderTileMode instead.")]
public static SKShaderTileMode ToShaderTileMode (this SKMatrixConvolutionTileMode tileMode);
```


#### New Type: SkiaSharp.SKColorChannel

```csharp
[Serializable]
public enum SKColorChannel {
	A = 3,
	B = 2,
	G = 1,
	R = 0,
}
```

#### New Type: SkiaSharp.SkiaSharpVersion

```csharp
public static class SkiaSharpVersion {
	// properties
	public static System.Version Native { get; }
	public static System.Version NativeMinimum { get; }
	// methods
	public static bool CheckNativeLibraryCompatible (bool throwIfIncompatible);
}
```


