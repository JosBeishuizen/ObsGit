# Opstartschijf creëren vanuit de terminal
sudo fdisk -l  
sudo umount /dev/sdb*  
sudo dd if=/path/to/ubuntu.iso of=/dev/sdb bs=1M