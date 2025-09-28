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

* [https://www.reddit.com/r/linuxquestions/comments/t3dnkz/can\_i\_run\_my\_windows\_partition\_as\_a\_vm\_in\_linux/](https://www.reddit.com/r/linuxquestions/comments/t3dnkz/can_i_run_my_windows_partition_as_a_vm_in_linux/)&#x20;
* [https://wiki.archlinux.org/title/PCI\_passthrough\_via\_OVMF#Virtio\_disk](https://wiki.archlinux.org/title/PCI_passthrough_via_OVMF#Virtio_disk)&#x20;
* [https://www.linux-kvm.org/images/b/b3/01x09b-VFIOandYou-small.pdf](https://www.linux-kvm.org/images/b/b3/01x09b-VFIOandYou-small.pdf)&#x20;
* [https://www.reddit.com/r/VFIO/](https://www.reddit.com/r/VFIO/)&#x20;
* [https://www.reddit.com/r/VFIO/comments/1nmsszd/kvmfr\_in\_fedora/](https://www.reddit.com/r/VFIO/comments/1nmsszd/kvmfr_in_fedora/)&#x20;
* [https://www.reddit.com/r/VFIO/comments/1njetxa/single\_gpu\_passthrough\_poor\_cpu\_performance/](https://www.reddit.com/r/VFIO/comments/1njetxa/single_gpu_passthrough_poor_cpu_performance/)&#x20;
* [https://www.reddit.com/r/VFIO/comments/1nj0u3p/reliablecurrent\_nvidia\_single\_gpu\_passthrough/](https://www.reddit.com/r/VFIO/comments/1nj0u3p/reliablecurrent_nvidia_single_gpu_passthrough/)&#x20;
*

[^1]: **V**irtual **M**achine
