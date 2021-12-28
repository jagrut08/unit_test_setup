# unit_test_setup
A skeleton setup for running unit tests, built using CMake. Works as expected on MacOS with gtest/gmock installed from source, cmake installed as `brew install cmake`, and clang-tidy installed by installing [llvm](https://stackoverflow.com/questions/53111082/how-to-install-clang-tidy-on-macos).

## Building
From the root of the repo:
- `mkdir build && cd build`
- `cmake ../ && make`


## Running
From within the `build` sub-directory, `./cpp_unit_tests.tsk` should run all gtests. Can pass in `--gtest_filter=` arg to pick and choose tests to run.


## Adding test files
Add unit test files named as `*.t.cpp`, e.g., `HelloWorld.t.cpp` at the root of the repo, and they should automatically get built and run.


## Running static analysis
From the root of the repo, run `clang-tidy -p build/ <filename.t.cpp>`. A compilation should exist in the `build/` directory after `make` succeeds.
