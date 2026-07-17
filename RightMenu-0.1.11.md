
### Added

- Added an optional Desktop-location **Hide Desktop Items** command above
  Refresh on both the wallpaper and the Desktop folder background.
- The command changes to **Show Desktop Items** after hiding desktop files, so
  the same desktop context menu can restore them.
- Added a Settings toggle that independently shows or hides the new command.

### Changed

- Desktop visibility now records a recovery bookmark before applying Finder's
  hidden metadata to each visible Desktop item. It restores only items changed
  by RightMenu, keeps newly added items hidden with an event-driven listener,
  and never moves, renames, or deletes files.
- Finder's desktop layer remains active while items are hidden, preserving the
  native wallpaper context menu across Show Desktop, multiple Spaces, and
  different per-Space wallpapers.
- RightMenu restores changed items on normal quit and automatically recovers an
  interrupted hide session on the next launch.
- The Hide or Show command is available from both the wallpaper background and
  a Finder window opened at the Desktop folder, providing a recovery entry
  where the hidden contents are being viewed.
- Finder extension state is resynchronized from the host after each change,
  keeping the desktop command title and Settings-controlled menus consistent.

### Fixed

- Compiler-gated the macOS 26 Liquid Glass toolbar customization so macOS 15
  SDK builds keep the legacy toolbar path instead of failing on an unknown
  SwiftUI modifier.

