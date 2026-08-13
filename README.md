# Taskbar Separators

Add clean, customizable visual separators between application buttons on the
Windows 11 taskbar.

Unlike placeholder applications or pinned shortcuts, these separators are
visual, non-clickable elements. They do not launch programs or occupy normal
application slots.

## Preview

![Taskbar Separators
preview](https://raw.githubusercontent.com/digart11/taskbar-separators/master/images/taskbar-separators-preview.jpg)

## Features

* Add multiple separators at configurable taskbar positions
* Optional separator before the first application button
* Live position and appearance updates
* Nine configurable visual styles:

  * Fade
  * Solid
  * Double
  * Rounded
  * Glow
  * Dot
  * Ring
  * Square
  * Diamond
* Adjustable physical divider gap, thickness, length, opacity, color, and effect settings
* Physical divider gaps create real layout space between neighboring taskbar buttons
* Existing taskbar button margins are preserved and the divider gap is added on top of them
* Improved positioning after taskbar button drag/reorder
* Pixel-aligned divider positioning for more consistent rendering
* Automatic horizontal and vertical taskbar orientation
* Optional animation compatibility mode
* Clean removal of divider visuals and added spacing when the mod is disabled

## Getting started

1. Open the mod's **Settings** tab.
2. Add separator positions to the **Separators** list.
3. A position of `3` places a separator after the third application button.
4. Select a style and adjust its appearance.
5. Use **Divider Gap** to reserve additional physical space around configured separators.

## Position behavior

Numbered positions place separators after application buttons:

* Position `1` places a separator after the first application button
* Position `2` places a separator after the second application button
* Position `3` places a separator after the third application button

Enable **Separator before first app** to place a separator before the first
application button.

Start, Search, Widgets, Task View, and other system buttons are not counted as
application buttons.

Positions follow the current visual order of taskbar application buttons.
Opening, closing, pinning, unpinning, or rearranging applications can change
which icons appear beside a configured separator.

## Divider gap

The **Divider Gap** setting reserves additional physical space at each configured
separator position.

The gap is applied only where separators exist. It does not globally increase
the spacing between all taskbar buttons.

Existing taskbar button margins are preserved, allowing the gap to work alongside
normal Windows layout values and compatible taskbar styling mods.

Set **Divider Gap** to `0` to use the original overlay-only behavior.

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

* Windows 11 horizontal taskbars
* Vertical taskbars via Vertical Taskbar for Windows 11
* Compatible with Windows 11 Taskbar Styler in normal configurations
* Physical divider gaps are layered on top of existing taskbar button margins

## License and attribution

Licensed under the GNU General Public License v3.0.

Taskbar hook and UI-thread infrastructure includes code and patterns adapted
from Windhawk mods by Michael Maltsev (m417z), including Taskbar Labels for
Windows 11, Taskbar Multirow, and Windows 11 Taskbar Styler.
