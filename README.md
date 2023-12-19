# Raspberry Pi Pico Visual Studio Code extension

This is the official Visual Studio Code extension for Raspberry Pi Pico development. It provides a set of tools to help you develop for the Pico using Visual Studio Code.

[Download latest Beta RC 📀](https://github.com/paulober/vscode-raspberry-pi-pico/releases/tag/v0.9.1)

## Features

- Project generator (supports options for Board-Type and Libraries; targets ninja build system)
- Automatic CMake configuration on project load
- Easy option to switch between Pico-SDK and ARM Toolchain versions
- No configuration of environment variables required
- Automatic download/management of Toolchain and SDK (no separate manuall download/installation required)
- On-click project compilation per status bar button (with the selected Pico-SDK and Toolchain)

## Requirements by OS

> Supported Platforms: Windows x64, macOS (Sonoma only), Linux x64 and arm64

- Visual Studio Code v1.84.2 or later
- Native C/C++ compiler (in PATH), supported compilers are: `gcc` and `clang`
- \[Optional\] OpenOCD for debuging

### macOS
- Git (in PATH, you can install it by running `xcode-select --install`)
- Tar (in PATH)

### Linux
- Python 3.9 or later (in PATH or set in settings)
- Git (in PATH)
- Tar (in PATH)
- Ninja (in PATH on Linux aarch64 only)

## Extension Settings

This extension contributes the following settings:

* `raspberry-pi-pico.cmakePath`: Set custom cmake path
* `raspberry-pi-pico.python3Path`: Set custom python3 path
* `raspberry-pi-pico.ninjaPath`: Set custom ninja path
* `raspberry-pi-pico.gitPath`: Set custom git path
* `raspberry-pi-pico.cmakeAutoConfigure`: Enable/Disable cmake auto configure on project load

## Known Issues

- Cannot run project generator 2 times in a row without restarting the extension
- Custom Ninja, Python3 or git paths are not stored in CMakeLists.txt like SDK and Toolchain paths so using them would require to build and configure the project thought the extension
