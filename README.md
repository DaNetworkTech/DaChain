# Decentralized Autonomous Network BlockChain

Fast and feature-rich multi-network Decentralized Autonomous Network client. Forked from openethereum.

[» Download the latest DAClient release «]



## 1. Description 

**Built for mission-critical use**: Miners, service providers, and exchanges need fast synchronisation and maximum uptime. OpenEthereum provides the core infrastructure essential for speedy and reliable services.

- Clean, modular codebase for easy customisation
- Advanced CLI-based client
- Minimal memory and storage footprint
- Synchronise in hours, not days with Warp Sync
- Modular for light integration into your service or product

## 2. Technical Overview 

DA-Client's goal is to be the fastest, lightest, and most secure chain client. We are developing DA-Client using the **Rust programming language**. DA-Client is licensed under the GPLv3 and can be used for all your Ethereum needs.

By default, OpenEthereum runs a JSON-RPC HTTP server on port `:8545` and a Web-Sockets server on port `:8546`. This is fully configurable and supports a number of APIs.


## 3. Building 

### 3.1 Build Dependencies

DA-Client requires **latest stable Rust version** to build.

We recommend installing Rust through [rustup](https://www.rustup.rs/). If you don't already have `rustup`, you can install it like this:

- Linux:
  ```bash
  $ curl https://sh.rustup.rs -sSf | sh
  ```

  DA-Client also requires `clang` (>= 9.0), `clang++`, `pkg-config`, `file`, `make`, and `cmake` packages to be installed.

- OSX:
  ```bash
  $ curl https://sh.rustup.rs -sSf | sh
  ```

  `clang` is required. It comes with Xcode command line tools or can be installed with homebrew.

- Windows:
  Make sure you have Visual Studio 2015 with C++ support installed. Next, download and run the `rustup` installer from
  https://static.rust-lang.org/rustup/dist/x86_64-pc-windows-msvc/rustup-init.exe, start "VS2015 x64 Native Tools Command Prompt", and use the following command to install and set up the `msvc` toolchain:
  ```bash
  $ rustup default stable-x86_64-pc-windows-msvc
  ```

Once you have `rustup` installed, then you need to install:
* [Perl](https://www.perl.org)
* [Yasm](https://yasm.tortall.net)

Make sure that these binaries are in your `PATH`. After that, you should be able to build OpenEthereum from source.

### 3.2 Build from Source Code <a id="chapter-0032"></a>

```bash
# download DA-Client code
$ git clone https://github.com/DaNetworkTech/DaChain
$ cd DaChain

# build in release mode
$ cargo build --release --features final
```

This produces an executable in the `./target/release` subdirectory.

Note: if cargo fails to parse manifest try:

```bash
$ ~/.cargo/bin/cargo build --release
```

Note, when compiling a crate and you receive errors, it's in most cases your outdated version of Rust, or some of your crates have to be recompiled. Cleaning the repository will most likely solve the issue if you are on the latest stable version of Rust, try:

```bash
$ cargo clean
```

This always compiles the latest nightly builds. If you want to build stable, do a

```bash
$ git checkout stable
```

### 3.3 Starting DA-Client

#### Manually

To start OpenEthereum manually, just run

```bash
$ ./target/release/dachain
```


