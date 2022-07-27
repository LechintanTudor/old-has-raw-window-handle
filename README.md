# OldHasRawWindowHandleWrapper

Wrap any type that implements `HasRawWindowHandle` and `HasRawDisplayHandle`
from `raw-window-handle 0.5` in `OldHasRawWindowHandleWrapper` to get a type
that implements `HasRawWindowHandle` from `raw-window-handle 0.4`.

## Why?

So you can use crates that haven't yet updated to the latest version of
`has-raw-window-handle`.

## How?

* Add both versions of `raw-window-handle` in your `Cargo.toml` as such:
```toml
old-raw-window-handle = { package = "raw-window-handle", version = "0.4" }
raw-window-handle = "0.5"
```

* Copy the code from the `lib.rs` file somewhere in your project.
