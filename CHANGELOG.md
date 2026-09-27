# Changelog

All notable changes are documented here.
Format follows keepachangelog.com, versions are semver-ish.

## [0.4.3] - 2026-08-21

### Fixed
- wrong exit code on partial failures
- off-by-one in the summary counter

### Changed
- faster directory walking, fewer syscalls

## [0.3.0] - 2026-06-04

### Added
- atomic saves (temp file + os.replace) behind a write lock

## [0.2.0] - 2026-06-18

### Added
- atomic saves (temp file + os.replace) behind a write lock

## [0.1.0] - 2026-04-07

### Added
- first working version
