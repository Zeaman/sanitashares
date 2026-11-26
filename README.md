# Sanita-share (Ubuntu File Share)

Direct device-to-device file sharing for **every Ubuntu machine**: PCs, laptops, and NVIDIA Jetson. No account. No cloud. Transfers stay on your local Wi-Fi or Ethernet. Home is two rows: **SEND** and **RECEIVE**, then **TEXT** (two-way notes on the same session). Settings include English/Amharic and Light/Dark theme.

Copyright © 2026 **YomTech Solutions (Amanuel Mihiret)**  
License: MIT (see `LICENSE` and `copyright`)  
Email: yomtech44@gmail.com · Telegram: [@YomTech44](https://t.me/YomTech44)  
Downloads: https://github.com/Zeaman/sanitashares/releases/latest

These installers are **`.deb` files** (Debian/Ubuntu packages). Apt cannot install a `.db` file. Use `./` so apt reads the file in the current folder.

| Computer | Installer |
|---|---|
| Jetson Orin Nano / other ARM64 Ubuntu | `sanitashares_0.1.0_arm64.deb` |
| Regular Ubuntu PC (Intel / AMD) | `sanitashares_0.1.0_amd64.deb` |

## Which file?

```bash
dpkg --print-architecture
```

`arm64` → Jetson / ARM file. `amd64` → Ubuntu PC file.

## Install on Jetson / ARM64

```bash
sudo apt install --reinstall ./sanitashares_0.1.0_arm64.deb
```

## Install on Ubuntu PC (Intel / AMD)

```bash
sudo apt install --reinstall ./sanitashares_0.1.0_amd64.deb
```

## Open

```bash
ufshare
```

Or search the app menu for **Sanita-share** and double-click it.

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

## Remove

```bash
sudo apt remove --purge sanitashares ufshare
```

Works on Ubuntu 20.04, 22.04, and 24.04.

## Copyright

```
Copyright (c) 2026 YomTech Solutions (Amanuel Mihiret)
```

Published by **YomTech Solutions**. Contact: yomtech44@gmail.com · Telegram @YomTech44.
