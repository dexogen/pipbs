<p align="center">
  <img width="800" height="220" src="https://newsletter.proxmox.com/uploads/Proxmox-logo-opensource-white-background-800.png">
</p>

# PiPBS - Proxmox Backup Server for the Raspberry Pi
![arm64](https://img.shields.io/badge/architecture-arm64-9cf)
[![wofferl](https://img.shields.io/badge/wofferl-proxmox--backup--arm64-orange.svg)](https://github.com/wofferl/proxmox-backup-arm64)
![GitHub last commit](https://img.shields.io/github/last-commit/dexogen/pipbs)
![Workflow](https://github.com/dexogen/pipbs/actions/workflows/main.yml/badge.svg)
![GitHub Tag](https://img.shields.io/github/v/tag/wofferl/proxmox-backup-arm64)

Based on the excellent script of [wofferl](https://github.com/wofferl/proxmox-backup-arm64).

## Installation

> **Note:** Starting from version **4.0**, Proxmox Backup Server requires **Debian 13 (Trixie)** or distributions based on it.

### Set up the repository

1. Update the apt package index and install packages to allow apt to use a repository over HTTPS:
    ```bash
    sudo apt update
    sudo apt install -y ca-certificates curl gnupg lsb-release
    ```

2. Add GPG key:
    ```bash
    mkdir -p /etc/apt/keyrings
    sudo curl -fsSL https://dexogen.github.io/pipbs/gpg.key | sudo gpg --dearmor -o /etc/apt/keyrings/pipbs.gpg
    ```

3. Use the following command to set up the repository:
    ```bash
    echo "deb [arch=arm64 signed-by=/etc/apt/keyrings/pipbs.gpg] https://dexogen.github.io/pipbs/ trixie main" | sudo tee /etc/apt/sources.list.d/pipbs.list
    ```
    

### Install Proxmox Backup Server

1. Update the `apt` package index:
    ```bash
    sudo apt update
    ```
2. Install packages:
    ```bash
    sudo apt install -y raspberrypi-kernel-headers pv zfs-initramfs zfsutils-linux
    sudo apt install -y proxmox-backup-server
    ```
## Debug

If you encounter issues, first check the [Help section](https://github.com/wofferl/proxmox-backup-arm64?tab=readme-ov-file#help-section) and consult the official [Proxmox Backup Server documentation](https://pbs.proxmox.com/docs/installation.html).

<!--GAMFC-->
<!--GAMFC-END-->

<a href="https://star-history.com/#dexogen/pipbs&Date">
 <picture>
   <source media="(prefers-color-scheme: dark)" srcset="https://api.star-history.com/svg?repos=dexogen/pipbs&type=Date&theme=dark" />
   <source media="(prefers-color-scheme: light)" srcset="https://api.star-history.com/svg?repos=dexogen/pipbs&type=Date" />
   <img alt="Star History Chart" src="https://api.star-history.com/svg?repos=dexogen/pipbs&type=Date" />
 </picture>
</a>
