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

**Solution:** first when you start your system spam e to get to Systemd-boot menu n cmdline delete aplash and quiet and press f10

after when you boot to sytem  you need go to shell amd 

sudo nano /etc/default/limine
find KERNEL_CMDLINE["linux-cachyos"]="nowatchdog rw rootflags=... plymouth.enable=0"  

and delete aplash and quiet then 

sudo mkinitcpio -P                 
sudo limine-mkinitcpio               
sudo reboot


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

**Last Updated:** February 7, 2026
