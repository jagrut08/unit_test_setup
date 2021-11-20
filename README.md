# unit_test_setup
A skeleton setup for running unit tests, built using CMake. Works as expected on MacOS with gtest/gmock installed from source, and cmake installed as `brew install cmake`.

## Building
From the root of the repo:
- `mkdir build && cd build`
- `cmake ../ && make`


## Running
From within the `build` sub-directory, `./cpp_unit_tests.tsk` should run all gtests. Can pass in `--gtest_filter=` arg to pick and choose tests to run.


## Adding test files
Add unit test files named as `*.t.cpp`, e.g., `HelloWorld.t.cpp` at the root of the repo, and they should automatically get built and run.
