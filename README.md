![GitHub forks][github-forks]
![GitHub Repo stars][github-stars]
![GitHub contributors][github-contributors]
![GitHub][github-license]
[![NuGet][nuget-badge]][nuget-package]

## About

DoxygenTool is a repackaging of the [Doxygen][doxygen-site] Documentation Generator as a [Dotnet tool][dotnet-tools].

Doxygen is already available in numerous formats for [installation][doxygen-download].
Packaging it as a Dotnet tool allows for multiple versions to be installed and cached on a system
simultaneously, and users can control which version is used through a
[Dotnet tool manifest file][dotnet-manifest].

## Installation & Usage

The following will add DoxygenTool to a Dotnet tool manifest file:

```bash
dotnet new tool-manifest # if you are setting up this repo
dotnet tool install --local DEMAConsulting.DoxygenTool
```

The tool can then be executed by:

```bash
dotnet doxygen <arguments>
```

## Contributing

Contributions are welcome! Please see our [Contributing Guide][contributing] for details.

## Code of Conduct

This project has adopted a [Code of Conduct][code-of-conduct] that we expect participants to adhere to.

## Security

For information about reporting security vulnerabilities, please see our [Security Policy][security].

## License

This project is licensed under the GPL-2.0-or-later License - see the [LICENSE][license] file for details.

[github-forks]: https://img.shields.io/github/forks/demaconsulting/DoxygenTool?style=plastic
[github-stars]: https://img.shields.io/github/stars/demaconsulting/DoxygenTool?style=plastic
[github-contributors]: https://img.shields.io/github/contributors/demaconsulting/DoxygenTool?style=plastic
[github-license]: https://img.shields.io/github/license/demaconsulting/DoxygenTool?style=plastic
[nuget-badge]: https://img.shields.io/nuget/v/DemaConsulting.DoxygenTool?style=plastic&logo=nuget
[nuget-package]: https://www.nuget.org/packages/DemaConsulting.DoxygenTool
[doxygen-site]: https://www.doxygen.nl/
[doxygen-download]: https://www.doxygen.nl/download.html
[dotnet-tools]: https://learn.microsoft.com/en-us/dotnet/core/tools/global-tools
[dotnet-manifest]: https://learn.microsoft.com/en-us/dotnet/core/tools/global-tools#install-a-local-tool
[contributing]: https://github.com/demaconsulting/DoxygenTool/blob/main/CONTRIBUTING.md
[code-of-conduct]: https://github.com/demaconsulting/DoxygenTool/blob/main/CODE_OF_CONDUCT.md
[security]: https://github.com/demaconsulting/DoxygenTool/blob/main/SECURITY.md
[license]: https://github.com/demaconsulting/DoxygenTool/blob/main/LICENSE

