# Code Retreat Repo

This repository was created to facilitate code retreat exercises for a team using C++.  The goals:

* Become comfortable with test-first (TDD) style coding.
* Experience paired or ensemble programming.
  
## Building

Because C++ has a heterogeneous build environment, multiple ways to build are possible.  These are the setups that have been tested with this repo:

### Visual Studio

#### Requirements

* Visual Studio installed on your system. Community edition will be fine, but higher licenses will also work.
* cmake available in the system path.

#### Commands

```
mkdir visualstudio
cd visualstudio
cmake ..
```

Assuming the cmake run completes successfully, open the generated `life.sln` file in Visual Studio.

*Note:* Build All will fail. You can safely build and run test-life, and that will work correctly.

### Clang/LLVM

#### Requirements

* Visual Studio installed. Community edition or higher will be fine.
* cmake installed in the system path
* GNU Make installed
* clang/llvm installed

Cmake, GNU Make, and LLVM can be installed independently, but it's easier using a package manager like [chocolatey](https://chocolatey.org).  Note when installing cmake that you want to use the installer package option to enable adding the package to the path.

#### Commands

```
mkdir llvm
cd llvm
cmake -G "Unix Makefiles" ..
```

Edit source with your favorite editor.

To build your project, `make` from the llvm folder.
To run tests, `test\test-life` from the llvm folder.