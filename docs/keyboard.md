# Keyboard Configuration

**RePlayOS** was designed to make the keyboard function like the original hardware on systems that natively support it, such as microcomputers. Consequently, the keyboard's primary functionality is UI navigation and integration with core emulators that support this mode.

**NOTE**: the keyboard does not emulate or function as a gamepad when used with console or arcade games.

The system offers two function modes, which can be selected via `SYSTEM > INPUT > KEYBOARD REAL MODE`:

- `ON`: The keyboard behaves like the original hardware while also supporting UI navigation.  
- `OFF`: The keyboard operates in a special hotkey command mode while still supporting UI navigation.

You can also select several of the below hotkeys for opening/closing the UI menu from `SYSTEM > INPUT > KEYBOARD MENU KEY`.

## Default UI Key Mapping

| Key                                        | Description    |
| ------------------------------------------ | -------------- |
| <kbd>Up</kbd> <kbd>Down</kbd>              | Used for moving up and down through the menus |
| <kbd>Left</kbd> <kbd>Right</kbd>           | Used for jumping forward and backward thorugh the menu pages |
| <kbd>Page Up</kbd> <kbd>Page Down</kbd>    | Used for jumping forward and backward to the next letter thorugh the menu pages |
| <kbd>Backspace</kbd>                       | Used to navigate to the previous menu or screen |
| <kbd>Return</kbd>                          | Used for starting games, choosing options, and accessing menus |
| <kbd>R Shift</kbd> <kbd>L Shift</kbd>      | Functions as the gamepad Select button (delete favorite/recent) |
| <kbd>Space</kbd>                           | Functions as the gamepad Start button |
| <kbd>Tab</kbd>                             | Hotkey for opening MAME native config menu (only works in real mode) |
| <kbd>H</kbd>                               | Hotkey for system halt (useful for taking real photos) |
| <kbd>S</kbd>                               | Hotkey for taking screenshots |
| <kbd>Mute</kbd> <kbd>M</kbd>               | Hotkey for toggling system mute |
| <kbd>Volume Up</kbd> <kbd>Keypad +</kbd>   | Hotkey for increasing system volume |
| <kbd>Volume Down</kbd> <kbd>Keypad -</kbd> | Hotkey for decreasing system volume |
| <kbd>R Windows</kbd> <kbd>L Windows</kbd>  | Hotkey for opening/closing the UI menu |
| <kbd>Play/Pause</kbd>                      | Hotkey for opening/closing the UI menu |
| <kbd>Home Page</kbd>                       | Hotkey for opening/closing the UI menu |
| <kbd>Home</kbd>                            | Hotkey for opening/closing the UI menu |
| <kbd>Caps Lock</kbd>                       | Hotkey for toggling Keyboard Real mode ON/OFF |

## Key Remapping (example **Right Ctrl → Right Super**)

### Software method with `keyd`

```bash
apt update
apt install keyd
systemctl enable --now keyd
mkdir -p /etc/keyd
nano /etc/keyd/default.conf
```

Config:

```ini
[ids]
*

[main]
rightcontrol = rightmeta
```

Apply:

```bash
systemctl restart keyd
```

### Firmware method on Pi 500 / Pi 500+

```bash
apt update
apt install rpi-keyboard-config
```

Find Right Ctrl position:

```bash
rpi-keyboard-config info --ascii
```

List keycodes:

```bash
rpi-keyboard-config list-keycodes
```

Look for the right Super/GUI keycode, likely:

```text
KC_RGUI
```

Unlock:

```bash
rpi-keyboard-config unlock
```

Set Right Ctrl’s row/column to Right GUI. Replace `<row>` and `<column>` with the coordinates shown for **Right Ctrl**:

```bash
rpi-keyboard-config key set <row> <column> KC_RGUI
```

Lock:

```bash
rpi-keyboard-config lock
```

Reset if needed:

```bash
rpi-keyboard-config reset-keymap
```
