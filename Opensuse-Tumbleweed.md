# Youtube videos not working on Firefox. Install codecs

https://en.opensuse.org/OpenH264

# Distribution upgrade

```
sudo zypper dup
```

# To update OSTW

```
sudo zypper update
```

# Additional Packages

## Codecs / Firefox not playing youtube vidoes

```
sudo zypper install opi
opi codecs
```

## MS Fonts (basic)

```
sudo zypper install fetchmsttfonts
```

# Fonts

```
sudo zypper install google-noto-fonts google-noto-serif-fonts google-noto-coloremoji-fonts google-noto-sans-cjk-fonts
```

## Others

```bash
sudo zypper install patterns-devel-base-devel_basis libvulkan_radeon-32bit kernel-devel v4l2loopback-kmp-default

#reboot for v4l2loopback to get setup properly for OBS virtual camera to work
```

# Codecs

```bash
sudo zypper install ffmpeg gstreamer-plugins-good gstreamer-plugins-bad gstreamer-plugins-ugly gstreamer-plugins-libav libavcodec vlc-codecs
```
