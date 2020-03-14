# This package is intended for internal usage. You don't have permission to re-distribute it.

# ZheJiang DPTech SSL VPN - Linux Version

Based On: Arch Linux PKGBUILD System

# Disclaimer

This linux version of this software precompiled binary is offered by ZheJiang DPTech, All Copyright Reserved to DPTech.

Only Offer x64 version here. 

**Personally Suggest DO NOT USE THEIR OFFICIAL `install.sh` script, that script will replace your own `openssl` to a relatively old version (0.9.8), since `openssl` is a core component of most linux core software, this behaviour is really dangerous!!!!!! They also replaced your `mxml` library to a relatively old version, and seems it included some breaking changes comparing with newer version. So I added the preloaded `mxml` library to this package.**

So in order to make it can be used, I set it to **depends on**  `openssl098` on AUR and `mxml` library already included in this specific version of package(set to **conflict** with `mxml` Arch official package).

**PLEASE TAKE INTO SERIOUS CONSIDERATION OF USING THIS SOFTWARE!**

# Usage

Usage:

```bash
$ pikaur -S --asdeps openssl098    # To install the openssl 0.9.8 from AUR
$ git clone https://github.com/kmahyyg/dptech_sslvpn_ynu.git
$ makepkg -si
```

After that, modify the **username**, **server**, **port**, **password** inside the config in `/etc/sslvpn.conf`, then run `sudo dpsslvpn -c` to connect.  **The SERVER in config file can only use IP instead of domain name.**

If you wanna disconnect, run `sudo dpsslvpn -d` **twice**.

# License

Custom. Free to Use.

