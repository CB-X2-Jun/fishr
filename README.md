# fishr - ><> interpreter

![Rust](https://github.com/CB-X2-Jun/fishr/actions/workflows/rust.yml/badge.svg)

This is an interpreter for the [Fish esoteric language](https://esolangs.org/wiki/Fish), originally created by [Marc Noirot](https://github.com/noirotm/fishr).

It is written in Rust and aims to be a fast and safe program. 

## 📦 Installation

> ⚠️ **Note:** The npm package currently bundles a pre-compiled binary for **Linux x64** only (optimized for GitHub Actions runners). For macOS/Windows, please compile from source using Cargo.

### via npm (binaries & examples)
```bash
npm install -g @cb-x2-jun/fishr
```
*Note: Even though the package is scoped, the CLI command remains simply `fishr`.*

### via Cargo (From Source)
If you want to compile it yourself, you need Rust 1.85+ (Rust 2024 Edition) installed:
```bash
git clone https://github.com/CB-X2-Jun/fishr.git
cd fishr
cargo build --release
# The binary will be located at target/release/fishr
```

## 🚀 Usage

You can run a `.fish` script directly, or pass code via command line.

**Execute a file:**
```bash
fishr examples/hello.fish
# Output: hello world
```

**Execute a string of code directly:**
```bash
fishr -c '"hello world"0r!/:?\;
                \ o/'
```

## 📁 Examples Included

We have included the original `examples/` directory in the npm package. You can easily test them out:

```bash
fishr examples/fizzbuzz.fish
fishr examples/factorial.fish
fishr examples/quine.fish
```

## 🛠️ Flags & Options

- `-c, --code <CODE>` : Execute a string of instructions instead of a file.
- `-s, --string <STR>` : Push strings onto the stack before execution starts.
- `-v, --value <NUM>` : Push numbers onto the stack before execution starts.
- `-t, --tick <SEC>` : Define a delay between the execution of each instruction.
- `-d, --debug` : Dump interpreter state before executing an instruction.

## 📄 License

This project is licensed under the MIT License.   
Original Copyright © 2017 [Marc Noirot](https://github.com/noirotm).  
Modifications Copyright © 2026 [CB-X2-Jun](https://github.com/CB-X2-Jun).  
