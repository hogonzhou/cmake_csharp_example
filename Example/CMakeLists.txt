
#project(Example VERSION 0.1.0 LANGUAGES CSharp)
project(Example LANGUAGES CSharp)

set(CMAKE_CSharp_COMPILER "C:/Windows/Microsoft.NET/Framework64/v4.0.30319/csc.exe")


include(CSharpUtilities)

add_executable(Example
	App.config
	App.xaml
	App.xaml.cs
	MainWindow.xaml
	MainWindow.xaml.cs

	Properties/AssemblyInfo.cs
	Properties/Resources.Designer.cs
	Properties/Resources.resx
	Properties/Settings.Designer.cs
	Properties/Settings.settings)

csharp_set_designer_cs_properties(
	Properties/AssemblyInfo.cs
	Properties/Resources.Designer.cs
	Properties/Resources.resx
	Properties/Settings.Designer.cs
	Properties/Settings.settings)

csharp_set_xaml_cs_properties(
	App.xaml
	App.xaml.cs
	MainWindow.xaml
	MainWindow.xaml.cs)

set_property(SOURCE App.xaml PROPERTY VS_XAML_TYPE "ApplicationDefinition")

set_property(TARGET Example PROPERTY VS_DOTNET_TARGET_FRAMEWORK_VERSION "v4.6.1")
#set_property(TARGET Example PROPERTY VS_DOTNET_TARGET_FRAMEWORK_VERSION "v5.0")
#set_property(TARGET Example PROPERTY WIN32_EXECUTABLE TRUE)

set_property(TARGET Example PROPERTY VS_DOTNET_REFERENCES
	"Microsoft.CSharp"
	"PresentationCore"
	"PresentationFramework"
	"System"
	"System.Core"
	"System.Data"
	"System.Data.DataSetExtensions"
	"System.Net.Http"
	"System.Xaml"
	"System.Xml"
	"System.Xml.Linq"
	"WindowsBase")

