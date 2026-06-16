# API diff: SkiaSharp.Vulkan.SharpVk.dll

## SkiaSharp.Vulkan.SharpVk.dll

### Namespace SkiaSharp

#### Removed Type SkiaSharp.GRVkExtensionsExtensions
#### New Type: SkiaSharp.GRVkExtensionsSharpVkExtensions

```csharp
public static class GRVkExtensionsSharpVkExtensions {
	// methods
	public static void Initialize (this GRVkExtensions extensions, GRSharpVkGetProcedureAddressDelegate getProc, SharpVk.Instance instance, SharpVk.PhysicalDevice physicalDevice);
	public static void Initialize (this GRVkExtensions extensions, GRSharpVkGetProcedureAddressDelegate getProc, SharpVk.Instance instance, SharpVk.PhysicalDevice physicalDevice, string[] instanceExtensions, string[] deviceExtensions);
}
```


