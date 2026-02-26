# CachyOS - Fixes and Troubleshooting

This document contains solutions and fixes for common CachyOS issues.

## Table of Contents
- [Installation Issues](#installation-issues)
- [Performance Problems](#performance-problems)
- [Hardware Compatibility](#hardware-compatibility)
- [Software Conflicts](#software-conflicts)
- [Other Issues](#other-issues)

## fixes are random try to find what you want to fix 

### Issue: [probrem with multiple monitors]
**Problem:** [probrem with multiple monitors]

**Solution:** [first when you start your system spam e to get to Systemd-boot menu n cmdline delete aplash and quiet and press f10

after when you boot to sytem  you need go to shell amd 

sudo nano /etc/default/limine
find KERNEL_CMDLINE["linux-cachyos"]="nowatchdog rw rootflags=... plymouth.enable=0"  

and delete aplash and quiet then 

sudo mkinitcpio -P                 
sudo limine-mkinitcpio               
sudo reboot
]

---

## disk dipaer from mount

### Issue: [disk dipaer from mount]
**Problem:** [title]

**Solution:** [

1 step 
use in conslone/shell/(or what is name of thle conmmand line)  ** lsblk -f **
to know that disk you have and there uuid (just ignote zram pls ) 

2 step
check the hooks for fun  ** lsblk -f ** cat /etc/mkinitcpio.conf | grep -A 5 HOOKS **
then go to sudo nano /etc/mkinitcpio.conf and add to hookd with dont has # in fornt and add mdadm_udev 
shud looks like this 
"HOOKS=(base systemd autodetect microcode kms modconf block mdadm_udev keyboard sd-vconsole plymouth filesystems fsck)"
or copy it i dont cake 

2.5 shot of apsitne 

3 then 
regenere mkinitcpio
" sudo mkinitcpio -P "
somme in long there will be " Custom /etc/mdadm.conf file will be used in initramfs for assembling arrays. "

4 reboot 

5 

]

---
## this is temate for me 

### Issue: [Title]
**Problem:** [Description of the issue]

**Solution:** [Steps to fix]

---

## Additional Resources

- [CachyOS Official Website](https://cachyos.org/)
- [Community Forum](https://discuss.cachyos.org/)
- [GitHub Issues](https://github.com/CachyOS/linux-cachyos/issues)

---
i know why i dirnk apsinte
**Last Updated:** February 26, 2026
