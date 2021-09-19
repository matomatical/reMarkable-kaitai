reMarkable Kaitai Specs
=======================

The [reMarkable](https://remarkable.com/)
is a pretty cool e-ink tablet.
The tablet stores a notebook's pen strokes in binary files on the device
(`.rm` files, also called *lines* format).
For backup and/or conversion jobs, it can be helpful to parse this binary
format.

[Kaitai Struct](http://kaitai.io/)
is a declarative parser specification language for binary data formats,
and an accompanying parser generator.
Kaitai Struct specifications can be compiled to code for a parser in one
of various languages.

This repository contains a Kaitai Struct specification for some versions
of the reMarkable lines (`.rm`) format.

Notes
-----

This specification was made very quickly for fun, and it could probably
be improved. For example, it might be helpful to add some documentation
to the specification, and it might be an improvement to automatically
detect one of multiple versions of the format from the header, and parse
accordingly. Contributions welcome.

The specifications have only been tested superficially, on a single-layer
v5 lines document with strokes of a single brush type and size. To be honest
I haven't even rendered the output to check it makes sense.
The v3 spec has not been tested at all. Issues or corrections welcome.

The reMarkable lines format evolves as the reMarkable receives updates,
and this repository is probably not going to be kept up to date. Forks
are welcome.

However, at least for the time being, this project might serve as a useful
starting point for someone who wants to make the specification properly,
and it might save a little work if someone just wants a parser in a
Kaitai-supported language.


Contents
--------

* `rm_v5.ksy`---spec for reMarkable .lines format, version 5
  * `hello.rm`---example v5 lines binary file
* `rm_v3.ksy`---spec for reMarkable .lines format, version 3

TODO:

* `rm_v0.ksy`---spec for reMarkable .lines format, early version (no number)

Credits
-------

Time for an overly gratuitous thank you speech:

* Thanks to ax3l for documenting a
  [thorough exploration of the binary format](https://plasma.ninja/blog/devices/remarkable/binary/format/2017/12/26/reMarkable-lines-file-format.html),
  and for the
  [C++](https://github.com/ax3l/lines-are-beautiful)
  and
  [Rust](https://github.com/ax3l/lines-are-rusty)
  reference implementations of the parser.
* Thanks to reHackable's
  [awesome-reMarkable](https://github.com/reHackable/awesome-reMarkable)
  project, which brings together many great and open projects for enhancing
  the reMarkable notebook experience, and helped me find ax3l's work.
* Thanks to a [stackoverflow answer](https://stackoverflow.com/a/39827436)
  for informing me about Kaitai Struct, saving me from writing a parser in
  Python (I use Python too much, and should really branch out more).
* Kaitai Struct was super easy to pick up due to the great documentation and
  online IDE. Thanks,  for helping me feel like a hacker!
* Thanks to [reMarkable AS](https://remarkable.com/) for your awesome tablet.
  It is a technology that has an unquestionably positive impact on my life
  (and in case anyone hasn't noticed, that's saying something for a technology
  these days).

In case it's not clear, this repository is not affiliated with reMarkable AS.
