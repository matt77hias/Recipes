# Hierarchical Organization of Build Files

1. Add the c++ fixup targets to the VS project:

**Widget.vcxproj**:
```xml
<?xml version="1.0" encoding="utf-8"?>
<Project DefaultTargets="Build" xmlns="http://schemas.microsoft.com/developer/msbuild/2003">
  ...
  <Import Project="..\Targets\CppFixup.targets" />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.targets" />
  ...
</Project>
```
