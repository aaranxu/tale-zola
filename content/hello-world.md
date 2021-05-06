+++
title = "Hello World"
date = 2021-05-01T11:11:00+00:00

[taxonomies]
tags = ["Rust", "Sample"]

[extra]
author = "Rustaceans"
+++

This is the source code of the traditional *Hello World* program.
<!-- more -->

```rust
// This is a comment, and is ignored by the compiler

// This is the main function
fn main() {
    // Statements here are executed when the compiled binary is called

    // Print text to the console
    println!("Hello World!");
}
```

`println!` is a macro that prints text to the console.

A binary can be generated using the Rust compiler: `rustc`.

```bash
$ rustc hello.rs
```

`rustc` will produce a `hello` binary that can be executed.

```bash
$ ./hello
Hello World!
```