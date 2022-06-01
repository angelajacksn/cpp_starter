# C++ Starter
Template C++/CMake project to get a quick start 

Requires:
* CMake
* A (hopefully modern) C++ compiler

Includes:
* Simple CMake setup
* Easy to enable tests with CTest
* [fmt](https://github.com/fmtlib/fmt) as submodule for formatting

# Getting Started
Use the big green [Use this template](https://github.com/angelajacksn/cpp_starter/generate) button on the top right of
the GitHub repo. After which you can simply clone your project and get started.
```
git clone https://github.com/<username>/<repo>.git <folder>
```

# Testing
We provide a utility `define_test` function to use
in CMake. Currently, it requires you to create a library.

Steps to enable testing:
1. Create library target: `add_library(${my_project_lib} <source_files>)`. (CMake variable `my_project_lib` is created for you.)
2. Create a <test_name>.cpp file
3. Use `define_test(<test_name>)` in any CMakeLists.txt under `tests/` folder to create a new test executable
4. Set CMake option `ENABLE_TESTING` to build tests