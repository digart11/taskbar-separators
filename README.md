# Taskbar Separators

Add clean, customizable visual separators between application buttons on the
Windows 11 taskbar.

Unlike placeholder applications or pinned shortcuts, these separators are
visual, non-clickable elements. They do not launch programs or occupy normal
application slots.

Current release: **1.2.0**.

## Preview

![Taskbar Separators
preview](https://raw.githubusercontent.com/digart11/taskbar-separators/master/images/taskbar-separators-preview.jpg)

## Features

- Add multiple separators at configurable taskbar positions
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

- Correct separator positioning for taskbar labels and uncombined or otherwise variable-width buttons
- Supports mixed multi-monitor layouts, such as labels on one taskbar and icon-only buttons on another

## What's new in 1.2.0

- Added support for Windows taskbar labels and uncombined application buttons
- Added accurate separator positioning for variable-width taskbar buttons
- Added support for mixed layouts across multiple monitors, such as labels on one taskbar and icon-only buttons on another
- Improved taskbar initialization and multi-monitor reconciliation
- Improved handling of separator settings containing empty or zero-valued entries
- Improved before-first separator handling when there is not enough layout information for reliable placement
- Refined internal margin tracking and cleanup

![Taskbar Separators 1.2.0 with taskbar labels](https://raw.githubusercontent.com/digart11/taskbar-separators/master/images/taskbar-separators-labels.jpg)

## Getting started

1. Open the mod's **Settings** tab.
2. Add separator positions to the **Separators** list.
3. A position of `3` places a separator after the third application button.
4. Select a style and adjust its appearance.
5. Use **Divider gap** to reserve additional physical space around configured separators.

## Position behavior

Numbered positions place separators after application buttons:

- Position `1` places a separator after the first application button-
- Position `2` places a separator after the second application button
- Position `3` places a separator after the third application button

Enable **Separator before first app** to place a separator before the first
application button.

Start, Search, Widgets, Task View, and other system buttons are not counted as
application buttons.

Positions follow the current visual order of taskbar application buttons.
Opening, closing, pinning, unpinning, or rearranging applications can change
which icons appear beside a configured separator.

## Divider gap

The **Divider gap** setting reserves additional physical space at each configured
separator position.

The gap is applied only where separators exist. It does not globally increase
the spacing between all taskbar buttons.

Existing taskbar button margins are preserved, allowing the gap to work alongside
normal Windows layout values and compatible taskbar styling mods.

Set **Divider gap** to `0` to use the original overlay-only behavior.

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
