# Centralized C++ Configuration

1. Add the c++ properties to each VS project with C++ code:

**Widget.vcxproj**:
```xml
<?xml version="1.0" encoding="utf-8"?>
<Project DefaultTargets="Build" xmlns="http://schemas.microsoft.com/developer/msbuild/2003">
  ...
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.props" />
  <Import Project="..\Properties\Cpp.props" />
  ...
</Project>
```
