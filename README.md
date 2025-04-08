# OpenVPN-Setup-on-Ubuntu-VM-using-Nyr-Script
# 🌐 OpenVPN Setup on Ubuntu VM using Nyr Script

This project walks you through installing and configuring an OpenVPN server on an Ubuntu virtual machine using the community-trusted [Nyr OpenVPN install script](https://github.com/Nyr/openvpn-install).

---

### 🧱 Installation Start
Google whats my ip address and make a note of your public ip address we will need it for the set-up

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
Pick Google

Create client name (e.g., client1.ovpn)

## 🔑 Client File Location
The .ovpn file will be generated in your home directory:
```bash
/home/your-username/<name-of-client>.ovpn
```
### 📂 Client Config Output location
![Screenshot 2025-04-08 143204](https://github.com/user-attachments/assets/33ef0e72-9827-417e-8850-a1d8635bcb59)



Transfer this file to your VPN client device to connect securely.

### 👤 Add more clients
![Screenshot 2025-04-08 143047](https://github.com/user-attachments/assets/db2dfdfa-07e9-42ef-82fa-8079c402a9b7)

![Screenshot 2025-04-08 143105](https://github.com/user-attachments/assets/221ced53-79f0-4033-984e-972f3a2306a9)

![Screenshot 2025-04-08 143131](https://github.com/user-attachments/assets/0d393245-ef73-4364-a380-93f75fb826df)

## 🧪 Testing the VPN
You can test your VPN connection by:

Downloading the .ovpn file to a VPN client (e.g., OpenVPN app).

Importing the profile.

Connecting and verifying your new IP address.

Type the following command stop the OpenVPN service:
```bash
$ sudo systemctl stop openvpn@server
```
Type the following command start the OpenVPN service:
```bash
$ sudo systemctl start openvpn@server
```
Type the following command restart the OpenVPN service:
```bash
$ sudo systemctl restart openvpn@server
```
## 🙌 Credits
Huge thanks to Nyr for the auto-install script that makes VPN setup quick and easy.
