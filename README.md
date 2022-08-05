# Kernel-upgrade-in-Amazon-linux-2
Simple steps to upgrade kernel to latest available version in amazon linux 2

Updating Kernel in Amazon Linux server:

To Check current runnig kernel vesrion
```bash
uname -r
```

To list all available kernel version
```bash
rpm -qa kernel
```

To install latest available kernel
```bash
sudo yum install -y kernel
```

To remove old kernel
```bash
sudo yum remove < outdated kernel > 
```

Utility to install new kernel
```bash
sudo yum install binutils -y
```

To set newly installed kernel as default
```bash
rub2-set-default 0 && grub2-mkconfig -o /boot/grub2/grub.cfg 
reboot
```

After reboot verify and remove old kernel
```bash
uname -r
rpm -qa kernel  
sudo yum remove < outdated kernel >
```
