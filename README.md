# 🚀 Mobile Desktop Pro: Ubuntu on Android

<p align="center">
  <img src="https://img.shields.io/badge/Ubuntu-22.04_LTS-8A2BE2?style=for-the-badge&logo=ubuntu&logoColor=white" />
  <img src="https://img.shields.io/badge/Platform-Android_Termux-blue?style=for-the-badge&logo=android&logoColor=white" />
  <img src="https://img.shields.io/badge/GUI-XFCE4-9400D3?style=for-the-badge&logo=xfce&logoColor=white" />
</p>

<p align="center">
  <img src="https://images2.imgbox.com/22/46/JdJE2JMG_o.png" width="600" alt="Ubuntu on Android Preview" />
</p>

Full guide to transforming an Android device into a functional **Ubuntu Linux** workstation. Optimized for performance and hardware acceleration using Termux-X11.

---

### 🏛️ Stack
* **Engine:** Termux (Proot-distro)
* **Distro:** Ubuntu Jammy (Udroid)
* **DE:** XFCE4 (Hardware Accelerated)
* **Display:** Termux-X11

---

### 🛠️ Installation

#### 1. Requirements
Install via **F-Droid**:
* [Termux](https://f-droid.org/en/packages/com.termux/)
* [Termux-X11](https://f-droid.org/en/packages/com.termux.x11/)

#### 2. Environment Setup
```bash
pkg update && pkg upgrade -y
termux-setup-storage
