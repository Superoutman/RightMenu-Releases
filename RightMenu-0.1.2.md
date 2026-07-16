
### Added

- Added the public `RightMenu-Releases` repository for the Sparkle feed and downloadable update archive.
- Added tag-triggered GitHub Actions publishing from the private source repository.
- Added repository-scoped Deploy Key publishing and encrypted Sparkle signing-key storage.

### Changed

- The app now reads its update feed from the public release repository.
- Version metadata now has a shared command-line source in `Configuration/Version.env`.
- Ordinary source pushes do not publish updates; only matching `v*` tags trigger publishing.

### Distribution note

- Automated builds remain ad-hoc signed until Developer ID signing and Apple notarization credentials are configured.

