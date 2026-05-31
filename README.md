# XoerisOS2

#### _Clean. Fast. Maximum._

XoerisOS2 is a lightweight Android-based operating system focused on performance optimization, system stability, deep UI customization, and clean integration for development environments[cite: 1].

---

## Overview

XoerisOS2 is designed to provide a minimal, highly customizable, and efficient base suitable for developers, kernel engineers, and advanced Android users[cite: 1]. The system emphasizes clarity in configuration, smooth SystemUI animations, real-time hardware monitoring, and generic kernel compatibility[cite: 1].

---

## Technical Features & Changelog (v1.0 - v2.0)

XoerisOS2 brings massive upgrades to the SystemUI framework, layout stability, and performance tracking[cite: 1]. Below is the complete feature set implemented up to the latest release:

### 🌟 SystemUI & Layout Optimizations (v2.0 Latest)
*   **Vertical Dual Row Signal Layout Fix**: Completely corrected the dual-row SIM layout horizontal spacing bug[cite: 1]. Single-row mobile indicators now transition to a `GONE` visibility state when dual-row signal is toggled, letting the vertically stacked primary/secondary indicators take over layout bounds correctly[cite: 1].
*   **Dynamic Sibling View Container Detection**: Refactored `DualRowSignalController` to dynamically traverse sibling `ModernStatusBarMobileView` children inside the status bar's parent icon container, ensuring the second SIM is correctly identified and disabled to prevent duplicate rows[cite: 1].
*   **MIUI Elastic Spring Overscroll Support**: Integrated MIUI's `miuix.springback.view.SpringBackLayout` wrapper around the custom **About** (Powered by) and **System Changelogs** screens, enabling the native elastic spring overscroll animation[cite: 1].

### 📱 Status Bar & Dynamic Island (v1.6 - v1.9)
*   **Dual Row Signal Integration**: Introduced SystemUI observers and custom vector drawables representing stacked primary and secondary SIM indicators[cite: 1].
*   **Dynamic Island Transition Fix**: Fixed clock pattern dissolve delays and alignment offsets occurring during the expansion sizing animations of the Dynamic Island[cite: 1].
*   **SystemUI Stability Correction**: Prevented SystemUI crashes on Island Collision toggle by resolving Java Reflection field access permissions for the clock dissolve system[cite: 1].
*   **Real-time Preference UI Redraw**: Enabled real-time UI redraw updates for clock format and date preferences upon toggling settings, without requiring a reboot[cite: 1].
*   **Dynamic Island Dissolve Tweaks**: Re-aligned and resolved rendering timing during the Dynamic Island collision transitions[cite: 1].

### ⚙️ Settings, Shortcuts & Hardware Polling (v1.2 - v1.5)
*   **Settings Toolbox Shortcut Integration**: Re-routed the custom Settings Toolbox shortcuts to launch the Xoeris Toolbox[cite: 1].
*   **ReVanced MicroG Redirect**: Re-directed default ReVanced settings paths to launch MicroG[cite: 1].
*   **Real-time Seconds Tick**: Added background ticking logic for custom clock formats requiring real-time seconds updates[cite: 1].
*   **Left RRI Jitter/Oscillation Fix**: Resolved structural loop feedback layout oscillations during Left RRI rendering inside the clock area by replacing custom sizing rules with stable `INVISIBLE` transition states[cite: 1].
*   **Settings Provider Standard**: Unified and corrected settings storage access patterns (System vs Secure) ensuring settings switches apply instantly[cite: 1].
*   **Custom Observables Registry**: Registered and loaded comprehensive SystemUI background watchers tracking format changes dynamically[cite: 1].
*   **Refresh Rate Indicator (RRI) Toggle**: Integrated a settings toggle to switch the Refresh Rate Indicator position between Left and Right status bar locations[cite: 1].
*   **Dynamic Island Collision & Dissolve System**: Implemented collision-detection rules to dissolve or hide the clock text if the Dynamic Island expands near its margins[cite: 1].
*   **Date/Time Formatting Engines**: Embedded preprocessors in settings to allow advanced user customization of clock and date string formats[cite: 1].
*   **RRI Lockscreen Handshake**: Resolved initialization issues that caused the Refresh Rate Indicator to disappear upon lockscreen unlock or during early boot phases[cite: 1].
*   **My Device Integration**: Added custom "Powered by Xoeris" and "System Changelogs" preference cards inside the Settings My Device dashboard[cite: 1].
*   **CPU/GPU Frequency Polling**: Added sysfs polling threads to fetch real-time clock frequencies for performance cards[cite: 1].
*   **Visual Card Design Overhaul**: Restyled the performance monitor metrics for improved integration with dark mode, fixing focus bounds and touch ripple effects[cite: 1].
*   **Monitors Refactoring**: Packaged and modularized all monitoring code inside the `xoerislibx` library structure[cite: 1].

### 🚀 Core OS Base Features (v1.0 Initial Release)
*   **Settings Performance Monitor Dashboard**: Displays real-time system usage statistics (CPU load, GPU load, RAM allocation, and Storage capacity)[cite: 1].
*   **Debloated Environment**: Completely removed unnecessary system and user applications[cite: 1].
*   **Architecture & Kernels**: Built for `arm64` architecture with generic kernel compatibility and a clean AVB configuration management setup[cite: 1].

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

[cite: 1]

---

## Intended Audience

*   Android developers[cite: 1]
*   Kernel developers[cite: 1]
*   ROM maintainers[cite: 1]
*   Advanced power users[cite: 1]

---

## Disclaimer

> **Warning:** XoerisOS2 is intended for development and testing purposes[cite: 1]. Flashing modified images may void warranties or permanently damage devices[cite: 1]. Users assume full responsibility for any modifications performed[cite: 1].

---

## Roadmap

*   Advanced kernel tuning[cite: 1]
*   Boot performance improvements[cite: 1]
*   Modular component structure[cite: 1]
*   Automated build pipeline[cite: 1]

---

## Contributing

Contributions are welcome[cite: 1]. Please open an issue on the GitHub repository before submitting significant changes[cite: 1].

---

### *License*

This project is licensed under the MIT License[cite: 1].  
See the LICENSE file for details[cite: 1].
