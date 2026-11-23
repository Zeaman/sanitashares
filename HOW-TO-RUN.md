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

## 2. Install on Jetson / ARM64

```bash
sudo apt install --reinstall ./sanitashares_0.1.0_arm64.deb
```

## 3. Install on Ubuntu PC (Intel / AMD)

```bash
sudo apt install --reinstall ./sanitashares_0.1.0_amd64.deb
```

## 4. Open

```bash
ufshare
```

or double-click **Sanita-share** in the applications menu.

If the window does not open:

```bash
systemctl --user daemon-reload
```

```bash
systemctl --user enable --now ufshared.service
```

```bash
ufshare
```

## 5. Remove

```bash
sudo apt remove --purge sanitashares ufshare
```
