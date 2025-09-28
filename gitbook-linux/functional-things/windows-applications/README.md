# Windows applications

## Windows software I've tried

<table data-view="cards"><thead><tr><th data-type="content-ref"></th></tr></thead><tbody><tr><td><a href="fontlab-8.md">fontlab-8.md</a></td></tr></tbody></table>

## Options

### Compatibility layers

#### Wine

* Wine
* WineTricks

#### Proton & Steam

Proton is (I think) a derivative of Wine that has been developed by Valve, to make all Windows games work on Linux, with high performance and native-like function.

The Proton layer can be used to run non-game applications too, although this isn't widely tested and things will likely not work exactly right.

* Proton (Valve, Steam)
* ProtonTricks
* ProtonGE

#### WinApps

I haven't used this yet but it looks like a reasonable way to run virtualised Windows software inside Linux.

1. Runs Windows in a Docker, Podman or libvirt virtual machine
2. Creates shortcuts to selected Windows applications on the host GNU/Linux OS
3. Uses [FreeRDP](https://www.freerdp.com/) as a backend to seamlessly render Windows applications alongside GNU/Linux applications.

Link: [github.com/winapps-org/winapps](https://github.com/winapps-org/winapps)&#x20;

### Virtualisation

Virtual machines are nothing new, but getting good performance out of them is less simple.

Recent years have brought "passthrough" virtualisation, in which the VM[^1] software enables direct hardware access for the virtual operating system. In the last couple of years, a new piece of software has been developed which essentially replicates the framebuffer from the VM's GPU into the host's GPU, thereby providing 1-frame-behind-realtime visual access into the VM's graphical output.&#x20;

{% content-ref url="../../hard-things/passthrough-virtualisation.md" %}
[passthrough-virtualisation.md](../../hard-things/passthrough-virtualisation.md)
{% endcontent-ref %}

Virtual machine applications:

* VirtualBox
* QEMU
* Gnome Boxes
* idk actually, it's been years since I used virtual machines. I'll add things to this list later when I'm undertaking this adventure.



## Links

{% embed url="https://www.reddit.com/r/linux4noobs/comments/1khzhhp/this_is_how_to_use_windows_programs_on_linux/" %}

[^1]: **V**irtual **M**achine
