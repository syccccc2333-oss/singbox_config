# Personal sing-box Workspace

A high-performance **sing-box** configuration and management suite for Android (Magisk/Box modules) and Windows.

---

## 📋 Prerequisites

### The Core (Mandatory)
This setup **requires** the **[reF1nd fork](https://github.com/reF1nd/sing-box)** of sing-box.
* **Why?** It enables `proxy_providers` and `rule_providers` for remote subscription management, which are not available in the official upstream version.

---

## 💻 Windows Setup Guide

### 1. Directory & File Naming
For the management scripts to function, you must place the following files in the **same folder** and use these exact names:

| File | Requirement |
| :--- | :--- |
| **`sing-box.exe`** | The binary from reF1nd fork. |
| **`config.json`** | Your main config (rename `server_templates.json` to this). |
| **`singbox-manager.ps1`** | The PowerShell management script. |

### 2. Portable Launcher (`start-manager.bat`)
You can place `start-manager.bat` anywhere (e.g., Desktop) to avoid navigating folders:
1.  Right-click `start-manager.bat` -> **Edit**.
2.  Change the `TARGET_DIR` to your actual sing-box folder path:
    `set "TARGET_DIR=D:\Path\To\Your\sing-box"`
3.  **Run**: Double-click the `.bat` to launch the Cyberpunk-style manager with Admin privileges.

---

## 📱 Android Setup Guide (Box Modules)

Optimized for **Box4Magisk**, **KM-Box**, or similar Magisk-based transparent proxy modules.

### 1. Configuration Deployment
1.  Locate your module's configuration directory (usually `/data/adb/box/` or `/data/adb/sing-box/`).
2.  Upload `config_box.json` and rename it to `config.json` within that folder.
3.  Upload `webRTC.json` to the `rule_set` subfolder (or as specified in your `config.json` paths).

### 2. Core Replacement
Ensure the binary used by the module is the **reF1nd fork**:
* Replace the file at `/data/adb/box/bin/sing-box` with the reF1nd Android binary.
* Set permissions to `0755` (rwxr-xr-x) using a file manager like MT Manager or via terminal:
  `chmod +x /data/adb/box/bin/sing-box`

### 3. Usage
* Use the module's dashboard or terminal command (e.g., `box start`) to initialize.
* Check logs via `/data/adb/box/run/runs.log` to ensure rule-sets are downloading correctly.

---

## 🛠 Features
* **Smart Routing**: Advanced rules for Google, Telegram, YouTube, and Bilibili.
* **Ad-Blocking**: Integrated `AWAvenue-Ads` for a cleaner browsing experience.
* **Enhanced DNS**: High-concurrency DNS settings over QUIC and HTTP/3.
* **Windows Service**: Easily install sing-box as a background service via the PS1 script.

---
*Disclaimer: For personal use and technical research only.*
