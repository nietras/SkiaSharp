# API diff: HarfBuzzSharp.dll

## HarfBuzzSharp.dll

### Namespace HarfBuzzSharp

#### Type Changed: HarfBuzzSharp.Buffer

Added methods:

```csharp
public void AddCodepoints (System.ReadOnlySpan<int> text);
public void AddCodepoints (System.ReadOnlySpan<int> text, int itemOffset, int itemLength);
public void AddUtf32 (System.ReadOnlySpan<int> text);
public void AddUtf32 (System.ReadOnlySpan<int> text, int itemOffset, int itemLength);
```


#### Type Changed: HarfBuzzSharp.Font

Added property:

```csharp
public OpenTypeMetrics OpenTypeMetrics { get; }
```

Added methods:

```csharp
public bool TryGetGlyph (int unicode, out uint glyph);
public bool TryGetGlyph (int unicode, uint variationSelector, out uint glyph);
public bool TryGetNominalGlyph (int unicode, out uint glyph);
public bool TryGetVariationGlyph (int unicode, out uint glyph);
public bool TryGetVariationGlyph (int unicode, uint variationSelector, out uint glyph);
```


#### New Type: HarfBuzzSharp.OpenTypeMetrics

```csharp
public struct OpenTypeMetrics {
	// constructors
	public OpenTypeMetrics (IntPtr font);
	// methods
	public float GetVariation (OpenTypeMetricsTag metricsTag);
	public int GetXVariation (OpenTypeMetricsTag metricsTag);
	public int GetYVariation (OpenTypeMetricsTag metricsTag);
	public bool TryGetPosition (OpenTypeMetricsTag metricsTag, out int position);
}
```

#### New Type: HarfBuzzSharp.OpenTypeMetricsTag

```csharp
[Serializable]
public enum OpenTypeMetricsTag {
	CapHeight = 1668311156,
	HorizontalAscender = 1751216995,
	HorizontalCaretOffset = 1751347046,
	HorizontalCaretRise = 1751347827,
	HorizontalCaretRun = 1751347822,
	HorizontalClippingAscent = 1751346273,
	HorizontalClippingDescent = 1751346276,
	HorizontalDescender = 1751413603,
	HorizontalLineGap = 1751934832,
	StrikeoutOffset = 1937011311,
	StrikeoutSize = 1937011315,
	SubScriptEmXOffset = 1935833199,
	SubScriptEmXSize = 1935833203,
	SubScriptEmYOffset = 1935833455,
	SubScriptEmYSize = 1935833459,
	SuperScriptEmXOffset = 1936750703,
	SuperScriptEmXSize = 1936750707,
	SuperScriptEmYOffset = 1936750959,
	SuperScriptEmYSize = 1936750963,
	UnderlineOffset = 1970168943,
	UnderlineSize = 1970168947,
	VerticalAscender = 1986098019,
	VerticalCaretOffset = 1986228070,
	VerticalCaretRise = 1986228851,
	VerticalCaretRun = 1986228846,
	VerticalDescender = 1986294627,
	VerticalLineGap = 1986815856,
	XHeight = 2020108148,
}
```


