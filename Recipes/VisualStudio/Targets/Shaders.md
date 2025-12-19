# Shader Build

1. Add the shader targets to the VS project:

**Widget.vcxproj**:
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

**Widget.vcxproj**:
```xml
<?xml version="1.0" encoding="utf-8"?>
<Project DefaultTargets="Build" xmlns="http://schemas.microsoft.com/developer/msbuild/2003">
  <ItemGroup>
     <None Include="..\..\..\Code\Foo.hlsli" />
     <None Include="..\..\..\Code\Bar.hlsli" />
  </ItemGroup>
  <ItemGroup>
    <ComputeShader Include="..\..\..\Code\Foo.ps.hlsl" />
    <ComputeShader Include="..\..\..\Code\Bar.ps.hlsl" />
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

**Widget.vcxproj.filters**:
```xml
<?xml version="1.0" encoding="utf-8"?>
<Project ToolsVersion="4.0" xmlns="http://schemas.microsoft.com/developer/msbuild/2003">
  ...
  <ItemGroup>
    <None Include="..\..\..\Code\Foo.hlsli">
      <Filter>Header Files</Filter>
    </None>
    <None Include="..\..\..\Code\Bar.hlsli">
      <Filter>Header Files</Filter>
    </None>
  </ItemGroup>
  <ItemGroup>
    <ComputeShader Include="..\..\..\Code\Foo.ps.hlsl">
      <Filter>Source Files</Filter>
    </ComputeShader>
    <ComputeShader Include="..\..\..\Code\Bar.ps.hlsl">
      <Filter>Source Files</Filter>
    </ComputeShader>
  </ItemGroup>
  <ItemGroup>
    <PixelShader Include="..\..\..\Code\Foo.ps.hlsl">
      <Filter>Source Files</Filter>
    </PixelShader>
    <PixelShader Include="..\..\..\Code\Bar.ps.hlsl">
      <Filter>Source Files</Filter>
    </PixelShader>
  </ItemGroup>
  <ItemGroup>
    <VertexShader Include="..\..\..\Code\Foo.vs.hlsl">
      <Filter>Source Files</Filter>
    </VertexShader>
    <VertexShader Include="..\..\..\Code\Bar.vs.hlsl">
      <Filter>Source Files</Filter>
    </VertexShader>
  </ItemGroup>
  ...
</Project>
```
(_Shader files, added after the shader targets, should be grouped automatically based on their file extension._)
