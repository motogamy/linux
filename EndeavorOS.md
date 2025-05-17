# Systemd-boot Quiet

- Run command `sudo nano /etc/kernel/cmdline` and add `quiet` at the begining
- Run `sudo reinstall-kernels`
- Reboot

This will prevent from long list of text being printed on the screen during boot

# KDE Connect setup - fwd entry

Open Firewalld >> select current network from "Connections" section >> for both "public" and "trusted" put a check on KDE Connect from "Service" list

# Numlock on at Startup

`sudo nano /etc/sddm.conf`  and add below lines

```
[General]
InputMethod=
Numlock=on
```

# Add secondary drive/HDD to auto mount without password

- Install disk partition software. For GNOME use gparted or gdisk. For KDE use KDE Partition manager.
- Edit settings of "Edit Mount Settings". For GNOME ones, uncheck the first option, select the mouting option. For KDE, just update the mouting option.

# Emoji Fix on KDE

Install `noto-fonts-emoji` package

# VScode in KDE

Install `visual-studio-code-bin` from AUR by using `yay` command

# Proper implementation of Dark mode in Gnome

Run
`sudo pacman -S xdg-desktop-portal-gnome xdg-desktop-portal`
