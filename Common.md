# Root account is locked after updating FSTAB

From boot options select the OS and press `e` to open the boot command. Add `init=/bin/bash` in the end and you will be able to boot with console.

Remove the additional drives entry by running `sudo nano /etc/fstab` and reboot.

# Lutris epic games install Error 256 due to fonts installation

Download fonts from [here](https://sourceforge.net/projects/corefonts/files/the%20fonts/final/) and copy/past them in `home/sajeesh/.cache/winetricks/corefonts` and the restart the installation

# Check File and Folder size on Ubuntu Terminal

Install ncdu `sudo apt install ncdu`

Run `ncdu -x /`

## Full wipe or format disk

Usefull while installing Arch via archinstall and it is throwing errors

`sudo wipefs --all --force --backup /dev/vdb`

Post that format nvme disk to btrfs by running

`mkfs.btrfs /dev/nvme0n1`

## Change Global theme and icons for GTK in Gnome

Copy the theme and icon by running following commands

`cp -r <theme-name> /usr/share/themes`

`cp -r <icons-name> /usr/share/icons`

## KVM QEMU Virt-Manager setup

https://youtu.be/7tqKBy9r9b4?si=89ZWWiscIz2MctWW

## Dark theme for KDE applications (Kdenlive / Okular) in GNOME

Install Plasma breeze `sudo dnf install plasma-breeze` or `yay breeze` for Arch

# Calibri font download

https://github.com/jondot/dotfiles/blob/master/.fonts/calibri.ttf

# Fix top bar icons of flatpak application

- Right click top bar of app
- More actions >> configure special window setting
- Add property
- In search write desktop and select Desktop file name
- Now search app in the start menu, right click >> edit application >> copy the app name “com.bitwarden.desktop”
- Paste it in the previous screen againt desktop file name
