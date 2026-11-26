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

The installer stops any old hidden Sanita-share window. Then:

```bash
ufshare
```

or double-click **Sanita-share** in the applications menu. Home is two rows: **SEND** and **RECEIVE** on the first row, **TEXT** under SEND on the second. SEND has two boxes (**Drop files here** and **Select folder to send**) plus a green **Select files** button. TEXT waits for another machine on TEXT, then shows a scrollable **Send Text** box and a **Receive Text** box with a copy icon. Nearby devices show as chips; **QR** shows the LAN address. Closing the window keeps receiving from the tray. Language (ENGLISH / AMHARIC) and theme (Light / Dark icon buttons) are under the gear.

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

If Connect finds the other computer but cannot join, on the machine that has **RECEIVE** open run:

```bash
sudo ufw allow 47621/tcp && sudo ufw allow 47622/udp
```

or `ufshare firewall` and approve the password prompt.

## 5. Remove

```bash
sudo apt remove --purge sanitashares ufshare
```

Closing the window only hides Sanita-share in the tray. New packages stop that tray on uninstall. If an icon is still there after remove, run:

```bash
pkill -x ufshare; pkill -x ufshared; pkill -x sanitashares
systemctl --user disable --now ufshared.service 2>/dev/null || true
rm -f ~/.local/share/applications/solutions.yomtech.sanitashares.desktop
```
