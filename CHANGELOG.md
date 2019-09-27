# Version master

## Breaking changes

- `sys` module is no longer public

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
