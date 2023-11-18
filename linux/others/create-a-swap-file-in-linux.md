# Create a swap file in linux

Swap space is a crucial aspect of any Linux system’s memory management. In a broad sense, swap space provides a safety net when physical RAM is exhausted, allowing the system to continue running smoothly. However, there may be times when we need to increase the swap space to ensure the Linux system’s optimal performance.

```bash
# view active swaps
swapon --show
# view available memory and swaps
free -h
# view avalibale space in disks
df -h    
# make an empty file
sudo fallocate -l 1G /swapfile_extend_1GB 
# give root only access   
sudo chmod 600 /swapfile_extend_1GB
# make it a swap file 
sudo mkswap /swapfile_extend_1GB 
# enbale swap   
sudo swapon /swapfile_extend_1GB 
# now add /swapfile_extend_1GB       none       swap    sw        0       0
# this line in fstab to allow remember after reboot
sudo vi /etc/fstab


```

Reference : [https://www.baeldung.com/linux/increase-swap-space](https://www.baeldung.com/linux/increase-swap-space)
