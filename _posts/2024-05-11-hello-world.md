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

xxd a.out
```xxd
			.
			.
			.

00003f90: 1002 40f9 0002 1fd6 4865 6c6c 6f20 776f  ..@.....Hello wo
00003fa0: 726c 6421 0000 0000 0100 0000 1c00 0000  rld!............

			.
			.
			.
```
xxd에서 리틀엔디안 출력하려면 ```xxd -e a.out```

objdump -hD a.out
```objdump
			.
			.
			.

0000000100003f98 <__cstring>:
100003f98: 6c6c6548     ldnp    d8, d25, [x10, #-320]
100003f9c: 6f77206f     umlal2.4s       v15, v3, v7[3]
100003fa0: 21646c72     <unknown>
100003fa4: 00           <unknown>

			.
			.
			.
```

### **참조**

-   CSAPP:part2-7 linker
-   clang v15.0.0 [https://releases.llvm.org/15.0.0/tools/clang/docs/CommandGuide/clang.html](https://releases.llvm.org/15.0.0/tools/clang/docs/CommandGuide/clang.html)