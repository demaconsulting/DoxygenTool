![GitHub forks](https://img.shields.io/github/forks/demaconsulting/DoxygenTool?style=plastic)
![GitHub Repo stars](https://img.shields.io/github/stars/demaconsulting/DoxygenTool?style=plastic)
![GitHub contributors](https://img.shields.io/github/contributors/demaconsulting/DoxygenTool?style=plastic)
![GitHub](https://img.shields.io/github/license/demaconsulting/DoxygenTool?style=plastic)

# About

DoxygenTool is a repackaging of the [Doxygen](https://www.doxygen.nl/) Documentation Generator as a [Dotnet tool](https://learn.microsoft.com/en-us/dotnet/core/tools/global-tools).

Doxygen is already available in numerous formats for [installation](https://www.doxygen.nl/download.html).
Packaging it as a Dotnet tool allows for multiple versions to be installed and cached on a system
simultaneously, and users can control which version is used through a
[Dotnet tool manifest file](https://learn.microsoft.com/en-us/dotnet/core/tools/global-tools#install-a-local-tool).


# Installation & Usage

The following will add DoxygenTool to a Dotnet tool manifest file:

```
dotnet new tool-manifest # if you are setting up this repo
dotnet tool install --local DEMAConsulting.DoxygenTool
```

The tool can then be executed by:

```
dotnet doxygen <arguments>
```
