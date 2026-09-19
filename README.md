# Project Sage EDR — Official Releases & Downloads

[![Release](https://img.shields.io/badge/Release-v1.0.0--beta-blue?style=flat-square)](https://github.com/Jishnu09-siuu/Sage-edr-releases/releases)
[![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20macOS%20%7C%20Linux-lightgrey?style=flat-square)](https://github.com/Jishnu09-siuu/Sage-edr-releases/releases)
[![License](https://img.shields.io/badge/License-Proprietary%20EULA-crimson?style=flat-square)](LICENSE)
[![Security](https://img.shields.io/badge/AI%20Engine-100%25%20Local%20Ollama-orange?style=flat-square)](https://ollama.ai)

This is the **official public distribution repository** for **Project Sage EDR** compiled installers, setup binaries, and integrity checksums. 

> [!NOTE]
> **Project Sage EDR** is a proprietary commercial cybersecurity platform. The core detection engine and source code are maintained in a private repository. This repository provides signed releases, installers, and release notes for public evaluation and client deployments.

---

## 📥 Downloads (v1.0.0-beta)

| Operating System | Package Type | Architecture | Download Link |
| :--- | :--- | :---: | :--- |
| **Windows 10 / 11** | Setup Installer (`.exe`) | x64 | [**Download Windows Installer (.exe)**](https://github.com/Jishnu09-siuu/Sage-edr-releases/releases/download/v1.0.0-beta/Sage-EDR-Setup-1.0.0-beta.exe) |
| **macOS** | Universal Disk Image / Bundle | Apple Silicon (M1/M2/M3) & Intel | [**Download macOS (.zip)**](https://github.com/Jishnu09-siuu/Sage-edr-releases/releases/download/v1.0.0-beta/macos-binaries.zip) |
| **Linux** | AppImage & Debian Package | x64 (Ubuntu / Debian / CentOS) | [**Download Linux (.zip)**](https://github.com/Jishnu09-siuu/Sage-edr-releases/releases/download/v1.0.0-beta/linux-binaries.zip) |

---

## 🔒 Verification & Checksums

Always verify the integrity of downloaded binaries before installation:

```text
Sage-EDR-Setup-1.0.0-beta.exe (SHA-256):
02EDB25F2F4D08B485BB39A73BB116135CE0673F02F62B2C235AFDFD6ABCD648

Sage-EDR-Setup-1.0.0-beta.zip (SHA-256):
B3DED6C130E7C8C27D9DECE953A7299108E8DB073B6461209BDAAEE3F92ECCCF

Sage-EDR-1.0.0-beta.exe (SHA-256):
13C57808DF44125E01566F2DE859418572BB4456E0E7C0C728B9D51BA609A2A3
```

You can verify with PowerShell on Windows:
```powershell
Get-FileHash -Algorithm SHA256 "Sage-EDR-Setup-1.0.0-beta.exe"
```

---

## 🚀 Quick Start Guide

### Prerequisites
1. **Local Ollama AI Engine**: Install [Ollama](https://ollama.ai) on your system.
2. **Pull the AI Model**: Open terminal/command prompt and run:
   ```bash
   ollama run monotykamary/whiterabbitneo-v1.5a
   ```
   *(Optional lightweight routes: `ollama pull qwen2.5:0.5b` and `ollama pull llama3.2:1b`)*

### Installation & Permission Guide

#### 🪟 Windows 10 / 11 (SmartScreen & Administrator Privileges)

Because **Sage EDR** is an endpoint security tool that inspects live processes and controls firewall isolation, Windows Security and User Account Control (UAC) will prompt for permissions during setup:

1. **Windows SmartScreen Alert ("Windows protected your PC")**:
   * **Why it appears**: Sage EDR v1.0.0-beta is a newly released build undergoing commercial certification. Microsoft Defender SmartScreen flags unrecognized new binaries by default.
   * **How to proceed**: Click **"More info"** on the blue banner ➔ Click **"Run anyway"**.

2. **User Account Control (UAC Prompt)**:
   * **Why it appears**: As an EDR (Endpoint Detection and Response) platform, Sage requires administrative privileges to:
     * Terminate malicious processes and inject memory blocks.
     * Vault and encrypt suspicious files in the Fernet AES-256 quarantine vault.
     * Isolate network adapters using Windows Firewall (`netsh`) during active containment.
   * **How to proceed**: Click **"Yes"** to grant administrative permissions.

3. **Launch the Application**:
   * Launch **Sage EDR** from your Desktop shortcut or Start Menu.
   * The desktop system tray icon will appear, initialize baseline sensors, and open your control dashboard at `http://127.0.0.1:5050`.

---

#### 🍏 macOS (Gatekeeper Verification)

* **Why it appears**: macOS Gatekeeper checks new third-party applications before launch.
* **How to proceed**:
  1. Open the downloaded `.zip` and mount the `Sage-EDR-1.0.0-beta.dmg`.
  2. Drag **Sage EDR** into your `/Applications` folder.
  3. If prompted with *"macOS cannot verify the developer"*, go to **System Settings ➔ Privacy & Security**, scroll down, and click **"Open Anyway"** (or right-click the app and select **Open**).

---

#### 🐧 Linux (AppImage & Debian)

1. Extract `linux-binaries.zip`.
2. **For AppImage**: Make it executable and run:
   ```bash
   chmod +x Sage-EDR-1.0.0-beta.AppImage
   ./Sage-EDR-1.0.0-beta.AppImage
   ```
3. **For Debian / Ubuntu (`.deb`)**:
   ```bash
   sudo dpkg -i sage-edr_1.0.0-beta_amd64.deb
   ```

---

## 📜 License & Terms

Project Sage EDR is proprietary commercial software. All rights reserved by Project Sage.

* **Evaluation / Beta License**: Permitted solely for personal testing, defensive evaluation, and non-commercial security research in accordance with the [End User License Agreement (LICENSE)](LICENSE).
* **Commercial Use & Fleet Deployments**: Commercial deployment, multi-tenant managed security services (MSSP), sublicensing, reselling, or white-labeling is strictly prohibited without an explicit commercial license.
* **Disclaimer**: This software is provided "AS IS" without warranty of any kind. Always test defensive tools in a staging environment prior to production deployment.

For commercial fleet licensing, custom YARA intelligence feeds, or enterprise inquiries, please contact the maintainers.
