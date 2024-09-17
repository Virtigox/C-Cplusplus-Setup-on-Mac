# C++ Setup on Mac
>-  **Running Large-Scale C/C++ code on a Macbook with an M-Series Chip**

1. **Install Xcode**
	- Open the App Store and search for Xcode.
	- Install the latest version of Xcode.
 	- Type `xcode-select --version` to check whether it's already installed. 	

1. **Install Xcode Command Line Tools**
	- Open *Terminal* 
	- Run the following command to install command line tools:
```bash
		xcode-select --install
```

3. **Install [Homebrew](https://brew.sh/)**
	- Open *Terminal* and and install Homebrew by running:
	- Type `brew --version` to check whether it's installed.
```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

4. **Install CMake via Homebrew**
	- Install Cmake(for building C/C++ projects) using Homebrew:
	- Type `cmake --version` to check whether it's installed.
```bash
```bash
brew install cmake
```

5. **Download and Install [Visual Studio Code](https://code.visualstudio.com/download). If already skip this step.**

6. **Install necessary VS Code extensions:**
	- Open VS Code
	- Press `cmd + shift + X` to open the Extension view.
	- Search for and install the following extensions:
		- **CMake Tools**
		- **C/C++** by Microsoft

7. **Set up your project**
	- Create a new folder for your project
	- Enter the project where your executable programs exist
	- Add your source files and CMakeLists.txt
		1. Open the command palette by pressing  `cmd+shift+p`
		2. Find the `CMake: Quick Start`
		3. Enter the name of the project
		4. Choose `c++ project` option
		5. Choose `c++ executable`option
		6. Not Mandatory : include other extension package
		7. Choose the `.cpp`files

8. **Build and Run the program by selecting `play button` down the VSCode.**
<img width="1468" alt="Pasted image 20240909153320" src="https://github.com/user-attachments/assets/acc3c506-2023-4432-b15d-db2627bf412e">


9. **Configure Debugging**
	- To debug the C++ program using LLDB, set up the *launch.json* configuration. Open your `launch.json` file and add the following configuration for debugging:
	- Read this in [VScode_web](https://code.visualstudio.com/docs/cpp/config-clang-mac)
```json

{
    "configurations": [
        {
            "name": "C/C++: clang++ build and debug active file",
            "type": "cppdbg",
            "request": "launch",
            "program": "${fileDirname}/${fileBasenameNoExtension}",
            "args": [],
            "stopAtEntry": false,
            "cwd": "${fileDirname}",
            "environment": [],
            "externalConsole": false,
            "MIMode": "lldb",
            "preLaunchTask": "C/C++: clang++ build active file"
        },
        {
            "name": "C/C++: clang build and debug active file",
            "type": "cppdbg",
            "request": "launch",
            "program": "${fileDirname}/${fileBasenameNoExtension}",
            "args": [],
            "stopAtEntry": false,
            "cwd": "${fileDirname}",
            "environment": [],
            "externalConsole": false,
            "MIMode": "lldb",
            "preLaunchTask": "C/C++: clang build active file"
        }
    ],
    "version": "2.0.0"
}
```
10. Final step is to choose a kits which a toolchain for compiling and linking the project.
	- Choose the kit in `No Kit Selected` section.
 	- Or goes to the command palette, and select toolkit from `CMake: Select a kit` option.
 	- *Select the appropriate one and Happy Coding*.
<img width="1468" alt="Pasted image 20240909153320" src="https://github.com/user-attachments/assets/f95c71ba-1985-4fad-b8d3-87a68675f10e">

