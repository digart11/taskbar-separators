# Changelog

## 1.3.0

### Added

- Added separator targeting by application name
- Added `+` for before-target placement and `-` for after-target placement
- Added `+-` and `-+` for placing separators on both sides of a target
- Added prefix syntax support for both numeric positions and application names

### Improved

- App-name separators now follow applications when taskbar icons are reordered
- Improved application-name matching for Windows taskbar items
- Improved separator setting parsing and whitespace handling

### Fixed

- Fixed before-first placement for first-position targets

## 1.2.0

### Added

- Added support for Windows taskbar labels and uncombined application buttons
- Added accurate separator positioning for variable-width taskbar buttons
- Added support for mixed layouts across multiple monitors

### Improved

- Improved taskbar initialization and multi-monitor reconciliation
- Improved handling of separator settings containing empty or zero-valued entries
- Improved before-first separator handling when there is not enough layout information for reliable placement
- Refined internal margin tracking and cleanup

## 1.1.0

### Added

- Added configurable divider gap
- Added nine visual separator styles
- Added configurable separator thickness, length, opacity, and color
- Added optional separator before the first application button
- Added live settings updates
- Added vertical taskbar compatibility

## 1.0.0

### Added

- Initial release
- Added configurable visual separators between Windows 11 taskbar application buttons
- Added support for multiple separator positions
