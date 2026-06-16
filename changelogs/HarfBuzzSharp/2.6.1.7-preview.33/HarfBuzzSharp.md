# API diff: HarfBuzzSharp.dll

## HarfBuzzSharp.dll

### Namespace HarfBuzzSharp

#### Type Changed: HarfBuzzSharp.Feature

Removed interface:

```csharp
System.IEquatable<Feature>
```

Removed methods:

```csharp
public virtual bool Equals (Feature obj);
public override bool Equals (object obj);
public override int GetHashCode ();
public static bool op_Equality (Feature left, Feature right);
public static bool op_Inequality (Feature left, Feature right);
```


#### Type Changed: HarfBuzzSharp.FontExtents

Removed interface:

```csharp
System.IEquatable<FontExtents>
```

Removed methods:

```csharp
public virtual bool Equals (FontExtents obj);
public override bool Equals (object obj);
public override int GetHashCode ();
public static bool op_Equality (FontExtents left, FontExtents right);
public static bool op_Inequality (FontExtents left, FontExtents right);
```


#### Type Changed: HarfBuzzSharp.GlyphExtents

Removed interface:

```csharp
System.IEquatable<GlyphExtents>
```

Removed methods:

```csharp
public virtual bool Equals (GlyphExtents obj);
public override bool Equals (object obj);
public override int GetHashCode ();
public static bool op_Equality (GlyphExtents left, GlyphExtents right);
public static bool op_Inequality (GlyphExtents left, GlyphExtents right);
```


#### Type Changed: HarfBuzzSharp.GlyphInfo

Removed interface:

```csharp
System.IEquatable<GlyphInfo>
```

Removed methods:

```csharp
public virtual bool Equals (GlyphInfo obj);
public override bool Equals (object obj);
public override int GetHashCode ();
public static bool op_Equality (GlyphInfo left, GlyphInfo right);
public static bool op_Inequality (GlyphInfo left, GlyphInfo right);
```


#### Type Changed: HarfBuzzSharp.GlyphPosition

Removed interface:

```csharp
System.IEquatable<GlyphPosition>
```

Removed methods:

```csharp
public virtual bool Equals (GlyphPosition obj);
public override bool Equals (object obj);
public override int GetHashCode ();
public static bool op_Equality (GlyphPosition left, GlyphPosition right);
public static bool op_Inequality (GlyphPosition left, GlyphPosition right);
```


#### Type Changed: HarfBuzzSharp.OpenTypeMetrics

Modified base type:

```diff
-System.Object
+System.ValueType
```

Removed constructor:

```csharp
public OpenTypeMetrics (Font font);
```

Added constructor:

```csharp
public OpenTypeMetrics (IntPtr font);
```


#### Removed Type HarfBuzzSharp.BufferDiffFlags
#### Removed Type HarfBuzzSharp.OpenTypeColorLayer
#### Removed Type HarfBuzzSharp.OpenTypeColorPaletteFlags
#### Removed Type HarfBuzzSharp.OpenTypeLayoutBaselineTag
#### Removed Type HarfBuzzSharp.OpenTypeLayoutGlyphClass
#### Removed Type HarfBuzzSharp.OpenTypeMathConstant
#### Removed Type HarfBuzzSharp.OpenTypeMathGlyphPart
#### Removed Type HarfBuzzSharp.OpenTypeMathGlyphPartFlags
#### Removed Type HarfBuzzSharp.OpenTypeMathGlyphVariant
#### Removed Type HarfBuzzSharp.OpenTypeMathKern
#### Removed Type HarfBuzzSharp.OpenTypeMetaTag
#### Removed Type HarfBuzzSharp.OpenTypeNameEntry
#### Removed Type HarfBuzzSharp.OpenTypeNameId
#### Removed Type HarfBuzzSharp.OpenTypeVarAxis
#### Removed Type HarfBuzzSharp.OpenTypeVarAxisFlags
#### Removed Type HarfBuzzSharp.OpenTypeVarAxisInfo
#### Removed Type HarfBuzzSharp.Variation

