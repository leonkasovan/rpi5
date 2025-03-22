# rpi5
Raspberry Pi 5

# Change Page Size Kernel on the Raspberry Pi from 16K to 4K 
Why? 16K is faster but some software may crash (ex: VSCode).  

How?  
Edit config.txt  
```
[pi5]
kernel=kernel_2712.img
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
# Use Memory DDR NVMe via USB
Why? Power is not enough. So NVMe can not be loaded.  

How?  
Edit config.txt and add this line
```
[pi5]
sudo nano /boot/firmware/config.txt
usb_max_current_enable=1
sudo raspi-config
-> Advanced Options -> Boot Order -> NVMe/USB Boot
sudo reboot
```

