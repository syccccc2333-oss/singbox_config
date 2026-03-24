# Personal sing-box Workspace

A customized **sing-box** configuration and management suite optimized for Android (via Box modules) and Windows (via enhanced PowerShell scripts).

---

## 📂 File Descriptions

* **`server_templates.json`**: Core configuration template featuring Clash API, DNS over QUIC/HTTP3, and FakeIP support.
* **`webRTC.json`**: Specialized rule-set for managing, optimizing, or blocking WebRTC/STUN traffic.
* **`singbox-manager.ps1`**: An advanced Windows manager with a Cyberpunk-style UI, real-time log monitoring, and service controls.
* **`start-manager.bat`**: A portable one-click launcher that allows you to run the manager from any directory.

---

## ⚙️ Requirements

### 1. The Core (Mandatory)
This setup **requires** the **[reF1nd fork](https://github.com/reF1nd/sing-box)** of sing-box.
> **Note:** This configuration relies on `proxy_providers` and `rule_providers` for automated subscription and rule-set management. These features are currently not supported in the official upstream version.

### 2. Android
Recommended for use with the **box** (Box4Magisk) module for system-wide transparent proxying.

---

## 🚀 Windows Usage Guide

### 1. File Placement & Naming
For the `singbox-manager.ps1` script to function correctly, the following files **must** be placed in the **same directory** and use these exact names:
* **Binary**: `sing-box.exe`
* **Configuration**: `config.json` (You may rename `server_templates.json` to `config.json` after editing).
* **Manager**: `singbox-manager.ps1`

### 2. Configure the Launcher
The `start-manager.bat` can be placed anywhere (e.g., your Desktop) for convenience:
* Right-click `start-manager.bat` and select **Edit**.
* Locate the line `set "TARGET_DIR=..."` and change the path to the folder where your `sing-box.exe` is actually stored.

### 3. Execution
Double-click `start-manager.bat` to:
* Automatically request Administrator privileges.
* Launch the PowerShell Manager menu to install services, toggle the system proxy, or monitor traffic.

---

## 🛠 Key Features
* **Portable Launcher**: Run your manager from any location without navigating to the program folder.
* **Smart Routing**: Pre-configured rules for Google, Telegram, YouTube, and AWAvenue/217heidai ad-blocking.
* **System Integration**: Easily register sing-box as a Windows Service for silent, background operation and auto-start on boot.
* **Customizable**: Script variables for file names and paths can be modified within the `.ps1` file if you have specific naming preferences.

---
*Disclaimer: For personal use and educational purposes only.*
