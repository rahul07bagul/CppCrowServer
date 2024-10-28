
# Crow Web Server in C++

This project is a basic setup for creating a web server using the Crow framework in C++. Follow the steps below to install necessary tools, set up the project structure, and run a simple Crow server.

## Prerequisites

- **Operating System**: Windows
- **Tools Required**:
  - [Visual Studio Code (VS Code)](https://code.visualstudio.com/)
  - [CMake](https://cmake.org/download/)
  - [vcpkg](https://github.com/microsoft/vcpkg) - C++ package manager

## Setup and Installation

### 1. Clone this repository and open in VS Code

### 2. Install `vcpkg` and Set Up Dependencies

1. Clone the `vcpkg` repository and install Crow and Asio dependencies:
   Open terminal in root directory and execute below commands-

   ```bash
   git clone https://github.com/microsoft/vcpkg.git
   cd vcpkg
   .\bootstrap-vcpkg.bat
   .\vcpkg install crow asio
   .\vcpkg integrate install
   ```

### Build the Project
1. Configure CMake to use `vcpkg`:
   - In `.vscode/settings.json`, add:

     ```json
     {
       "cmake.configureSettings": {
         "CMAKE_TOOLCHAIN_FILE": "${workspaceFolder}/vcpkg/scripts/buildsystems/vcpkg.cmake"
       }
     }
     ```

2. Run **CMake: Configure** from command palette and after that use build button which is at the bottom of the VS Code. The executable will be created in `build/Debug`.

### 3. Run the Application

To run the server:

```bash
cd build/Debug
.\MyCrowProject.exe
```

Navigate to `http://localhost:8080` in a web browser to see the message `"Hello, World!"`.
