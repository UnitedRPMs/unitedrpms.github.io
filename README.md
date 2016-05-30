# FedoraUnited.github.io

# [Website](https://unitedrpms.github.io/)

### How to enable UnitedRPMs repository in your system

Run this code in your console from superuser:

```
# dnf config-manager --add-repo=https://raw.githubusercontent.com/UnitedRPMs/unitedrpms.github.io/master/unitedrpms.repo
```

**Important: import and verify the GPG key:**

```
# rpm --import https://raw.githubusercontent.com/UnitedRPMs/unitedrpms.github.io/master/URPMS-GPG-PUBLICKEY-Fedora-24
```

Now you can install the packages:

```
# dnf update
# dnf install vlc mpv ffmpeg gnome-mpv
```

How to install all GStreamer codecs:
```
# dnf install gstreamer{1,}-{ffmpeg,libav,plugins-{good,ugly,bad{,-free,-nonfree}}} --setopt=strict=0
```
