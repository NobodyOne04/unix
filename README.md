# unix

UNIX operating systems labs (2021): a build script, POSIX threads, an autotools package and a
Docker image. The lab descriptions were in Russian; this is the English version.

| Lab | Folder | Topic |
|---|---|---|
| 1 | `compile/` | `script.sh`: compile a C file in a temp folder; the output name comes from an `//Output: name` comment in the source |
| 2 | `threads/` | `main.cpp`: producer/consumer with a pthread mutex and condition variable (CMake) |
| 4 | `automake&autoconf/` | `hello.c` packaged with autoconf/automake (`configure.ac`, `Makefile.am`) |
| 5 | `docker/` | a small Django app in a `python:3.7-alpine` image |

(There is no lab 3 in the repo.)

## Run

```sh
cd compile && ./script.sh program.c                  # lab 1: builds the name given in program.c
cd threads && mkdir -p build && cd build && cmake .. && cmake --build .   # lab 2
cd 'automake&autoconf' && ./configure && make        # lab 4
cd docker && docker build . -t lab && docker run -p 8080:80 lab           # lab 5: http://localhost:8080
```

`compile/run` and `threads/run` are prebuilt Linux x86-64 binaries from the original
submission; they don't run on macOS.

Decisions: [docs/adr](docs/adr/README.md).
