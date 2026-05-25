# rust-hello-world

A minimal Rust program that prints `Hello, world!`.

## Setup

These instructions assume you have **no Rust toolchain installed**. They cover macOS, Linux, and Windows.

### 1. Install platform build tools

Rust needs a system linker and C toolchain to produce binaries. Install these *before* running the Rust installer.

**macOS** — install the Xcode Command Line Tools (provides `cc`, `ld`, etc.):

```sh
xcode-select --install
```

A GUI prompt will appear; accept it and wait for the install to finish. If you've already installed them (or full Xcode), this is a no-op.

**Linux** — install a C compiler and `curl` via your distro's package manager:

```sh
# Debian / Ubuntu
sudo apt update && sudo apt install -y build-essential curl

# Fedora / RHEL
sudo dnf install -y gcc make curl

# Arch
sudo pacman -S --needed base-devel curl
```

**Windows** — install the **MSVC build tools** before running `rustup-init`. Either:

- Install [Visual Studio Build Tools](https://aka.ms/vs/17/release/vs_BuildTools.exe) and select the **Desktop development with C++** workload, **or**
- Let `rustup-init` install them for you when it prompts (recommended for new users).

### 2. Install Rust

The recommended installer is [`rustup`](https://rustup.rs), which manages the Rust compiler (`rustc`) and the build tool (`cargo`).

**macOS / Linux**

```sh
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

Follow the prompts (option `1` — default install — is fine). When it finishes, either restart your shell or load the new environment into the current one:

```sh
source "$HOME/.cargo/env"
```

**Windows**

Download and run the installer from <https://rustup.rs>. Follow the prompts (the default option is fine), then open a new terminal so `cargo` is on your `PATH`.

### 3. Verify the installation

```sh
rustc --version
cargo --version
```

Both commands should print a version number. This project was verified with `rustc 1.95.0` / `cargo 1.95.0`, but any recent stable toolchain should work.

### 4. Clone the repo

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
