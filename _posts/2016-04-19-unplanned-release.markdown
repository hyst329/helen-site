---
layout: post
title: "Unplanned release"
date: "2016-04-19 12:37:33 +0300"
---

Today is the date of initially unplanned release --- v0.1.5.
It was decided to do this because the 0.2.0 isn't yet buildable, but the 0.1
family lacks a very important feature --- the ability to call C 'vararg'
(i. e. variable-argument count) function from Helen. So, this is only new
feature in 0.1.5.

The declaration is very similar to C:

```
declare printf(ptr char fmt, ...) style(C)
```

Compare with this

```C
int printf(char* fmt, ...);
```

These changes are already integrated to the 0.2 branch (currently `master`),
so this is also a first step to variable-argument functions in Helen!
