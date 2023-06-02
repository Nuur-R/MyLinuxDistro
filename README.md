# USB TTL Error code 2 solution
https://askubuntu.com/questions/112568/how-do-i-allow-a-non-default-user-to-use-serial-device-ttyusb0
- sudoedit /etc/udev/rules.d/50-myusb.rules

KERNEL=="ttyUSB[0-9]*",MODE="0666"
KERNEL=="ttyACM[0-9]*",MODE="0666"



# Ubuntu TTL ttyUSB not show 
cp210
https://esp32.com/viewtopic.php?t=8673#:~:text=To%20sum%20this%20up%3A%20the%20original%20Silicon%20Labs,solved%20by%20installing%20the%20Pololu%20CP210x%20COM%20driver.
sudo chmod 666 /dev/ttyS3
sudo usermod -a -G dialout $USER