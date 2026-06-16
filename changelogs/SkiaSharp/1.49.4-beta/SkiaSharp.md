# API diff: SkiaSharp.dll

## SkiaSharp.dll

### Namespace SkiaSharp

#### Type Changed: SkiaSharp.SKFileStream

Added method:

```csharp
protected override void Dispose (bool disposing);
```


#### Type Changed: SkiaSharp.SKMemoryStream

Added method:

```csharp
protected override void Dispose (bool disposing);
```


#### Type Changed: SkiaSharp.SKObject

Added property:

```csharp
protected bool OwnsHandle { get; }
```


#### Type Changed: SkiaSharp.SKTypeface

Added property:

```csharp
public string FamilyName { get; }
```

Added methods:

```csharp
public byte[] GetTableData (uint tag);
public uint[] GetTableTags ();
public bool TryGetTableData (uint tag, out byte[] tableData);
```


#### New Type: SkiaSharp.SKDocument

```csharp
public class SKDocument : SkiaSharp.SKObject, System.IDisposable {
	// fields
	public static const float DefaultRasterDpi;
	// methods
	public void Abort ();
	public SKCanvas BeginPage (float width, float height);
	public SKCanvas BeginPage (float width, float height, SKRect content);
	public bool Close ();
	public static SKDocument CreatePdf (SKWStream stream, float dpi);
	public static SKDocument CreatePdf (string path, float dpi);
	protected override void Dispose (bool disposing);
	public void EndPage ();
}
```

#### New Type: SkiaSharp.SKDynamicMemoryWStream

```csharp
public class SKDynamicMemoryWStream : SkiaSharp.SKWStream, System.IDisposable {
	// constructors
	public SKDynamicMemoryWStream ();
	// methods
	public SKData CopyToData ();
	public SKStreamAsset DetachAsStream ();
	protected override void Dispose (bool disposing);
}
```

#### New Type: SkiaSharp.SKFileWStream

```csharp
public class SKFileWStream : SkiaSharp.SKWStream, System.IDisposable {
	// constructors
	public SKFileWStream (string path);
	// methods
	protected override void Dispose (bool disposing);
}
```

#### New Type: SkiaSharp.SKWStream

```csharp
public abstract class SKWStream : SkiaSharp.SKObject, System.IDisposable {
	// properties
	public int BytesWritten { get; }
	// methods
	public void Flush ();
	public static int GetSizeOfPackedUInt32 (uint value);
	public void NewLine ();
	public bool Write (byte[] buffer, int size);
	public bool Write16 (ushort value);
	public bool Write32 (uint value);
	public bool Write8 (byte value);
	public bool WriteBigDecimalAsText (long value, int digits);
	public bool WriteBool (bool value);
	public bool WriteDecimalAsTest (int value);
	public bool WriteHexAsText (uint value, int digits);
	public bool WritePackedUInt32 (uint value);
	public bool WriteScalar (float value);
	public bool WriteScalarAsText (float value);
	public bool WriteStream (SKStream input, int length);
	public bool WriteText (string value);
}
```


