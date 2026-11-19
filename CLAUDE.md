# unix

UNIX OS labs (2021): shell build script, pthreads, autotools, Docker. One folder per lab.

## Commands
- Lab 1: `cd compile && ./script.sh program.c`
- Lab 2: `cd threads && mkdir -p build && cd build && cmake .. && cmake --build .`
- Lab 4: `cd 'automake&autoconf' && ./configure && make` (quote the folder name)
- Lab 5: `cd docker && docker build . -t lab && docker run -p 8080:80 lab`
No tests.

## Layout
- `compile/`: `script.sh`, `program.c` (with `//Output:`), prebuilt `run` (Linux ELF).
- `threads/`: `main.cpp`, `CMakeLists.txt`, prebuilt `run` (Linux ELF).
- `automake&autoconf/`: `hello.c`, `configure.ac`, `Makefile.am` plus generated autotools files.
- `docker/`: `Dockerfile`, `app/` (Django project `vendor`, app `rest`).
- `docs/adr/`: decision records (`.adr`), index in `docs/adr/README.md`.

## Conventions
- Read the ADR before changing a recorded decision; commit subjects carry its number.
- The generated autotools files and prebuilt binaries are the submitted state; leave them.
- Archived coursework: docs or small fixes only unless asked.
