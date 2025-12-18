# Caps Lock Language Switch (AutoHotkey v2)

Remap **Caps Lock** to **Left Alt + Shift** for switching input language on Windows.

Designed for people who type a lot and want fast, consistent language switching  
without wasting Caps Lock on uppercase mode.

---

## Features

- Caps Lock → Left Alt + Shift (change input language)
- Prevents Caps Lock from toggling uppercase
- Lightweight, no background service
- AutoHotkey v2 only

---

## Requirements

- Windows 10 / 11
- AutoHotkey **v2.x**

Download AutoHotkey v2:  
https://www.autohotkey.com/download/ahk-v2.exe

---

## Usage

1. Install AutoHotkey v2
2. Clone this repository or download the script
3. Run the script:

```powershell
capslock-lang-switch.ahk
```

Once running, pressing **Caps Lock** will switch the input language.

---

## Auto Start on Windows Startup (Manual – Recommended)

This method is simple, stable, and survives Windows updates.

### Step 1: Open Startup Folder

Press `Win + R`, then type:

```
shell:startup
```

Press Enter.

---

### Step 2: Create Shortcut

1. Right-click → **New → Shortcut**
2. Target:

```
"C:\path\to\capslock-lang-switch.ahk"
```

> Adjust the path to match your script location.

3. Click **Finish**

---

## Script

```ahk
CapsLock::
{
    KeyWait "CapsLock"
    SetCapsLockState("Off")
    Send("{LAlt down}{Shift}{LAlt up}")
}
```

---

## Notes

- Make sure Windows input language shortcut is set to **Left Alt + Shift**
- Do not run multiple AutoHotkey scripts that remap Caps Lock at the same time

---

## License

MIT License
