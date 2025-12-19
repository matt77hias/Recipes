# Shader Build

## Widget.vcxproj

1. Add the shader targets to the VS project:

```xml
<?xml version="1.0" encoding="utf-8"?>
<Project DefaultTargets="Build" xmlns="http://schemas.microsoft.com/developer/msbuild/2003">
  ...
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.targets" />
  <Import Project="..\Targets\Shaders.targets" />
  ...
</Project>
```

2. Add the shader files to the VS project:

```xml
<?xml version="1.0" encoding="utf-8"?>
<Project DefaultTargets="Build" xmlns="http://schemas.microsoft.com/developer/msbuild/2003">
  <ItemGroup>
     <None Include="..\..\..\Code\Foo.hlsli" />
     <None Include="..\..\..\Code\Bar.hlsli" />
  </ItemGroup>
  <ItemGroup>
    <PixelShader Include="..\..\..\Code\Foo.ps.hlsl" />
    <PixelShader Include="..\..\..\Code\Bar.ps.hlsl" />
  </ItemGroup>
  <ItemGroup>
    <VertexShader Include="..\..\..\Code\Foo.vs.hlsl" />
    <VertexShader Include="..\..\..\Code\Bar.vs.hlsl" />
  </ItemGroup> 
</Project>
```

(_Shader files, added after the shader targets, should be grouped automatically based on their file extension._)
