# Karabiner Elements Custom Configurations

This repository contains custom keyboard mappings for [Karabiner Elements](https://karabiner-elements.pqrs.org/), a powerful keyboard customizer for macOS.

## Available Configurations

### 1. Accented Vowels (`accenti_vocali.json`)
Creates shortcuts for typing Italian accented vowels using simultaneous key presses.

**Mappings:**
- `a + 1` → à (grave accent)
- `a + 2` → á (acute accent)
- `e + 1` → è (grave accent)
- `e + 2` → é (acute accent)
- `i + 1` → ì (grave accent)
- `i + 2` → í (acute accent)
- `o + 1` → ò (grave accent)
- `o + 2` → ó (acute accent)
- `u + 1` → ù (grave accent)
- `u + 2` → ú (acute accent)

**Customization:**
- Change the vowel by modifying the `key_code` in the `simultaneous` array
- Change the number trigger (1 or 2) by modifying the second `key_code`
- Adjust timing sensitivity with `basic.simultaneous_threshold_milliseconds` (default: 65ms)
- Modify the accent type by changing the `to` array sequence

### 2. Caps Lock to Super Key (`caps_lock_to_super_key.json`)
Transforms Caps Lock into a powerful modifier key.

**Behavior:**
- Hold: Acts as `Control + Option + Shift` (super key)
- Tap: Types underscore (`_`)

**Customization:**
- Change the modifier combination in the `to` section by modifying `modifiers` array
- Change tap behavior by modifying `to_if_alone` → `key_code` and its modifiers
- Example: To make tap type hyphen instead: change `"key_code": "hyphen"` and remove the shift modifier

### 3. End Key to Folder Opener (`end_to_open_folder.json`)
Maps the End key to quickly open a specific folder in Finder.

**Behavior:**
- Press `End` → Opens `/Users/mattia/hub/%temp` in Finder

**Customization:**
- Change the target folder path in `shell_command`: `"shell_command": "open '/your/custom/path'"`
- Change the trigger key by modifying `from` → `key_code`
- Add multiple folder shortcuts by duplicating the manipulator block

### 4. Page Up/Down to Zoom (`pagUp_pagDown_to_zoom.json`)
Remaps Page Up/Down to zoom controls.

**Behavior:**
- `Page Up` → `⌘+` (zoom in)
- `Page Down` → `⌘-` (zoom out)

**Customization:**
- Change zoom in key: modify the first manipulator's `to` section
- Change zoom out key: modify the second manipulator's `to` section
- Use different trigger keys by changing `from` → `key_code`

### 5. Quick App Opener (`quick_app_opener.json`)
Launches applications with keyboard shortcuts using the super key combination.

**Behavior:**
- `Control + Option + Shift + M` → Opens Music app

**Customization:**
- Change the app: modify `shell_command`: `"shell_command": "open /Applications/YourApp.app"`
- Change the trigger key: modify `from` → `key_code` (currently `m`)
- Add more app shortcuts by duplicating the manipulator block with different keys
- For system apps, use: `/System/Applications/AppName.app`
- For user apps, use: `/Applications/AppName.app`

### 6. Tab to Command (`tab_to_command.json`)
Dual-purpose Tab key for enhanced workflow.

**Behavior:**
- Hold: Acts as `⌘ Command`
- Tap: Types `Tab`

**Customization:**
- Change hold behavior: modify `to` → `key_code`
- Change tap behavior: modify `to_if_alone` → `key_code`
- Example alternatives:
  - Hold for Control: `"key_code": "left_control"`
  - Hold for Option: `"key_code": "left_option"`

## Contributing

If you have helpful Karabiner Elements configurations like these, feel free to contribute! You can:

1. Fork this repository
2. Add your configuration file (`.json`) to the collection
3. Update this README with a description of your configuration and customization instructions
4. Submit a pull request

Contributions that improve existing configurations or add new useful mappings are always welcome!
