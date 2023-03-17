# AnxiousNano

This repository holds the projects used to build anxiousnano, an experimental website from a random human in the internet.

## Setup

To build this project, apart from assuming `cargo` is installed, it's necessary to have a few other things installed to run the code in wasm:

```shell
rustup target install wasm32-unknown-unknown
cargo install wasm-server-runner
cargo install wasm-bindgen-cli
```

## Wasm

```shell
cargo build --release --target wasm32-unknown-unknown
wasm-bindgen --out-dir ./out/ --target web ./target/
```