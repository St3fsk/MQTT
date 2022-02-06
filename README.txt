sudo apt update && sudo apt upgrade

sudo apt install -y mosquitto mosquitto-clients

sudo systemctl enable mosquitto.service

sudo nano /etc/mosquitto/mosquitto.conf
add "listener 1883" and "allow_anonymous true" to the bottom

sudo raspi-config
Boot Options
Wait for Network at Boot
Yes

sudo ufw status
sudo apt-get install ufw
sudo ufw enable
sudo ufw allow 1883

sudo reboot

hostname -I = IP address of MQTT broker



