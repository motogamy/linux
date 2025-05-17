# How to install Microsoft fonts on Debian

https://linuxcapable.com/how-to-install-microsoft-fonts-on-debian-linux/

```bash
sudo apt update && sudo apt upgrade
sudo apt-add-repository contrib non-free -y # Only if its not activated earlier
sudo apt install software-properties-common -y
sudo apt install ttf-mscorefonts-installer

```

# **Installing Multimedia Codecs (and VLC)**

For installing multimedia codecs and VLC, the following command was used:

```
sudo apt install -t bookworm-backports libavcodec-extra vlc
```

## Remove ibus and uim toolbar

```jsx
sudo apt remove --purge ibus*
sudo apt remove uim-mozc im-config
```

## V4l2loopback

```bash
sudo apt install linux-headers-$(uname -r)
wget http://ftp.us.debian.org/debian/pool/main/v/v4l2loopback/v4l2loopback-dkms_0.13.2-1_all.deb
sudo dpkg -i v4l2loopback-dkms_0.13.2-1_all.deb
```
