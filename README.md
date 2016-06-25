# How to enable UnitedRPMs repository in your system


## 1. Graphical Setup via Firefox web browser

For users of gpk (gnome package kit) or kpackagekit in Fedora that is easy and basically only one step: just click on one of the following files, then follow the default options that Firefox and Package Kit offer by clicking Enter a few times: 


[UnitedRPMs for Fedora 24/25](https://raw.githubusercontent.com/UnitedRPMs/unitedrpms/master/RPM/unitedrpms-24-2.noarch.rpm)



## 2. Command Line Setup using rpm

```
su -c 'dnf -y install https://raw.githubusercontent.com/UnitedRPMs/unitedrpms/master/RPM/unitedrpms-24-2.noarch.rpm'
```

#### How to check if your rpm is compromised?

If you still have the rpm file (above), check its sha512 signature with the command “sha512sum unitedrpms-24-2.noarch.rpm”.
You can verify, the sha512 is the same to:
```
3bfab42f1704f43e2304f8c057a2e6ed01bc8e5527964c0730dbe3401e2ee9a0703e4f87a3c34970b7d0da8993439a33e6abfc14f0d8a5c8cc3519229c718f42
```
Guide how to use [sha512sum](http://docs.oracle.com/cd/E36784_01/html/E36870/sha512sum-1.html)

checksum file which contains all the hash information [Here](https://raw.githubusercontent.com/UnitedRPMs/unitedrpms/master/unitedrpms-CHECKSUM)


## 3. Step by step (expert mode, needs import the GPG key)

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

-----

# FedoraUnited.github.io

# [Website](https://unitedrpms.github.io/)

