# Godot-4.3-GDUnit4-CSharp-VisualStudio-2022
Working on Unit testing with Godot using Visual Studio 2022 and C# utilizing GDUnit4

## Prerequisites
Make sure you have the following installed before starting:

- **Godot 4.3**
- **Visual Studio 2022**
- **.NET SDK (8.0)**

## Steps to Install:

### 1. Create a New Godot Project
1. Open **Godot 4.3**.
2. Click on **Create**.
3. Choose a Project Name and Project Path.
5. Click **Create & Edit** to open the project.

### 2. Install GDUnit4 Plugin
1. Open the **AssetLib** from the top menu in Godot.
2. Search for **GdUnit4**.
3. Select **GdUnit4** from the search results and click **Download**.
4. Once downloaded, click **Install**.
5. After installation, **restart Godot** to avoid any caching issues.

### 3. Activate GDUnit4 Plugin
1. Go to **Project > Project Settings** in the Godot editor.
2. Navigate to the **Plugins** tab.
3. Find **GdUnit4** in the list of plugins and check the box to activate it.
4. Save your project settings and **restart Godot**.

### 4. Configure C# Project for GDUnit4
1. Open the project in **Visual Studio 2022** by double-clicking a C# script in Godot.
2. Open the `.csproj` file in Visual Studio and ensure it includes the following:

   ```xml
   <Project Sdk="Godot.NET.Sdk/4.3.0">
      <PropertyGroup>
         <TargetFramework>net8.0</TargetFramework>
         <LangVersion>11.0</LangVersion>
         <Nullable>enable</Nullable>
         <CopyLocalLockFileAssemblies>true</CopyLocalLockFileAssemblies>
         <NoWarn>NU1605</NoWarn>
      </PropertyGroup>
      <ItemGroup>
         <PackageReference Include="gdUnit4.api" Version="4.3.*" />
         <PackageReference Include="Microsoft.NET.Test.Sdk" Version="17.9.0" />
         <PackageReference Include="gdUnit4.test.adapter" Version="2.*" />
      </ItemGroup>
   </Project>
