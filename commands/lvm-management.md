# LVM Management

## Resize Virtual Machine Drive

Resize the VM drive in the VM software

Then run the following in the console

    sudo fdisk --list

If the next command mentions fixing an error, fix it

    sudo parted /dev/sda resizepart 3 100%

    sudo partx -u /dev/sda
    
    sudo pvresize /dev/sda3
    
    sudo lvextend -r -l +100%FREE /dev/mapper/ubuntu--vg-ubuntu--lv
