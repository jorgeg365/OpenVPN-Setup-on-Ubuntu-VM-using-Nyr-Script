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
![Screenshot 2025-04-08 145717](https://github.com/user-attachments/assets/dd240e8b-ef12-43a3-a67e-139c15f8b31e)

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

Sample
![Screenshot 2025-04-08 145747](https://github.com/user-attachments/assets/5bca8efb-08dc-44fb-a10e-1a6edf9e90b0)


## 🔑 Client File Location
The .ovpn file will be generated in your home directory:
```bash
/home/your-username/<name-of-client>.ovpn
```
### 📂 Client Config Output location
![Screenshot 2025-04-08 143204](https://github.com/user-attachments/assets/33ef0e72-9827-417e-8850-a1d8635bcb59)



Transfer this file to your VPN client device to connect securely.

### 👤 Add more clients
![Screenshot 2025-04-08 143037](https://github.com/user-attachments/assets/e65902a4-61ee-4654-8f93-0bb3108d90e4)

![Screenshot 2025-04-08 143047](https://github.com/user-attachments/assets/db2dfdfa-07e9-42ef-82fa-8079c402a9b7)

![Screenshot 2025-04-08 143105](https://github.com/user-attachments/assets/221ced53-79f0-4033-984e-972f3a2306a9)

![Screenshot 2025-04-08 143131](https://github.com/user-attachments/assets/0d393245-ef73-4364-a380-93f75fb826df)

## 📤 Port Forwarding Rule (for OpenVPN)
To allow VPN clients to connect to your OpenVPN server from outside your local network, you need to forward the port on your router or cloud firewall.

```bash
Protocol: UDP
Port:     1194
Internal IP: <Your Ubuntu VM's IP address>
Internal Port: 1194
```

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
