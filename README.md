# General_installation_guide

1) Install [Git](https://git-scm.com/downloads)*.
2) Install [CMake](https://cmake.org/download/)*.
3) Install a build system, for example, [Ninja](https://github.com/ninja-build/ninja/releases)*.
4) Install a C/C++ compiler, for example, [Clang](https://github.com/llvm/llvm-project/releases)*.
5) Add the paths of Git, CMake, and the compiler executables to your OS environment paths:
   - **Windows**: Go to "System Properties" > "Environment Variables" and add the paths to the "Path" variable.
   - **macOS/Linux**: Add the paths to `.bashrc`, `.zshrc`, or `.profile`. For example:
     ```bash
     export PATH="/path/to/git/bin:/path/to/ninja/bin:/path/to/cmake/bin:/path/to/clang/bin:$PATH"
     ```
6) Presets are set for Ninja and Clang. If you are using different software, you can edit the `CMakePresets.json` file in the project root to configure your preferred build system or compiler.
7) Open a terminal, change the directory to the project root, and run `git init` to initialize a new Git repository. After this, run the `bash all.sh` command to configure, build, and run the project. Alternatively, you can run the scripts separately: `bash configure.sh`, `bash build.sh`, and `bash run.sh`.
   - You can pass an argument to each script:
     - `-r` for release mode
     - `-d` for debug mode
   - If no argument is passed, it defaults to release mode. For example:
     ```bash
     bash all.sh -d    # Configures, builds, and runs in debug mode
     bash build.sh -r  # Builds in release mode
     bash run.sh       # Runs in release mode
     ```
   - **Note for Windows users**: Make sure you have a Bash shell installed, such as Git Bash or WSL (Windows Subsystem for Linux).
   - **Note for Linux users**: You might need to install additional libs: libx11-dev libgl1-mesa-dev libglu1-mesa-dev libudev-dev libxrandr-dev libxcursor-dev libfreetype6-dev.

\* \- You can install this software with your package manager, or by clicking the provided link and following the manual installation instructions.
