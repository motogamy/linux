# Post Installation

## **Automatic cleaning the package cache**

```bash
sudo pacman -S pacman-contrib
sudo systemctl enable paccache.timer
```

# KVM QEMU VIRT Manager - Virtualization

Refer to the below link: https://gist.github.com/tatumroaquin/c6464e1ccaef40fd098a4f31db61ab22
> ## Internet not working for guest if UFW installed
> Edit `/etc/libvirt/network.conf` and enable firewall_backend = "iptables"

# Pacman Commands

## Remove packages using wildcard in Pacman

```bash
sudo pacman -Rns $(pacman -Qsq <package_name>* )

# replace package_name and make sure to put a * in the end to make it wildcard
```

## Find all pacman packages using wildcard

```bash
pacman -Qsq <package_name>*
```

## Davinci Resolve

Step 1

Install below package

```bash
# Step 1 - run below command 

yay -S rocm-opencl-runtime

# step 2 - 
# Download davici resolve linux vesion, extract it and run the .run file

# step 3 - run below commands

cd /opt/resolve/libs
sudo mkdir disabled-libraries
sudo mv libglib* disabled-libraries
sudo mv libgio* disabled-libraries
sudo mv libgmodule* disabled-libraries
```
