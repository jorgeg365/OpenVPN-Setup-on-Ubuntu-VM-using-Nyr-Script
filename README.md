# OpenVPN-Setup-on-Ubuntu-VM-using-Nyr-Script
# 🌐 OpenVPN Setup on Ubuntu VM using Nyr Script

This project walks you through installing and configuring an OpenVPN server on an Ubuntu virtual machine using the community-trusted [Nyr OpenVPN install script](https://github.com/Nyr/openvpn-install).

---

## 📸 Setup Previews

> Screenshots showing the process. Place your images in the `screenshots/` folder.

### 🧱 Installation Start
![Installation Start](screenshots/step1-installation.png)

### 👤 Client Profile Created
![Client Profile](screenshots/step2-client-creation.png)

### 📂 Client Config Output
![Client Config](screenshots/step3-client-config.png)

---

## 🛠️ Installation Steps

### 1. Update the System
```bash
sudo apt update && sudo apt upgrade -y
```
### 2. Download the script
```bash
wget https://git.io/vpn -O openvpn-install.sh
```

### 3. Run the installer
```bash
chmod +x openvpn-install.sh
```
Follow the prompts:

 Choose protocol (UDP recommended)

Default port (1194)

DNS provider (Google, Cloudflare, etc.)

Create client name (e.g., jorge.ovpn)

## 🔑 Client File Location
The .ovpn file will be generated in your home directory:

