# [ MOBILE_DESKTOP_PRO ] : Ubuntu on Android

<p align="center">
  <img src="https://img.shields.io/badge/Ubuntu-22.04_LTS-8A2BE2?style=for-the-badge&logo=ubuntu&logoColor=white" />
  <img src="https://img.shields.io/badge/Platform-Android_Termux-blue?style=for-the-badge&logo=android&logoColor=white" />
  <img src="https://img.shields.io/badge/GUI-XFCE4-9400D3?style=for-the-badge&logo=xfce&logoColor=white" />
</p>

<p align="center">
  <img src="https://images2.imgbox.com/22/46/JdJE2JMG_o.png" width="850" alt="Ubuntu on Android Preview" />
</p>

---

### [ >_ CORE_RESOURCES ]
<a href="https://github.com/ETF-Devb/Mobile-Workstation-Pro/releases/latest">
  <img src="https://img.shields.io/github/v/release/ETF-Devb/Mobile-Workstation-Pro?style=for-the-badge&color=8A2BE2&label=DOWNLOAD%20OFFICIAL%20APKs&logo=github" />
</a>

> [ # ] Access the latest optimized binaries from the official release section above.

---

### [ >_ INSTALLATION_FLOW ]

#### 1. Environment Setup
Initialize the Termux environment and grant necessary storage permissions.
```bash
pkg update && pkg upgrade -y
termux-setup-storage

```

#### 2. System Deployment

Deploy the *Udroid* engine and install the *Ubuntu Jammy* filesystem with *XFCE4* desktop environment.

```bash
# Fetch and run the official Udroid installer
curl -L -o install.sh [https://raw.githubusercontent.com/udroid-rc/udroid-installer/main/install.sh](https://raw.githubusercontent.com/udroid-rc/udroid-installer/main/install.sh) && bash install.sh

# Install the optimized Ubuntu distribution
udroid install jammy:xfce4

```

---

### [ !_ EXECUTION_PROTOCOL ]

> [!IMPORTANT]
> To ensure stability and avoid "Command Not Found" errors, follow this manual execution flow.

#### Step 1: Initialize X-Server

Start the display server in the background.

```bash
termux-x11 :1 -ac &

```

*(Ensure the **Termux-X11 app** is opened in the background).*

#### Step 2: System Login

Enter the Ubuntu proot environment.

```bash
udroid login jammy:xfce4

```

#### Step 3: Launch Desktop Environment

Once inside the Ubuntu shell (`root@localhost`), execute the following to start the GUI:

```bash
service dbus start && export DISPLAY=:1 && startxfce4

```

---

### [ X_ KILL_SWITCH ]

Use this protocol to properly terminate all background processes and clear the display cache.

```bash
# Exit the Ubuntu session first, then run:
pkill -9 termux-x11 && pkill -9 Xxwayland

```

---
