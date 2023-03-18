# AnxiousNano

This repository holds the projects used to build anxiousnano, an experimental website from a random human in the internet.

## Setup

```shell
rustup target install wasm32-unknown-unknown
cargo install wasm-server-runner
cargo install wasm-bindgen-cli
cargo install cargo-watch
```

## Wasm

```shell
cargo build --release --target wasm32-unknown-unknown
wasm-bindgen --out-dir ./out/ --target web ./target/
```

## Develop

- Run `cargo generate -p ./template -n project-name`
- Edit `project-name/Cargo.toml` to change `name="some project name"`
- Edit root `Cargo.toml` file to include the `project-name` into the `members=[]` property of the `[workspace]`
- Optionally, `cargo watch -cx "run --release --target wasm32-unknown-unknown"`
