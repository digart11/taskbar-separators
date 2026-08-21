# Taskbar Separators

Add clean, customizable visual separators between application buttons on the
Windows 11 taskbar.

Unlike placeholder applications or pinned shortcuts, these separators are
visual, non-clickable elements. They do not launch programs or occupy normal
application slots.

Current release: **1.3.0**.

## Preview
![Taskbar Separators
preview](https://raw.githubusercontent.com/digart11/taskbar-separators/master/images/taskbar-separators-preview.jpg)


## Features

- Add multiple separators at configurable taskbar positions
- Target separators by taskbar position or application name
- App-name separators follow applications when taskbar icons are reordered
- Optional separator before the first application button
- Live position and appearance updates
- Nine configurable visual styles:
  - Fade
  - Solid
  - Double
  - Rounded
  - Glow
  - Dot
  - Ring
  - Square
  - Diamond
- Correct separator positioning for taskbar labels and uncombined or otherwise
variable-width buttons
- Supports mixed multi-monitor layouts, such as labels on one taskbar and
icon-only buttons on another

## What's new in 1.3.0
- Added separator targeting by application name, based on a contribution from
  `mileso` in PR #2
- App-name separators now follow their application when taskbar icons are reordered
- Added `+` for before-target placement and `-` for after-target placement
- Added `+-` and `-+` for placing separators on both sides of a target
- Prefix syntax works with both numeric positions and application names
- Improved application-name matching for Windows taskbar items
- Improved separator setting parsing and whitespace handling
- Fixed before-first placement for first-position targets

## What's new in 1.2.0
- Added support for Windows taskbar labels and uncombined application buttons
- Added accurate separator positioning for variable-width taskbar buttons
- Added support for mixed layouts across multiple monitors, such as labels on
one taskbar and icon-only buttons on another
- Improved taskbar initialization and multi-monitor reconciliation
- Improved handling of separator settings containing empty or zero-valued entries
- Improved before-first separator handling when there is not enough layout information for reliable placement
- Refined internal margin tracking and cleanup


## Getting started

1. Open the mod's **Settings** tab.
2. Add taskbar positions or application names to the **Separators** list.
3. For example, `3` places a separator after the third application button,
   while `+Notepad` places one before Notepad.
4. Select a style and adjust its appearance.
5. Use **Divider gap** to reserve additional physical space around configured separators.

## Position behavior

Separators can target either a taskbar position or a specific application.

Placement prefixes:

- `+` = before
- `-` = after
- `+-` or `-+` = before and after

Examples:

- `+2` places a separator before the second application button
- `-3` places a separator after the third application button
- `+-3` places separators before and after the third application button
- `+Notepad` places a separator before Notepad
- `-Notepad` places a separator after Notepad
- `+-Notepad` places separators before and after Notepad

Plain values such as `3` or `Notepad` continue to place the separator after the target.

Application-name separators follow the matching application when its taskbar icon is reordered.

Enable **Separator before first app** to place a separator before the first application button.

Start, Search, Widgets, Task View, and other system buttons are not counted as application buttons.


## Divider gap

The **Divider gap** setting reserves additional physical space at each
configured separator position.

The gap is applied only where separators exist. It does not globally increase
the spacing between all taskbar buttons.

Existing taskbar button margins are preserved, allowing the gap to work
alongside normal Windows layout values and compatible taskbar styling mods.

Set **Divider gap** to `0` to use overlay-only separator positioning without
adding physical spacing.

## Settings

![Taskbar Separators
settings](https://raw.githubusercontent.com/digart11/taskbar-separators/master/images/taskbar-separators-settings.jpg)

## Alternate setups

![Taskbar Separators alternate
setups](https://raw.githubusercontent.com/digart11/taskbar-separators/master/images/taskbar-separators-alt.jpg)

## Animation compatibility

Static taskbars are fully supported.

The mod can follow icons animated by other taskbar mods, but very fast animation
may not remain perfectly synchronized because both mods update their visual
elements independently.

This affects animation appearance only and does not affect normal static
separator positioning.

## Compatibility

- Windows 11 horizontal taskbars
- Vertical taskbars via Vertical Taskbar for Windows 11
- Compatible with Windows 11 Taskbar Styler in normal configurations
- Taskbar labels and uncombined or otherwise variable-width taskbar buttons
- Mixed multi-monitor layouts with different button modes on each taskbar
- Physical divider gaps are layered on top of existing taskbar button margins

## License and attribution

Licensed under the GNU General Public License v3.0.

Taskbar hook and UI-thread infrastructure includes code and patterns adapted
from Windhawk mods by Michael Maltsev (m417z), including Taskbar Labels for
Windows 11, Taskbar Multirow, and Windows 11 Taskbar Styler.