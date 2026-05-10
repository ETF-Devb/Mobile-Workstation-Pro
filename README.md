

````md
# 🚀 Mobile Desktop Pro — Ubuntu on Android

<p align="center">
  <img src="https://img.shields.io/badge/Ubuntu-22.04%20LTS-8A2BE2?style=for-the-badge&logo=ubuntu&logoColor=white" />
  <img src="https://img.shields.io/badge/Platform-Android%20%2B%20Termux-3DDC84?style=for-the-badge&logo=android&logoColor=white" />
  <img src="https://img.shields.io/badge/Desktop-XFCE4-9400D3?style=for-the-badge&logo=xfce&logoColor=white" />
  <img src="https://img.shields.io/badge/License-MIT-blue?style=for-the-badge" />
</p>

<p align="center">
  <img src="https://images2.imgbox.com/22/46/JdJE2JMG_o.png" width="900" alt="Ubuntu on Android Preview" />
</p>

**Mobile Desktop Pro** is a lightweight and practical project that transforms an Android device into a usable **Ubuntu Linux workstation** using **Termux**, **proot-distro**, and **Termux-X11**.

It is designed for developers, learners, testers, and power users who want a desktop Linux environment on mobile hardware with a clean and efficient workflow.

---

## ✨ Overview

This project provides a guided setup for running **Ubuntu 22.04 LTS** with the **XFCE4 desktop environment** on Android.

It focuses on:
- simplicity
- stability
- performance
- clean installation workflow
- compatibility with Termux-X11

---

## 📦 Core Requirements

- Android device
- Termux
- Termux-X11
- Internet connection
- Enough storage space
- Basic familiarity with terminal commands

---

## 🧱 System Stack

- **Engine:** Termux + proot-distro
- **Distribution:** Ubuntu Jammy (22.04 LTS)
- **Desktop Environment:** XFCE4
- **Display Server:** Termux-X11
- **License:** MIT

---

## 🚀 Features

- Ubuntu 22.04 LTS on Android
- XFCE4 desktop interface
- Termux-X11 graphical session
- Lightweight and mobile-friendly setup
- Fast startup workflow
- Suitable for coding, testing, browsing, and Linux learning
- Easy to install, launch, and stop

---

## 🛠️ Installation

### 1) Update Termux and prepare storage

```bash
pkg update && pkg upgrade -y
pkg install wget curl proot-distro -y
termux-setup-storage
````

### 2) Download the installer

```bash
curl -fsSL https://git.io/udroid-installer -o install.sh
bash install.sh
```

### 3) Install Ubuntu XFCE4

```bash
udroid install jammy:xfce4
```

---

## ▶️ Running the Desktop

### 1) Start Termux-X11

Before launching the desktop, make sure **Termux-X11** is running in the background.

```bash
termux-x11 :1 -ac &
```

### 2) Start Ubuntu and XFCE4

```bash
udroid login jammy:xfce4 -- bash -lc 'service dbus start; export DISPLAY=:1; startxfce4'
```

---

## ⛔ Stopping the Session

To exit the environment normally:

```bash
exit
```

If you need to force-close leftover processes:

```bash
pkill -9 -u $(whoami)
```

---

## 🧭 Usage Notes

* Always start **Termux-X11** before the Ubuntu session.
* Keep the `DISPLAY` variable set correctly.
* If the desktop does not appear, restart Termux-X11 and relaunch the session.
* Make sure the installation finished successfully before trying to log in.

---

## 🧪 Troubleshooting

### Black screen or no desktop

* Confirm that Termux-X11 is open and active.
* Check that `DISPLAY=:1` is exported.
* Restart the session after killing leftover processes.

### Installer does not work

* Check your internet connection.
* Update Termux packages first.
* Retry the installer command.

### Desktop starts but closes immediately

* Ensure `dbus` is running.
* Make sure XFCE4 is installed correctly.
* Re-run the login command from a fresh Termux session.

---

## 🔐 Security & Scope

This project uses a **proot-based environment**, which is useful for portability and convenience.

It is designed for:

* education
* testing
* development
* mobile Linux workflows

It is **not** a replacement for a native full Linux installation on real hardware.

---

## 📁 Project Structure

```text
Mobile-Desktop-Pro/
├── README.md
├── LICENSE
├── install.sh
├── start.sh
└── assets/
```

---

## 📜 License

This project is licensed under the [MIT License](LICENSE).

---

## 👤 Author

**ETF-Devb**

---

## 💡 Final Note

Mobile Desktop Pro is built to give Android users a clean, functional, and efficient Linux desktop experience with minimal complexity and maximum usability.

```

