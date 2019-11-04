# RaspberryPi_setup
## Basic setups for raspberry pi, including eduroam and time.
### 1. Eduroam setup
  * 1. `sudo nano /etc/wpa_supplicant/wpa_supplicant.conf`
  * 2. Modify this file based the conf provided in this repo.
  * 3. `sudo wpa_supplicant -i wlan0 -c /etc/wpa_supplicant/wpa_supplicant.conf`
### 2. Time setup
  * 1. `sudo wget https://codeload.github.com/iridium77/htpdate/zip/master`
  * 2. `unzip master`
  * 3. `cd ./htpdate-master/`
  * 4. `make`
  * 5. `sudo make install`
  * 6. `sudo htpdate -d -s -l -b -t www.raspberrypi.org`
  * 7. `date`
  * 8. `cd ./scripts/`
  * 9. `sudo cp htpdate.init /etc/init.d/`
  * 10. `sudo chmod 777 htpdate.init`
  * 11. `cd /etc/init.d/`
  * 12. `sudo apt-get install insserv`
  * 13. `sudo insserv htpdate.init`
  * 14. `sudo systemctl daemon-reload`
  * 15. `sudo service htpdate.init start`
  
