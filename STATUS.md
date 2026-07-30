# Current status

System:
- Windows 11 24H2
- OS build 26100.8875
- Windhawk 1.7.3
- Taskbar Styler is also enabled

Proven:
- TaskListButton::UpdateVisualStates hook works.
- Taskbar buttons can be counted by position.
- A divider can be added after app button 3.
- A separate Rectangle overlay remains visible during hover.
- Changing taskbar layout from a layout callback caused an Explorer feedback loop.

Current bugs:
- Divider is not created immediately until a button visual-state update occurs.
- Divider remains after disabling the mod.
- Cleanup attempts from Wh_ModBeforeUninit have not worked.
- Do not change width or margin yet.

Immediate goal:
- One thin divider after button 3.
- Appears immediately when enabled.
- Disappears immediately when disabled.
- No Explorer restart.
- No taskbar layout callback.
- No settings yet.