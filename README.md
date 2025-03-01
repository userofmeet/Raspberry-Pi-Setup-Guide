# Raspberry Pi Basic Setup and Commands

## Introduction
This repository contains essential commands for setting up and using a Raspberry Pi. These commands are useful for installing packages, managing the system, and troubleshooting.

## Initial Setup
1. **Update and Upgrade Packages:**
   ```bash
   sudo apt update && sudo apt upgrade -y
   ```
2. **Install Basic Utilities:**
   ```bash
   sudo apt install -y vim git curl wget htop
   ```
3. **Enable SSH (if not enabled):**
   ```bash
   sudo systemctl enable ssh
   sudo systemctl start ssh
   ```

## Network Configuration
1. **Check IP Address:**
   ```bash
   hostname -I
   ```
2. **Configure Wi-Fi (if needed):**
   ```bash
   sudo nano /etc/wpa_supplicant/wpa_supplicant.conf
   ```
   Add the following:
   ```plaintext
   network={
       ssid="YourSSID"
       psk="YourPassword"
   }
   ```
   Then restart networking:
   ```bash
   sudo systemctl restart networking
   ```

## Package Installation
1. **Python and Pip:**
   ```bash
   sudo apt install -y python3 python3-pip
   ```
2. **Install Node.js & NPM:**
   ```bash
   sudo apt install -y nodejs npm
   ```
3. **Install OpenCV for Image Processing:**
   ```bash
   sudo apt install -y python3-opencv
   ```

## System Monitoring
1. **Check System Usage:**
   ```bash
   htop
   ```
2. **Check Disk Space:**
   ```bash
   df -h
   ```
3. **Check Memory Usage:**
   ```bash
   free -h
   ```

## GPIO and Camera Setup
1. **Enable GPIO & Camera:**
   ```bash
   sudo raspi-config
   ```
   - Navigate to *Interfacing Options* > Enable *Camera* & *GPIO*

## Miscellaneous
1. **Reboot System:**
   ```bash
   sudo reboot
   ```
2. **Shutdown System:**
   ```bash
   sudo shutdown -h now
   ```
3. **Check Kernel Version:**
   ```bash
   uname -a
   ```

## Contribution
Feel free to add more useful commands and improve this repository!

## License
MIT License
