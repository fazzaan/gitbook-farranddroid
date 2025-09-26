# Windows applications

## Windows software I've tried

<table data-view="cards"><thead><tr><th data-type="content-ref"></th></tr></thead><tbody><tr><td><a href="fontlab-8.md">fontlab-8.md</a></td></tr></tbody></table>

## Options

### Compatibility layers

Wine

WineTricks

Proton (Valve, Steam)

ProtonTricks

ProtonGE

Steam — Major project by Valve to make all Windows games work on Linux, with high performance

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

[^1]: **V**irtual **M**achine
