# Touchpad scroll slower

For some strange reason, scroll speed has been a problem in Wayland _forever_. I last used Linux properly in around 2019 and that was when Wayland was just starting to be used in mainstream distros. Touchpad input was already being handled and controlled by a new framework, _libinput_, and it was unable to handle scrolling properly.

It is honestly beyond me how there are thousands of YouTubers and bloggers posting about switching to Linux every day and I haven't heard a single one of them complain about the touchpad scroll speed. As far as I'm aware, this is a universal problem throughout all Wayland+LibInput systems, _and it is even more pronounced in Chromium-based browsers_. Honestly, the scrolling in _those_ is like it is on aderall.

There is a solution. I don't know how it works but someone made it back in 2021, based on someone else's earlier code. I have no idea why it hasn't been incorporated into the main code. The latest release from this wonderful developer was in 2023. As with most custom code solutions, the only distribution that makes it easy to install is Arch.

## 1. Install the code

### On Arch

* install libinput-config-git from AUR using yay or similar
* go to [step 2 — create the conf file](touchpad-scroll-slower.md#id-2.-create-the-.conf-file)&#x20;

### Not on Arch

* Download the project from here:

[https://gitlab.com/warningnonpotablewater/libinput-config](https://gitlab.com/warningnonpotablewater/libinput-config)&#x20;

* install the project build dependencies:

```
sudo apt install python3-pip ninja-build libinput-dev libudev-dev 
```

```
sudo pip3 install meson
```

* build the source code:

```
meson build
```

```
cd build
```

```
meson configure -Dnon_glibc=true
```

&#x20;\* this one ↑ is perhaps unnecessary but I think it protects you from borking your system and causing it to not even boot up.

```
ninja
```

```
sudo ninja install
```

## 2. Create the .conf file

* create the text file `libinput.conf` in `/etc/`
* put this in it:

```
override-compositor=enabled
scroll-factor=0.075
```

* log out and log back in
* it should work!
* tweak the `scroll-factor` property as you wish. I think it affects the scroll speed immediately, no need to log out and in.

## Uninstalling the code

you can uninstall it later if you need to but you need to keep the build files to do so!

```
cd build
```

```
sudo ninja pre-uninstall uninstall
```



## Sources

* project source code — [https://gitlab.com/warningnonpotablewater/libinput-config](https://gitlab.com/warningnonpotablewater/libinput-config)&#x20;
* AUR package with discussion — [https://aur.archlinux.org/packages/libinput-config-git](https://aur.archlinux.org/packages/libinput-config-git)&#x20;
* arch linux wiki for libinput — [https://wiki.archlinux.org/title/Libinput](https://wiki.archlinux.org/title/Libinput)&#x20;
* wayland freedesktop documentation about libinput — [https://wayland.freedesktop.org/libinput/doc/latest/configuration.html](https://wayland.freedesktop.org/libinput/doc/latest/configuration.html)&#x20;
