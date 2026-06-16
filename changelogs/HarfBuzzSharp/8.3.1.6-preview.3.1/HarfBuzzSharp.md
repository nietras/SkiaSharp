# API diff: HarfBuzzSharp.dll

## HarfBuzzSharp.dll

### Namespace HarfBuzzSharp

#### Type Changed: HarfBuzzSharp.Face

Removed methods:

```csharp
public uint[] GetPaletteColors (int paletteIndex);
public int GetPaletteColors (int paletteIndex, System.Span<uint> colors);
```

Added methods:

```csharp
public HBColor[] GetPaletteColors (int paletteIndex);
public int GetPaletteColors (int paletteIndex, System.Span<HBColor> colors);
```


#### New Type: HarfBuzzSharp.HBColor

```csharp
public struct HBColor, System.IEquatable<HBColor> {
	// constructors
	public HBColor (uint value);
	public HBColor (byte red, byte green, byte blue, byte alpha);
	// properties
	public byte Alpha { get; }
	public byte Blue { get; }
	public byte Green { get; }
	public byte Red { get; }
	public uint Value { get; }
	// methods
	public virtual bool Equals (HBColor other);
	public override bool Equals (object obj);
	public override int GetHashCode ();
	public override string ToString ();
	public static bool op_Equality (HBColor left, HBColor right);
	public static HBColor op_Explicit (uint value);
	public static uint op_Implicit (HBColor color);
	public static bool op_Inequality (HBColor left, HBColor right);
}
```


