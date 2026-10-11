# CSE 165 · Introduction to Object Oriented Programming

**UC Merced · Fall 2023 · C++ coursework**

Eight lab folders covering console programs, strings and vectors, pointers, classes, inheritance, and virtual methods. This repository preserves individual exercise sources, local headers, assignment PDFs, and original submission artifacts.

## Explore the labs

| Lab | Source guide | Assignment |
| --- | --- | --- |
| [1](Lab%201/) | [Console and file exercises](Lab%201/Code/): greeting, circle area, quadratic roots, text loading, and word counting | [PDF](Lab%201/Lab%201%20Exercises.pdf) |
| [2](Lab%202/) | [Number and pointer exercises](Lab%202/Code/): bit manipulation, numeric formatting, and arithmetic through pointers | [PDF](Lab%202/Lab%202%20Exercises.pdf) |
| [3](Lab%203/) | [String search](Lab%203/AddingandSearchingStrings.cpp), [integer accumulation](Lab%203/Integer_Accumulator.cpp), and [nested vectors](Lab%203/Vector_of_Vector.cpp) | [PDF](Lab%203/Lab%203%20Exercises.pdf) |
| [4](Lab%204/) | [Stash](Lab%204/Exercise%201/), [stack](Lab%204/Exercise%202/), [linked list](Lab%204/Exercise%203/), [void pointers](Lab%204/Exercise%204/), [entry](Lab%204/Exercise%205/), and [address book](Lab%204/Exercise%206/) | [PDF](Lab%204/Lab%204%20Exercises.pdf) |
| [5](Lab%205/) | [Circle class](Lab%205/Exercise%201/), [animal inheritance](Lab%205/Exercise%202/), [inheritance with a list](Lab%205/Exercise%203/), [instance counting](Lab%205/Exercise%204/), and [stack construction/destruction](Lab%205/Exercise%205/) | [PDF](Lab%205/Lab%205%20Exercises.pdf) |
| [6](Lab%206/) | [Vector class](Lab%206/Exercise%201/), [rectangle checks](Lab%206/Exercise%202/), and [interactive point containment](Lab%206/Exercise%203/) | [PDF](Lab%206/Lab%206%20Exercises.pdf) |
| [7](Lab%207/) | [References](Lab%207/Exercise%201/), [pointer initialization](Lab%207/Exercise%202/), [virtual animal methods](Lab%207/Exercise%203/), and [virtual window resizing](Lab%207/Exercise%204/) | [PDF](Lab%207/Lab%207%20Exercises.pdf) |
| [8](Lab%208/) | [Sortable interface](Lab%208/Exercise%203/Sortable.h): abstract `compare` and `print` methods; no executable implementation is included | [PDF](Lab%208/Lab%208%20Exercises.pdf) |

## Working with the source

Use a C++ compiler and standard library with **C++11 or later** support (`nullptr` and `override` appear in the later labs). There is no repository-wide build configuration or dependency manifest. Each complete exercise has its own `main`; compile one exercise at a time, keeping its neighboring headers together. Quote paths because lab and exercise names contain spaces.

The following commands are source-checked examples for a shell with `g++` installed. They were not compiled or executed during this documentation update because no C++ compiler was available on the review machine.

### Small console program

From the repository root, in a POSIX shell:

```sh
g++ -std=c++11 -Wall -Wextra "Lab 1/Code/Hello_world.cpp" -o /tmp/cse165-hello
/tmp/cse165-hello
```

The source prints `Hi, my name is Munir!` and takes no input.

### Reference exercise

```sh
g++ -std=c++11 -Wall -Wextra "Lab 7/Exercise 1/refs.cpp" -o /tmp/cse165-refs
printf '7\n' | /tmp/cse165-refs
```

The program prompts for an integer, passes it by reference to `triple`, and prints the resulting value (`21` for this input).

### File-dependent exercise

[Counting_words.cpp](Lab%201/Code/Counting_words.cpp) opens `words.txt` relative to the **working directory**. Run it inside `Lab 1/Code` so it can find the [included text file](Lab%201/Code/words.txt):

```sh
cd "Lab 1/Code"
g++ -std=c++11 -Wall -Wextra Counting_words.cpp -o /tmp/cse165-count
/tmp/cse165-count
```

Its `White Space Count:` label reports whitespace-delimited tokens read with `operator>>`, rather than the number of whitespace characters. The text-loading exercises similarly open `code.cpp` from their working directory.

## Archive notes

- These are preserved coursework submissions, with no automated test suite or guarantee that every exercise builds or behaves correctly. The [vector](Lab%206/Exercise%201/vectors.cpp) and [rectangle](Lab%206/Exercise%202/rectangles.cpp) programs include their own printed checks.
- [More_on_Inheritance.cpp](Lab%205/Exercise%203/More_on_Inheritance.cpp) contains an unterminated `#include "display.h` line. [Word_occurences.cpp](Lab%201/Code/Word_occurences.cpp) uses `transform` without including `<algorithm>`. These sources need attention before a reliable build.
- [refs2.cpp](Lab%207/Exercise%202/refs2.cpp) dereferences an uninitialized pointer. Inspect it before running. Temporary `tempCodeRunnerFile.cpp` fragments are also retained and are not standalone programs.
- Original ZIP archives and extensionless compiled artifacts remain in place. Build from the readable sources for your own platform; the stored binaries have not been validated here.

