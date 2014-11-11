---
layout: post
title:  "Elixir Recipe: Binary Pattern Matching"
date:   2014-11-12 00:20:45
categories: elixir otp
---

Playing around on [exercism.io](http://exercism.io) (highly recommended) I came across some interesting binary pattern matching that isn't in the Elixir lang Getting Started guide:

```Elixir
iex(44)> <<var::binary-3, rest::binary>> = "foobar"
"foobar"
iex(45)> var
"foo"
iex(46)> rest
"bar"
```

Apparently, what it's doing is specifying `var` as a three byte binary (and strings are binaries in Elixir). Note that these are bytes, not codepoints:

```Elixir
iex(55)> <<var::binary-1, rest::binary>> = "öla"          
"öla"
iex(56)> var
<<195>>
iex(57)> rest
<<182, 108, 97>>

iex(58)> <<var::binary-2, rest::binary>> = "öla"
"öla"
iex(59)> var
"ö"
iex(60)> rest
"la"
```

An alternate form of the above is:
```Elixir
iex(52)> <<var::bitstring-24, rest::bitstring>> = "foobar"
"foobar"
iex(53)> var
"foo"
iex(54)> rest
"bar"
```



