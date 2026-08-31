# UBUNTU

Run a full Ubuntu Desktop environment (XFCE or GNOME) directly on your Android device using Termux and Udroid. 

Setting up Linux on Android can be tricky, often leading to annoying display, audio, or permission errors. This repository simplifies the entire process, providing automated scripts to handle the heavy lifting alongside comprehensive manual setup instructions.

---

## 🌟 Features

* **Zero-Touch Configuration:** Installs all core dependencies—including X11 display servers and audio drivers—in one go.
* **Smart Auto-Fix System:** Instantly clears common environment hurdles like `Access Denied` or `Display Locked` errors without manual troubleshooting.
* **Full Native Audio:** Integrated PulseAudio support ensures crisp, working sound out of the box (fixing frequent audio issues in apps like Firefox).
* **100% Rootless:** Enjoy a full Linux desktop experience without risking your device's security or needing root access.

---
## Download Termux
[Download Termux (F-Droid)](https://f-droid.org/en/packages/com.termux/)

[Download Termux-X11 Nightly (GitHub)](https://github.com/termux/termux-x11/releases/tag/nightly)


## installation command 

```
pkg update -y && pkg upgrade -y && pkg install x11-repo -y && pkg install termux-x11-nightly -y && . <(curl -Ls https://bit.ly/udroid-installer) && udroid install jammy:xfce4

```

## launch commands
```
termux-x11 :1  -ac &
```
```
udroid login jammy:xfce4
```
```
export DISPLAY=:1
```
```
startxfce4 &
```

