# okane-golden

[![CI](https://github.com/xkikeg/okane-golden/actions/workflows/ci.yml/badge.svg)](https://github.com/xkikeg/okane-golden/actions/workflows/ci.yml)
[![crates.io](https://img.shields.io/crates/v/okane-golden?style=flat-square)](https://crates.io/crates/okane-golden)

Library to support [Golden testing](https://en.wikipedia.org/wiki/Characterization_test), which compares the given text
against the pre-captured *golden* input. This library supports pretty much simple string golden testing.

```rust
let target = std::path::Path::new(env!("CARGO_MANIFEST_DIR")).join("testdata/mukai.txt");
let golden = okane_golden::Golden::new(target)?;
golden.assert("zazen boys\n");
```


For more details, see:
- [docs.rs](https://docs.rs/okane-golden/latest/okane_golden/)

This library is licensed under [Apache 2.0](../LICENSE) license.
