# Install MS fonts in Fedora

```bash
sudo dnf install curl cabextract xorg-x11-font-utils fontconfig

sudo rpm -i https://downloads.sourceforge.net/project/mscorefonts2/rpms/msttcore-fonts-installer-2.6-1.noarch.rpm

```

# ROCM and ROCM-OPENCL

https://fedoraproject.org/wiki/SIGs/HC#Installation

# Bridge connection for VM - KVM Qemu setup for Fedora

### Install `bridge-utils` package before proceeding

https://www.youtube.com/watch?v=XWC02K9_5Ws

# Font Configuration

Create the below file
`~/.config/fontconfig/conf.d/20-no-embedded.conf`

```jsx
<?xml version="1.0"?>
<!DOCTYPE fontconfig SYSTEM "urn:fontconfig:fonts.dtd">
<fontconfig>
  <match target="font">
    <edit name="embeddedbitmap" mode="assign">
      <bool>false</bool>
    </edit>
  </match>
</fontconfig>
```
