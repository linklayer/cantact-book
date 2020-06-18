# CANtact Command Line Interface

The CANtact Command Line Interface (CLI) is a cross-platform tool with basic CAN functionality. 
These can be used to send and receive frames on Windows, macOS, and Linux.

## Building the CLI

Building the CLI requires Rust, which can be installed using [rustup](https://rustup.rs/).

Once Rust is installed, install CANtact using `cargo`.

```
cargo install cantact
```

## Running the CLI

The CLI provides a single binary named `can`. To get help, run `can --help`.