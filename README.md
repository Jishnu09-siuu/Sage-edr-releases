# Project Sage EDR — Official Releases & Downloads

[![Release](https://img.shields.io/badge/Release-v1.0.0--beta-blue?style=flat-square)](https://github.com/Jishnu09-siuu/Sage-edr-releases/releases)
[![Main Release](https://img.shields.io/badge/Release-main%20(Latest)-green?style=flat-square)](https://github.com/Jishnu09-siuu/Sage-edr-releases/releases/tag/main)
[![Platform](https://img.shields.io/badge/Platform-Windows%20%7C%20macOS%20%7C%20Linux-lightgrey?style=flat-square)](https://github.com/Jishnu09-siuu/Sage-edr-releases/releases)
[![License](https://img.shields.io/badge/License-Proprietary%20EULA-crimson?style=flat-square)](LICENSE)
[![Security](https://img.shields.io/badge/AI%20Engine-100%25%20Local%20Ollama-orange?style=flat-square)](https://ollama.ai)

This is the **official public distribution repository** for **Project Sage EDR** compiled installers, setup binaries, and integrity checksums. 

> [!NOTE]
> **Project Sage EDR** is a proprietary commercial cybersecurity platform. The core detection engine and source code are maintained in a private repository. This repository provides signed releases, installers, and release notes for public evaluation and client deployments.

### 🌟 Latest Release: Project Sage EDR Release main
* **Enterprise Redesign**: Dual theme system (White & Very Light Blue + Dark Graphite), Google Outfit typography, clean sidebar rail, and dedicated More Details investigation suite.
* **Full Endpoint Telemetry**: Integrated Endpoint Hardware & System Info diagnostics, process lineage graph, and real-time SSE threat event streams.
* 👉 [**View Latest Official Release & Binaries (main)**](https://github.com/Jishnu09-siuu/Sage-edr-releases/releases/tag/main)

---

## 📥 Downloads (Release `main` - Latest)

| Operating System | Package Type | Architecture | Download Link | File Size |
| :--- | :--- | :---: | :--- | :---: |
| **Windows 10 / 11** | Setup Installer (`.exe`) | x64 | [**Download Windows Setup Installer (.exe)**](https://github.com/Jishnu09-siuu/Sage-edr-releases/releases/download/main/Sage.EDR.Setup.1.0.0-beta.exe) | ~79 MB |
| **Windows 10 / 11** | Portable / Standalone (`.exe`) | x64 | [**Download Windows Portable (.exe)**](https://github.com/Jishnu09-siuu/Sage-edr-releases/releases/download/main/Sage.EDR.1.0.0-beta.exe) | ~79 MB |
| **macOS** | Disk Image (`.dmg`) | Apple Silicon (M1/M2/M3/M4) | [**Download macOS Installer (.dmg)**](https://github.com/Jishnu09-siuu/Sage-edr-releases/releases/download/main/Sage.EDR-1.0.0-beta-arm64.dmg) | ~100 MB |
| **macOS** | Application Bundle (`.zip`) | Apple Silicon (M1/M2/M3/M4) | [**Download macOS Bundle (.zip)**](https://github.com/Jishnu09-siuu/Sage-edr-releases/releases/download/main/Sage.EDR-1.0.0-beta-arm64-mac.zip) | ~95 MB |
| **Linux** | Universal AppImage | x64 (Any Linux distro) | [**Download Linux AppImage**](https://github.com/Jishnu09-siuu/Sage-edr-releases/releases/download/main/Sage.EDR-1.0.0-beta.AppImage) | ~108 MB |
| **Linux** | Debian / Ubuntu Package (`.deb`) | x64 (Ubuntu / Debian / Kali) | [**Download Debian Package (.deb)**](https://github.com/Jishnu09-siuu/Sage-edr-releases/releases/download/main/sage-edr-launcher_1.0.0-beta_amd64.deb) | ~73 MB |
| **Integrity Hashes** | SHA-256 Checksums | All Platforms | [**Download SHA256SUMS.txt**](https://github.com/Jishnu09-siuu/Sage-edr-releases/releases/download/main/SHA256SUMS.txt) | 582 B |

---

## 🔒 Verification & Checksums

Always verify the integrity of downloaded binaries before installation:

```text
ec7af8580658f6631689dc83f2cb58f7b1fa49e040c62c06c85e0e6349f070de  Sage.EDR.1.0.0-beta.exe
5e1b2925a7b9caef75be3a46d40892d7a86f8393868947707aa58f54d7aee9eb  Sage.EDR.Setup.1.0.0-beta.exe
49a6be370f7fba069c1b0e09e322cdcfefa2a9f13ac56f815c92ebccaf4e579c  Sage.EDR-1.0.0-beta-arm64-mac.zip
2dbffbc33f9abbad09dc73e0b7a2656b3392ae7f3d372be8caa5132bd4bfc0bc  Sage.EDR-1.0.0-beta-arm64.dmg
6c197f4d976cd79d7b8cd73f0b3f0e4417bb4d48ab27b8c73d2fd4f89a969e3a  Sage.EDR-1.0.0-beta.AppImage
e7dcb54029a72e3214af29004d7a94ec6a915d7cb4eef164260c5a3ca6bdb2d2  sage-edr-launcher_1.0.0-beta_amd64.deb
```

You can verify with PowerShell on Windows:
```powershell
Get-FileHash -Algorithm SHA256 "Sage.EDR.Setup.1.0.0-beta.exe"
```
Or on macOS / Linux:
```bash
shasum -a 256 "Sage.EDR-1.0.0-beta-arm64.dmg"
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
  1. Open the downloaded `Sage.EDR-1.0.0-beta-arm64.dmg` (or extract `Sage.EDR-1.0.0-beta-arm64-mac.zip`).
  2. Drag **Sage EDR** into your `/Applications` folder.
  3. If prompted with *"macOS cannot verify the developer"*, go to **System Settings ➔ Privacy & Security**, scroll down, and click **"Open Anyway"** (or right-click the app and select **Open**).

---

#### 🐧 Linux (AppImage & Debian)

1. **For AppImage**: Make it executable and run:
   ```bash
   chmod +x Sage.EDR-1.0.0-beta.AppImage
   ./Sage.EDR-1.0.0-beta.AppImage
   ```
2. **For Debian / Ubuntu (`.deb`)**:
   ```bash
   sudo dpkg -i sage-edr-launcher_1.0.0-beta_amd64.deb
   ```

---

## 📜 License & Terms

Project Sage EDR is proprietary commercial software. All rights reserved by Project Sage.

* **Evaluation / Beta License**: Permitted solely for personal testing, defensive evaluation, and non-commercial security research in accordance with the [End User License Agreement (LICENSE)](LICENSE).
* **Commercial Use & Fleet Deployments**: Commercial deployment, multi-tenant managed security services (MSSP), sublicensing, reselling, or white-labeling is strictly prohibited without an explicit commercial license.
* **Disclaimer**: This software is provided "AS IS" without warranty of any kind. Always test defensive tools in a staging environment prior to production deployment.

For commercial fleet licensing, custom YARA intelligence feeds, or enterprise inquiries, please contact the maintainers.
