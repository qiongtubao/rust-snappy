Snappy
------

[![Build Status](https://travis-ci.org/JeffBelgum/rust-snappy.svg?branch=master)](https://travis-ci.org/JeffBelgum/rust-snappy) [![](http://meritbadge.herokuapp.com/snappy)](https://crates.io/crates/snappy)

[ Originally forked from https://github.com/thestinger/rust-snappy ]

Snappy bindings for Rust (as written in the [The Official Rust Book](https://doc.rust-lang.org/book/ffi.html).)

[Documentation](https://jeffbelgum.github.io/snappy/snappy/)

Usage
-----

Add this to your `Cargo.toml`:

```ini
[dependencies]
snappy = "0.4"
```

and this to your crate root:

```rust
extern crate snappy;
```

Installing Snappy
-----------------

* The Snappy C++ library can be installed on Mac OS X using homebrew
  ```brew install snappy```.
* If that library is not installed in the usual path, you can export
  the `LD_LIBRARY_PATH` and `LD_RUN_PATH` environment variables before
  issueing `cargo build`.
* Static linking can be requested by an `export SNAPPY_SYS_STATIC=1` prior
  to `cargo build`.
* As a fallback, this crate will try to compile the Snappy C++ library
  itself and statically link against it.  (This behavior can be
  enforced by an `export SNAPPY_SYS_STATIC_FROM_SOURCE=1` prior to
  `cargo build`.)
