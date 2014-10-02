15-150-DocGen
=============

Generate the documentation for homework solutions in CMU's 15-150 Functional Programming course.

Installation
============

```
git clone https://github.com/Alex4913/15-150-DocGen.git
cd 15-150-DocGen
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

It does not support absolute paths quite yet. I will do that very soon!
