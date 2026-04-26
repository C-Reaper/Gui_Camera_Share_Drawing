# Project README

## Overview
This project is a simple camera application built using C/C++ and various libraries. The application utilizes the WindowEngine1.0 library for window management, RLCamera for camera functionality, and ImageFilter for image processing.

## Features
- Basic camera setup
- Displaying the camera feed in a window
- Point rendering based on mouse position

## Project Structure
### Prerequisites
- C/C++ Compiler (GCC)
- Make utility
- Standard development tools
- Libraries:
  - WindowEngine1.0
  - RLCamera
  - ImageFilter
  - X11 for Linux

## Build & Run
### Building on Linux
To build the project on a Linux system, follow these steps:

```bash
cd /path/to/project
make -f Makefile.linux all
```

This will compile the source code and generate an executable named `Main` in the `build/` directory.

To execute the program:
```bash
./build/Main
```

### Building on Windows
To build the project on a Windows system, follow these steps:

1. Install MinGW or MSYS2 to get GCC.
2. Open a command prompt and navigate to your project directory.
3. Build the project with debugging symbols for easier debugging:
```bash
make -f Makefile.windows alldebug
```

This will compile the source code and generate an executable named `Main.exe` in the `build/` directory.

To execute the program, simply run:
```bash
./build/Main.exe
```

### Building on WebAssembly
To build the project for the web using Emscripten:

1. Install Emscripten SDK.
2. Set up your environment by running `emsdk_env.sh`.
3. Navigate to your project directory and build with:
```bash
make -f Makefile.web all
```

This will compile the source code and generate an HTML file in the `build/` directory. You can run this using a web server or by opening it directly in a browser.

To execute, use Emscripten's built-in server:
```bash
emrun --no_browser --port 8080 build/index.html
```

### Build Options
- `make -f Makefile.(os) all`: Compile the project.
- `make -f Makefile.(os) do`: Compile and execute the project.
- `make -f Makefile.(os) clean`: Clean up build artifacts.

Replace `(os)` with `linux`, `windows`, or `web` depending on your target platform.