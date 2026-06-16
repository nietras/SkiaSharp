# API diff: HarfBuzzSharp.dll

## HarfBuzzSharp.dll

### Namespace HarfBuzzSharp

#### Type Changed: HarfBuzzSharp.Blob

Added method:

```csharp
protected override void Dispose (bool disposing);
```


#### Type Changed: HarfBuzzSharp.Buffer

Added methods:

```csharp
public void Add (int codepoint, int cluster);
protected override void Dispose (bool disposing);
```


#### Type Changed: HarfBuzzSharp.Face

Added method:

```csharp
protected override void Dispose (bool disposing);
```


#### Type Changed: HarfBuzzSharp.Font

Added method:

```csharp
protected override void Dispose (bool disposing);
```


#### Type Changed: HarfBuzzSharp.FontFunctions

Added method:

```csharp
protected override void Dispose (bool disposing);
```


#### Type Changed: HarfBuzzSharp.Script

Added method:

```csharp
public static bool TryParse (string str, out Script script);
```


#### Type Changed: HarfBuzzSharp.UnicodeFunctions

Added methods:

```csharp
protected override void Dispose (bool disposing);
public UnicodeCombiningClass GetCombiningClass (int unicode);
public UnicodeGeneralCategory GetGeneralCategory (int unicode);
public int GetMirroring (int unicode);
public Script GetScript (int unicode);
public bool TryCompose (int a, int b, out int ab);
public bool TryDecompose (int ab, out int a, out int b);
```



