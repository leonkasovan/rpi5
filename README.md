# rpi5
Raspberry Pi 5

# Using a 4K Page Size Kernel on the Raspberry Pi
Edit config.txt  
```
[pi5]
kernel=kernel8.img
usb_max_current_enable=1
```
Command Line:  
```
getconf PAGESIZE
16384
sudo nano /boot/firmware/config.txt
kernel=kernel8.img
sudo reboot
getconf PAGESIZE
4096
```
