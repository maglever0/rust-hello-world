# rust-hello-world

A minimal Rust program that prints `Hello, world!`.

## Setup

These instructions assume you have **no Rust toolchain installed**. They cover macOS, Linux, and Windows.

### 1. Install Rust

The recommended installer is [`rustup`](https://rustup.rs), which manages the Rust compiler (`rustc`) and the build tool (`cargo`).

**macOS / Linux**

```sh
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

Follow the prompts (the default option is fine). When it finishes, either restart your shell or load the new environment into the current one:

```sh
source "$HOME/.cargo/env"
```

**Windows**

Download and run the installer from <https://rustup.rs>. Follow the prompts (the default option is fine), then open a new terminal so `cargo` is on your `PATH`.

### 2. Verify the installation

```sh
rustc --version
cargo --version
```

Both commands should print a version number.

### 3. Clone the repo

```sh
git clone https://github.com/maglever0/rust-hello-world.git
cd rust-hello-world
```

## Run it

```sh
cargo run
```

You should see:

```
Hello, world!
```

## Build a release binary (optional)

```sh
cargo build --release
./target/release/rust-hello-world
```
