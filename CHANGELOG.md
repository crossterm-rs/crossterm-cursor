# Version 0.4.0

- Internal refactoring ([PR #2](https://github.com/crossterm-rs/crossterm-cursor/pull/2))
  - Improved public documentation
  - `sys` module is no longer public
- Fixed examples link ([PR #6](https://github.com/crossterm-rs/crossterm-cursor/pull/6))
- Sync documentation style ([PR #7](https://github.com/crossterm-rs/crossterm-cursor/pull/7))
- Removed all references to the crossterm book ([PR #8](https://github.com/crossterm-rs/crossterm-cursor/pull/8))
- Replaced `RAW_MODE_ENABLED` with `is_raw_mode_enabled` ([PR #9](https://github.com/crossterm-rs/crossterm-cursor/pull/9))
- Use `SyncReader` & `InputEvent::CursorPosition` for `pos_raw()` ([PR #10](https://github.com/crossterm-rs/crossterm-cursor/pull/10))

# Version 0.3.1

- Maintenance release only
- Moved to a [separate repository](https://github.com/crossterm-rs/crossterm-cursor)

# Version 0.3.0

- `TerminalCursor::pos()` returns `crossterm::Result<(u16, u16)>`
- `TerminalCursor::move_*` returns `crossterm::Result`
- `TerminalCursor::reset_position()` to `restore_position()`
- All `i16` values for indexing: set/get cursor pos synced to `u16` values
- `Command::get_anis_code()` to `ansi_code()`
- `ExecutableCommand::queue` returns `crossterm::Result`
- `QueueableCommand::queue` returns `crossterm::Result`
- Command API takes mutable self instead of self

# Version 0.2.0

- Removed `TerminalCursor::from_output()` 

# Version 0.1.0
 
- Moved out of `crossterm` 5.4 crate. 
