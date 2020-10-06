# Valgrind Creation
[![Build Status](https://travis-ci.org/adigoswami/Valgrind.svg?branch=master)](https://travis-ci.org/adigoswami/Valgrind)
[![Coverage Status](https://coveralls.io/repos/github/adigoswami/Valgrind/badge.svg?branch=master)](https://coveralls.io/github/adigoswami/Valgrind?branch=master)
---

## Overview

Starter project to implement valgrind to ensure maintanable code


## Standard install via command-line
```
git clone --recursive https://github.com/dpiet/cpp-boilerplate
cd <path to repository>
mkdir build
cd build
cmake ..
make
Run tests: ./test/cpp-test
Run program: ./app/shell-app
```

## Running valgrind
```
cd build/app
valgrind --leak-check=full --log-file=../../<file_name.txt> ./shell-app
valgrind --tool=callgrind ./shell-app
kcachegrind <callgrind.out.#> 
```

## Building for code coverage (for assignments beginning in Week 4)
```
sudo apt-get install lcov
cmake -D COVERAGE=ON -D CMAKE_BUILD_TYPE=Debug ../
make
make code_coverage
```
This generates a index.html page in the build/coverage sub-directory that can be viewed locally in a web browser.
