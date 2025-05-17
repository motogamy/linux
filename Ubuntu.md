# Post installation

Install below packages

```bash
sudo apt install ubuntu-restricted-extras
```

# Bridge connection KVM Qemu

https://www.tecmint.com/create-network-bridge-in-ubuntu/#bridgeinstall

# Remove unwanted apt repo source list from Ubuntu

Go to `/etc/apt/sources.list.d` folder and remove all the unnecessary repo files. Do `sudo apt update` once done.

# Static IP for Ubuntu Server 24.04

**Edit the Netplan Configuration File**: Netplan configuration files are stored in `/etc/netplan/`. You will find this file in the `/etc/netplan` directory. It might be named 01-netcfg.yaml or 50-cloud-init.yaml  or something similar, depending on your setup. Open or create a file for editing `sudo nano /etc/netplan/01-netcfg.yaml`

Here’s an example configuration to set a static IP address:

```
network:
  version: 2
  renderer: networkd
  ethernets:
    enp0s3:
      dhcp4: no
      addresses:
        - 192.168.1.10/24
      routes:
        - to: default
          via: 192.168.1.1
      nameservers:
        addresses: [8.8.8.8, 8.8.4.4]

```

Replace ‘enp0s3’ with your interface name. Adjust the IP address, 
subnet mask, default gateway, and DNS servers as necessary for your 
network.
