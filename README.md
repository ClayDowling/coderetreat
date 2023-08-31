# Code Retreat Repo

This repository was created to facilitate code retreat exercises for a team using C++.  The goals:

* Become comfortable with test-first (TDD) style coding.
* Experience paired or ensemble programming.
  
## The Exercise

Implement the rules for [Conway's Game of Life](https://en.wikipedia.org/wiki/Conway%27s_Game_of_Life).

1. Start by writing the simplest failing test that can cause a code change. It is important that the test fails, and fails for the correct reason.

2. Write just enough code, and no more, to make the test pass.  _If the test will pass without the code, remove the code._

Work either as a pair, alternating between driver (at the keyboard) and navigator (in charge of thinking), or as an enemble.

In an ensemble arrangement, the driver only remains the driver for a short period of time, 5 to 10 minutes. After the interval has expired, the navigator becomes the driver, and the driver gets to rest.

*The Driver* controls the keyboard, runs builds, and runs tests. They're not in charge of the deep thinking.  If the driver is unfamiliar with the language or the domain, the navigator is responsible for telling them what to do, in whatever level of detail is necessary.

*The Navigator* is in charge of the thinking. They figure out what failing test should be written and what logic should be written to make the test pass.  They fill gaps in language, tool, or domain knowledge that the driver may have.

Anybody else involved in the ensemble is free to offer suggestions, but is not obligated to. They can grab coffee, go into a mental rest mode, or whatever is necessary for them to be ready for their next time as a driver or navigator. It is often helpful to be monitoring what is being done. This passive observation functions as a code review.

### On Timing

People experienced with pair and ensemble programming can switch roles on a more casual basis. But especially with larger ensembles, a timer of 5 to 10 minutes is recommended.  The fast switches keep the context fresh in everybody's mind, and forces more frequent, more explicit communication.  The chief benefit of ensemble programming is wide knowledge of the entire system. Effectively everybody becomes an experienced developer in the system all at once.

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