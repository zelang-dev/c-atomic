# c-atomic

## An C89 compatible interface to C11 Atomics.

This library aims to implement an equivalent to the C11 atomics library. It's intended to be used as a way to enable the use of atomics in a mostly consistent manner to modern C, while still enabling compatibility with older compilers.

This **fork** is _WIP_ for an drop-in replacement to [C11 atomics](https://en.cppreference.com/w/c/atomic).

For _general usage on how to use_, see [Chapter 40 Atomics](https://beej.us/guide/bgc/html/split/chapter-atomics.html#lock-free-atomic) in **Beej's Guide to C Programming**, [An Introduction to Lock-Free Programming](https://preshing.com/20120612/an-introduction-to-lock-free-programming), and [Microsoft Windows: Atomic ops and memory barriers](https://billauer.co.il/blog/2021/05/windows-atomic-memory-fences/)

-----

### Usage

This is a header-only library. Just add `catomic.h` to your source tree and include it:

```c
#include "catomic.h"
```
