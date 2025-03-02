24.04.2 for RPi 5 
20.04.2 LTS for RPi 4

Write the imager file on it 

if rpi 5 then enable ssh and wifi using a separate monitor




sudo apt update
sudo apt upgrade
sudo apt install openssh-server
sudo systemctl enable ssh


sudo kill -9 36879


sudo ufw allow OpenSSH
sudo ufw enable
sudo ufw status

sudo systemctl restart ssh











sudo apt install -y xfce4 xfce4-goodies
sudo apt install -y xrdp
sudo adduser xrdp ssl-cert
sudo systemctl enable --now xrdp
echo "xfce4-session" | tee ~/.xsession
sudo ufw allow 3389/tcp
echo "xfce4-session" | tee ~/.xsession
chmod 644 ~/.xsession
sudo nano /etc/xrdp/startwm.sh



delete everything, paste this, save
#!/bin/sh
unset DBUS_SESSION_BUS_ADDRESS
unset XDG_RUNTIME_DIR
exec startxfce4


sudo systemctl restart xrdp
