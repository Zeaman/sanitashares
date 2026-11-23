# Sanita-share (Ubuntu File Share)

Direct device-to-device file sharing for **every Ubuntu machine**: PCs, laptops, and NVIDIA Jetson. No account. No cloud. Transfers stay on your local Wi-Fi or Ethernet.

Copyright © 2026 **YomTech Solutions (Amanuel Mihiret)**  
License: MIT (see `LICENSE` and `copyright`)  
Email: yomtech44@gmail.com · Telegram: [@YomTech44](https://t.me/YomTech44)  
Downloads: https://github.com/Zeaman/sanitashares/releases/latest

These installers are **`.deb` files** (Debian/Ubuntu packages). Apt cannot install a `.db` file.

| Computer | Installer |
|---|---|
| Jetson Orin Nano / other ARM64 Ubuntu | `sanitashares_0.1.0_arm64.deb` |
| Regular Ubuntu PC (Intel / AMD) | `sanitashares_0.1.0_amd64.deb` |

Check your computer first:

```bash
dpkg --print-architecture
```

`arm64` → use the Jetson/ARM file. `amd64` → use the PC file.

## Install, then open

Copy the matching `.deb` onto the Ubuntu machine, open a terminal in that folder, and run **one** of:

```bash
# Jetson / ARM64
sudo apt install ./sanitashares_0.1.0_arm64.deb

# Ubuntu PC (Intel/AMD)
sudo apt install ./sanitashares_0.1.0_amd64.deb
```

The `./` is required. Then open the app:

```bash
ufshare
```

Or search the app menu for **Sanita-share** and double-click it.

Works on Ubuntu 20.04, 22.04, and 24.04.

## Copyright

```
Copyright (c) 2026 YomTech Solutions (Amanuel Mihiret)
```

Published by **YomTech Solutions**. Contact: yomtech44@gmail.com · Telegram @YomTech44.
