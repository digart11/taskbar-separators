# Taskbar Separators development rules

This is a Windhawk C++ mod targeting explorer.exe on Windows 11 24H2.

Safety:
- Never modify taskbar width, margin, or parent layout during a layout callback.
- Never add repeated visual elements without checking for an existing named element.
- All XAML visual-tree changes must occur on the taskbar XAML/UI thread.
- The mod must restore every changed or inserted element when disabled.
- Do not add settings until enable/disable lifecycle is reliable.
- Do not invent undocumented hooks when a proven pattern exists in the reference mod.
- Preserve compilable Windhawk metadata.
- Make one focused change at a time.
- Explain the cause of a bug before editing.
- Review the diff for lifecycle and re-entrancy problems.

Reference:
- references/taskbar-labels.wh.cpp is known-working Windhawk taskbar code.
- Reuse its proven initialization, refresh, UI-thread dispatch, and unload patterns where applicable.
- Do not retain unrelated taskbar-label functionality.

Current milestone:
One persistent thin divider after taskbar app button 3 that appears on enable and is fully removed on disable.