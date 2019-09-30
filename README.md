![Lines of Code][s7] [![Latest Version][s1]][l1] [![MIT][s2]][l2] [![docs][s3]][l3] [![Join us on Discord][s5]][l5]

# Crossterm Cursor

This crate allows you to work with the terminal cursor. It supports all UNIX and Windows terminals down
to Windows 7 (not all terminals are tested, see the
[Tested Terminals](https://github.com/crossterm-rs/crossterm/blob/master/README.md#tested-terminals) for more info).

`crossterm_cursor` is a sub-crate of the [crossterm](https://crates.io/crates/crossterm) crate. You can use it
directly, but it's **highly recommended** to use the [crossterm](https://crates.io/crates/crossterm) crate with
the `cursor` feature enabled (see [feature flags](https://crossterm-rs.github.io/crossterm/docs/feature_flags.html)
for more info).

## Future

> The `crossterm_cursor` crate code will be moved to the `crossterm` crate (it's reexported there now).
> Date is not set yet, but it doesn't make a lot of sense to start a new project with it. Please, use
> the `crossterm` crate with the `cursor` feature enabled.

Issues in this repository are disabled for the same reason. Please, report all issues in the
[crossterm-rs/crossterm](https://github.com/crossterm-rs/crossterm/issues) repository.

## Features

- Cross-platform
- Multi-threaded (send, sync)
- Detailed documentation
- Few dependencies
- Cursor
  - Move the cursor N times (up, down, left, right)
  - Set/get the cursor position
  - Store the cursor position and restore to it later
  - Hide/show the cursor
  - Enable/disable cursor blinking (not all terminals do support this feature)

## Getting Started

<details>
<summary>
Click to show Cargo.toml.
</summary>

```toml
[dependencies]
# All crossterm features are enabled by default.
crossterm = "0.11"
```

</details>
<p></p>

```rust
use std::io::{stdout, Write};  
use crossterm::{execute, Goto, Result};

fn main() -> Result<()> {
    execute!(stdout(), Goto(10, 10))
}
```

It's recommended to use the [Command API](https://crossterm-rs.github.io/crossterm/docs/command.html),
because this might replace some of the existing API in the future. It is more convenient, faster and
easier to use.

## Other Resources

- [API documentation](https://docs.rs/crossterm_cursor/) (with other examples)
- [Examples repository](https://github.com/crossterm-rs/examples)
- [The Book](https://crossterm-rs.github.io/crossterm/docs/index.html)
   
## Authors

* **Timon Post** - *Project Owner & creator*

## License

This project is licensed under the MIT License - see the [LICENSE](./LICENSE) file for details

[s1]: https://img.shields.io/crates/v/crossterm_cursor.svg
[l1]: https://crates.io/crates/crossterm_cursor

[s2]: https://img.shields.io/badge/license-MIT-blue.svg
[l2]: ./LICENSE

[s3]: https://docs.rs/crossterm_cursor/badge.svg
[l3]: https://docs.rs/crossterm_cursor/

[s5]: https://img.shields.io/discord/560857607196377088.svg?logo=discord
[l5]: https://discord.gg/K4nyTDB

[s7]: https://travis-ci.org/crossterm-rs/crossterm.svg?branch=master
