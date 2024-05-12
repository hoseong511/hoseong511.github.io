---
layout: post
title: Hello World!
date: 2024-05-11 14:41 +0900
description: 
category: 환영
tags: 
---

```c
#include <stdio.h>

int main(void)
{
      printf("Hello Wolrd1");
      return 0;
}
```

**cpp -> cc1 -> as -> ld**

main.c  -> main.i -> main.s -> main.o -> a.out

```bash
> clang -E main.c -o main.i
> clang -S main.i main.s
> as main.s -o main.o
> ld -o a.out -lto_library /Library/Developer/CommandLineTools/usr/lib/libLTO.dylib -syslibroot /Library/Developer/CommandLineTools/SDKs/MacOSX.sdk -L/usr/local/lib -lSystem /Library/Developer/CommandLineTools/usr/lib/clang/15.0.0/lib/darwin/libclang_rt.osx.a main.o
```

> **명령어 'clang main.c'** 이면 위와 같은 컴파일과 링크과정이 절차적으로 발생한다.

### **참조**

-   CSAPP:part2-7 linker
-   clang v15.0.0 [https://releases.llvm.org/15.0.0/tools/clang/docs/CommandGuide/clang.html](https://releases.llvm.org/15.0.0/tools/clang/docs/CommandGuide/clang.html)