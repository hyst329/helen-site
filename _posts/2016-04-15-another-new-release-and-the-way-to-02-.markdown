---
layout: post
title: "Another new release and the way to 0.2 "
date: "2016-04-15 19:54:04 +0300"
---

Version 0.1.4 of Helen is released. However, it doesn't add any new features,
except the new syntax rules for the future feature --- generics.

The generic function syntax looks like this:
```
fun generic[T] f (T a, T b, int c) -> T
# The code comes here
endfun
```
Here `T` is the type parameter; when a specific instance of `f`, e. g. `f[int]`
is created, all occurrences of `T` are replaced by `int` (just like a feature
  in Java/C#, also called generics, and equivalent C++'s templates).

But, at least as of v0.1.4, generics are unusable. The code for `helc` itself
needs many structural improvements, so it was decided to _completely overhaul_
the code by 0.2.0 release; so, 0.1.4 will be the latest release in the 0.1
family, and the code for it now will reside at `v0.1` branch (which is now
archived). Maybe, the pattern of LDC will be used, because LDC is also an
LLVM-based compiler (for the D language, which already contains some features
to be implemented in Helen).
