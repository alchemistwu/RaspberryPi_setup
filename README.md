# RaspberryPi_setup
## Basic setups for raspberry pi, including eduroam and time.
### * 1. Eduroam setup
  * 1. `sudo nano /etc/wpa_supplicant/wpa_supplicant.conf`
  * 2. Modify this file based the conf provided in this repo.
  * 3. `sudo wpa_supplicant -i wlan0 -c /etc/wpa_supplicant/wpa_supplicant.conf`
