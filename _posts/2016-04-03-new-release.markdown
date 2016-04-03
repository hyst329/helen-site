---
layout: post
title:  "New release"
date:   2016-04-03 18:46:20 +0300
categories: Helen site
---

The new version of Helen, v0.1.3, is released today. It's mostly a bugfix
release, which doesn't add any new features both to the language and the tools.

Main features of this release are:
1. First, a bug with string literals was fixed. Essentially, the references to
string methods were not loaded to the resulting object, when a string was
constructed from a literal.
```
# Like this
String s1 = "Helen is the best"
# and not like this
String s2 = new String
```
As a consequence, all the standard library `libhelstd` renders almost unusable.
This annoying bug was finally fixed, so now you can deal with strings.
2. Second, there was also a bug in `helmake` tool for generating make files.
A bug was in the bitcode file name - it was absolute instead of being relative,
which lead to building errors with `make`.
