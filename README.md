# ⚡ HUDForge Engine v1.0

> **A Portable, Standalone & Modular Ambient Screen Processing Framework for Windows**  
> Developed by **[LetsGoDada](https://github.com/LetsGoDada)**

---

## 📌 Overview

**HUDForge** is a high-performance, lightweight, and modular Desktop HUD framework built with Python and Tkinter. Designed for gamers, speedrunners, and power users, HUDForge allows you to seamlessly integrate custom real-time widgets, capture instant replays, display smooth multi-monitor ambient light gradients, and parse verified input logs.

It functions as a completely standalone executable (`HUDForge.exe`), while dynamically loading external modular plugins directly from your desktop runtime workspace.

---

## ✨ Key Features

- 💎 **Standalone & Portable:** Compiled as a single, console-less executable (`--onefile`, `--noconsole`).
- 🎨 **Global HUD Customizer:** Adjust app title, transparency (opacity slider), and dynamic dark-theme color palettes across all active tabs in real-time.
- 💡 **Screen Ambient Light Engine:** Zero-lag ambient capture using `mss`, `OpenCV`, and `NumPy` with bilinear interpolation for smooth multi-monitor gradient syncing.
- 🎬 **Insta Screenrecord (Instant Replay):** Continuously buffers screen footage in memory to capture and export the last 60 seconds with a configurable global hotkey (e.g., `F10`).
- ⚡ **TAS & Macro Timeline Editor:** Import, edit, and play back input macros. Integrates seamlessly with **Locked Legit Inputs (LLI)** logs.
- 🔴 **Universal Input Recorder:** Capture global keyboard and mouse events into verified LLI-compatible log files.
- 🌊 **Wave Overlay:** Launch a semi-transparent ambient wave animation visualizer.

---

## 🛠️ Ecosystem Integration: LLI (Locked Legit Inputs)

HUDForge is designed as the input-parsing backbone for **[Locked Legit Inputs (LLI)](https://github.com/LetsGoDada/Locked-Legit-Inputs)**. 

- **LLI Verification:** Import tamper-proof, timestamped physical input logs directly into the TAS Timeline Editor.
- **Local Editing:** Automatically converts LLI proofs into locally editable sequence files without modifying original source evidence.
- **Automated Playback:** Replay physical key actions with millisecond-accurate tick delays.

---

## 📂 Desktop Folder Structure

HUDForge runs as a single executable, but automatically initializes and reads custom modular scripts from your Desktop workspace upon execution:

```text
C:\Users\<YourUser>\Desktop\HUDForge\
├── HUDForge.exe               # Main Executable
├── plugins/                   # Top-Level Tab Plugins
│   ├── custom_tabs.py         # Sub-Notebook Manager for Custom Hub
│   ├── hud_customizer.py     # Global Theme & Opacity Settings
│   └── screen_ambient.py      # MSS Ambient Screen Engine
└── custom_widgets/            # Sub-Tab Widgets (Loaded inside Custom Hub)
    ├── screenrecord.py        # 1-Min Instant Replay Engine
    ├── tas_editor.py          # TAS & LLI Log Importer/Player
    ├── tas_recorder.py        # Universal Input Logger
    └── wave_app.py            # Wave Animation Overlay
