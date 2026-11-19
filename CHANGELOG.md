# Changelog

## Unreleased

### Added
- README in English with all labs, CLAUDE.md, changelog and ADRs

### Fixed
- Lab 1 `script.sh`: an interrupted build left its temp folder behind (the `trap` lacked a `$`)
