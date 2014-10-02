SML-DocGen
=============

Disclaimer
----------

This is purely for personal use. I assume no liability for the use of this program on an
actual homework assignment, rather the intent is for use on personal code. Please see the
LISCENCE file.

Generate the documentation for SML files, following the standards set forth within CMU's
15-150 Functional Programming course.

It takes the following SML function declaration:
```
fun fact(0 : int) : int = 1
  | fact(n : int) : int = n * fact(n - 1)
```
and transforms it to this:
```
(*
    fact : int -> int
    REQUIRES: true
    ENSURES: fact
*)
fun fact(0 : int) : int = 1
  | fact(n : int) : int = n * fact(n - 1)
```

Installation
============

```
git clone https://github.com/Alex4913/SML-DocGen.git
cd SML-DocGen
chmod +x docgen
```

I would highly suggest moving `docgen` into your personal `bin` directory,
so that you can access it anywhere. On Andrew Unix, this is:
```
cp docgen ~/bin
```

Usage
=====

For modifying in the same directory
```
./docgen my-sml-file.sml
```

Or, if you installed it into `~/bin`
```
docgen my-sml-file.sml
```

`docgen` supports wildcards, multiple files passed in. It writes to
`my-sml-file.sml.tmp` when it completes, next to where the old file is.
It will overwrite any previous versions.

The Future
==========

It does not support absolute paths quite yet. Nor does it give templates
for test functions. These will be added in the future.
