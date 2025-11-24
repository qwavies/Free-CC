<h1 align="center">Free-CC: A Modified Version of <a href="https://github.com/TinyCC/tinycc">TCC (Tiny C Compiler)</a> Without the need for Semicolons! </h1>

<p align="center">If the compiler is smart enough to figure out where the semicolons <em>should</em> go, then why need them in the first place? -Aristole, probably</p>

## Requirements

- `make` installed on your system
- `gcc` installed on your system
- OS specific Requirements
  - BSD should use `gmake` instead of `make`
  - Windows should follow the instructions in `./win32/tcc-win32.txt`

## Installation

1. Run `./configure`
2. Run `make`
3. Run `make install` (root may be needed)
4. Optionally run `make test`

## Demo

The file `./tests/modified_hello_world.c` has been created as an example for what this compiler can do.

If you `cat ./tests/modified_hello_world.c`, you will get the following result:

```c
#include <stdio.h>

int main() {
    printf("Hello, world!\n") printf("2 print statements on the same line??\n")
    printf("Wow! No semicolons in this file???\n")
    return 0;
}
```

You can check if the code compiles by running `tcc ./tests/modified_hello_world.c && ./a.out`, which should get you the following output:
```
Hello, world!
2 print statements on the same line??
Wow! No semicolons in this file???
```

Feel free to compile your own semicolon-free c files!

## Changes from the Original TCC

- Forked off of the <a href="https://github.com/TinyCC/tinycc">Tiny C Compiler</a>
- Removed the need for semicolons as a statement terminator
- Removed README
- Added README.md
- Added tests/modified_hello_world.c
