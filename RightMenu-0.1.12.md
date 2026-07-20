
### Added

- Added a copyable information line for a single selected Finder file, with the
  file size displayed last.
- Images additionally show their pixel dimensions and embedded horizontal and
  vertical DPI values. Missing DPI metadata is omitted instead of inferred.

### Changed

- The Finder extension reads indexed image metadata through CoreServices and
  gives the local host a timeout-bounded opportunity to read lightweight image
  metadata before returning the first contextual menu.
- Added a fail-closed recovery guard: unvalidated future macOS major versions
  and interrupted information-menu builds suppress the new information line
  without removing the existing Copy File Path command.
- The Command Line Tools build now links the system CoreServices, ImageIO, and
  Uniform Type Identifiers frameworks used by the Finder extension.

