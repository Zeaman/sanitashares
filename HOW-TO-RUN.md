# How to install Sanita-share 0.1.0

Publisher: **YomTech Solutions (Amanuel Mihiret)**  
Copyright © 2026 YomTech Solutions  
Email: yomtech44@gmail.com · Telegram @YomTech44

## 1. Pick the file for that computer

```bash
dpkg --print-architecture
```

| Result | File |
|---|---|
| `arm64` | `sanitashares_0.1.0_arm64.deb` (Jetson Orin Nano and other ARM Ubuntu) |
| `amd64` | `sanitashares_0.1.0_amd64.deb` (ordinary Ubuntu PC / laptop) |

## 2. Install

In the folder that contains the `.deb`:

```bash
sudo apt install ./sanitashares_0.1.0_arm64.deb
```

or

```bash
sudo apt install ./sanitashares_0.1.0_amd64.deb
```

## 3. Open

```bash
ufshare
```

or double-click **Sanita-share** in the applications menu.

The window title is **Sanita-share**. The line under it is **Ubuntu File Share**.

If the window does not open, start the background service once:

```bash
systemctl --user daemon-reload
systemctl --user enable --now ufshared.service
ufshare
```
