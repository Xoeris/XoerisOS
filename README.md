# XoerisOS2

<img width="200" height="27" alt="XoerisOS4 Logo Text" src="https://github.com/user-attachments/assets/4124aeee-1af2-4d31-81cb-c0838a7ad5b4" />


#### _Clean. Fast. Maximum._

XoerisOS2 is a lightweight Android-based operating system focused on performance optimization, system stability, deep UI customization, and clean integration for development environments.

---

## Overview

XoerisOS2 is designed to provide a minimal, highly customizable, and efficient base suitable for developers, kernel engineers, and advanced Android users. The system emphasizes clarity in configuration, smooth SystemUI animations, real-time hardware monitoring, and generic kernel compatibility.

---

## Technical Features & Changelog (v1.0 - v2.0)

XoerisOS2 brings massive upgrades to the SystemUI framework, layout stability, and performance tracking. Below is the complete feature set implemented up to the latest release:

### 🌟 SystemUI & Layout Optimizations (v2.0 Latest)
*   **Vertical Dual Row Signal Layout Fix**: Completely corrected the dual-row SIM layout horizontal spacing bug. Single-row mobile indicators now transition to a `GONE` visibility state when dual-row signal is toggled, letting the vertically stacked primary/secondary indicators take over layout bounds correctly.
*   **Dynamic Sibling View Container Detection**: Refactored `DualRowSignalController` to dynamically traverse sibling `ModernStatusBarMobileView` children inside the status bar's parent icon container, ensuring the second SIM is correctly identified and disabled to prevent duplicate rows.
*   **MIUI Elastic Spring Overscroll Support**: Integrated MIUI's `miuix.springback.view.SpringBackLayout` wrapper around the custom **About** (Powered by) and **System Changelogs** screens, enabling the native elastic spring overscroll animation.

### 📱 Status Bar & Dynamic Island (v1.6 - v1.9)
*   **Dual Row Signal Integration**: Introduced SystemUI observers and custom vector drawables representing stacked primary and secondary SIM indicators.
*   **Dynamic Island Transition Fix**: Fixed clock pattern dissolve delays and alignment offsets occurring during the expansion sizing animations of the Dynamic Island.
*   **SystemUI Stability Correction**: Prevented SystemUI crashes on Island Collision toggle by resolving Java Reflection field access permissions for the clock dissolve system.
*   **Real-time Preference UI Redraw**: Enabled real-time UI redraw updates for clock format and date preferences upon toggling settings, without requiring a reboot.
*   **Dynamic Island Dissolve Tweaks**: Re-aligned and resolved rendering timing during the Dynamic Island collision transitions.

### ⚙️ Settings, Shortcuts & Hardware Polling (v1.2 - v1.5)
*   **Settings Toolbox Shortcut Integration**: Re-routed the custom Settings Toolbox shortcuts to launch the Xoeris Toolbox.
*   **ReVanced MicroG Redirect**: Re-directed default ReVanced settings paths to launch MicroG.
*   **Real-time Seconds Tick**: Added background ticking logic for custom clock formats requiring real-time seconds updates.
*   **Left RRI Jitter/Oscillation Fix**: Resolved structural loop feedback layout oscillations during Left RRI rendering inside the clock area by replacing custom sizing rules with stable `INVISIBLE` transition states.
*   **Settings Provider Standard**: Unified and corrected settings storage access patterns (System vs Secure) ensuring settings switches apply instantly.
*   **Custom Observables Registry**: Registered and loaded comprehensive SystemUI background watchers tracking format changes dynamically.
*   **Refresh Rate Indicator (RRI) Toggle**: Integrated a settings toggle to switch the Refresh Rate Indicator position between Left and Right status bar locations.
*   **Dynamic Island Collision & Dissolve System**: Implemented collision-detection rules to dissolve or hide the clock text if the Dynamic Island expands near its margins.
*   **Date/Time Formatting Engines**: Embedded preprocessors in settings to allow advanced user customization of clock and date string formats.
*   **RRI Lockscreen Handshake**: Resolved initialization issues that caused the Refresh Rate Indicator to disappear upon lockscreen unlock or during early boot phases.
*   **My Device Integration**: Added custom "Powered by Xoeris" and "System Changelogs" preference cards inside the Settings My Device dashboard.
*   **CPU/GPU Frequency Polling**: Added sysfs polling threads to fetch real-time clock frequencies for performance cards.
*   **Visual Card Design Overhaul**: Restyled the performance monitor metrics for improved integration with dark mode, fixing focus bounds and touch ripple effects.
*   **Monitors Refactoring**: Packaged and modularized all monitoring code inside the `xoerislibx` library structure.

### 🚀 Core OS Base Features (v1.0 Initial Release)
*   **Settings Performance Monitor Dashboard**: Displays real-time system usage statistics (CPU load, GPU load, RAM allocation, and Storage capacity).
*   **Debloated Environment**: Completely removed unnecessary system and user applications.
*   **Architecture & Kernels**: Built for `arm64` architecture with generic kernel compatibility and a clean AVB configuration management setup.

---

## Device Support

| Brand    | Support Status |
|----------|----------------|
| Xiaomi   | Supported      |
| POCO     | Supported      |
| Redmi    | Supported      |
| REDMAGIC | Supported      |
| Oppo     | Supported      |
| Realme   | Supported      |
| Vivo     | Not Supported  |
| iQOO     | Not Supported  |
| Samsung  | Not Supported  |
| Lenovo   | Not Supported  |
| Infinix  | Not Supported  |
| Nubia    | Not Supported  |


---

## Intended Audience

*   Android developers
*   Kernel developers
*   ROM maintainers
*   Advanced power users

---

## Disclaimer

> **Warning:** XoerisOS2 is intended for development and testing purposes. Flashing modified images may void warranties or permanently damage devices. Users assume full responsibility for any modifications performed.

---

## Roadmap

*   Advanced kernel tuning
*   Boot performance improvements
*   Modular component structure
*   Automated build pipeline

---

## Contributing

Contributions are welcome. Please open an issue on the GitHub repository before submitting significant changes.

---

### *License*

This project is licensed under the MIT License.  
See the LICENSE file for details.
