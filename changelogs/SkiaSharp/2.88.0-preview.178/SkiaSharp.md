# API diff: SkiaSharp.dll

## SkiaSharp.dll

### New Namespace SkiaSharp.Internals

#### New Type: SkiaSharp.Internals.IPlatformLock

```csharp
public interface IPlatformLock {
	// methods
	public virtual void EnterReadLock ();
	public virtual void EnterUpgradeableReadLock ();
	public virtual void EnterWriteLock ();
	public virtual void ExitReadLock ();
	public virtual void ExitUpgradeableReadLock ();
	public virtual void ExitWriteLock ();
}
```

#### New Type: SkiaSharp.Internals.PlatformLock

```csharp
public static class PlatformLock {
	// properties
	public static System.Func<IPlatformLock> Factory { get; set; }
	// methods
	public static IPlatformLock Create ();
	public static IPlatformLock DefaultFactory ();
}
```

