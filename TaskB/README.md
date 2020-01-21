---
title: 'Project 1b: XV6 Intro - Syscall'
---

We'll be doing kernel hacking projects in xv6. Xv6 is a port of a
classic version of unix to a modern processor, Intel's x86. It is a much
smaller and simpler kernel than the Linux kernel, making it more
accessible for projects and study.

The goal of this project is to implement a new system call to the xv6
kernel. This project is just a warmup, and thus relatively light on
actual code. The goal of the project is simple: to add a system call to
XV6. Your system call, `getprocs()`, simply returns how many processes
exist in the system at the time of the call.

 \
**Details**

 \
Your new syscall should look like this: `int getprocs(void)`\
Your system call returns the number of processes that exist in the
system at the time of the call.

 \
**Tips**

-   Find some other system call, like `getpid()` or any other simple
    call. Basically, copy it in all the ways you think are needed. Then
    modify it to do what you need.

-   Most of the time will be spent on understanding the code. There
    shouldn't be a whole lot of code added.

-   Using `gdb` (the debugger) may be helpful in understanding code,
    doing code traces, and is helpful for later projects too. Get
    familiar with this fine tool!

-   Remember that you will be writing *kernel code* to implement this
    system call. You must also write `userspace` code to test it.
    Remember that *kernel code* can impact the entire system. Think
    about your changes!

 \
**The Code**

 \
The source code for XV6 (and associated README) can be found in
<https://github.com/tallendev/xv6-cuspring2019>. Everything you need to
build and run and even debug the kernel is in there.

You may also find the following readings about xv6 useful, written by
the same team that ported xv6 to x86. See the course web page for this
and other resources. Particularly useful for this project: Chapters 0,
1, 2.

Remember that xv6 is *not* Linux. Every OS provides a standard library:
a grouping of functions for interacting with the operating system and
doing basic programming tasks. You may be familiar with the GNU C
standard library, and you probably used it in Project 1a. In xv6, you
will not have access to this standard library. xv6 does provide some
utility functions for you, ad syscalls for interacting with the kernel.
In practice, this means that if you find yourself writing system-scope
includes (`#include <…>`, not `#include ".."`), you have made a mistake.
Be careful, because your code may still compile but not run correctly in
the xv6 environment.

 \
**Submission**

-   Your archive should not contain temporary object files or
    executables when you submit it. To ensure this, just run
    `make clean` before archiving the directory.

-   Your code must run on the lab 110 machines, at minimum.

-   Your program must be written in C (not C++ or other languages).

-   You will have to modify the Makefile and kernel files. Do not
    *delete* anything from the Makefile - it may be used for grading.

-   Submit the archive via Canvas before the deadline.
