# Custom Atomic Image "Azurite Lite"

This is my personal atomic image that I use to build my own flavor of [Fedora Kinoite](https://fedoraproject.org/atomic-desktops/kinoite/) (KDE Atomic). I have taken the latest (Version 42, as of right now) Kinoite image, removed some unused items, and layered useful tools such as:

- Distrobox
- QEMU, libVirt, and virt-manager
- Borg Backup and UI
- Logitech Tools for Keyboard and Mouse
- KDE PIM
- Custom Wallpapers from Bluefin (I really like the dinosaurs)

In addition, a setup script (that sometimes fails when first starting) will install flathub, and then add a few packages that I use from day to day.

I was inspired by, and used (*ahem* stole), the setup from [Jorge Castro](https://www.ypsidanger.com), based on his post [here](https://www.ypsidanger.com/building-your-own-fedora-silverblue-image/). As such, feel free to take this work and build your own. If you'd like to just use this image, without any support, guarantees, or warranty, you can do the following:

First, do an install of the latest version of Kinoite or Silverblue (Kinoite is suggested), and perform a full update:

```
rpm-ostree update
systemctl reboot
```

Then you can rebase to this untrusted image:
```
rpm-ostree rebase ostree-unverified-registry:ghcr.io/jcrawford813/azurite-lite-jc:42
systemctl reboot
```

Note that all of the above need to be done as root.

The Action rebuilds the image every night, so it should remain relatively up-to-date. I will change the image from time to time based on my personal needs.