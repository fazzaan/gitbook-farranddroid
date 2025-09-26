# Passthrough Virtualisation

Virtual machines are nothing new, but getting good performance out of them is less simple.

### Passthrough virtualisation

Recent years have brought "passthrough" virtualisation, in which the VM[^1] software enables direct hardware access for the virtual operating system. Modern applications, notably 3D games, graphic rendering and neural networks (machine learning, large language models, "artificial intelligence"), depend on GPU architecture for massive data processing in real-time, so passthrough virtualisation with GPU access is absolutely vital for serious VM solutions and it allows users to run Linux as their primary operating system while still being able to access Windows at full power & performance without rebooting.

### Looking Glass framebuffer replication

In the last couple of years, a new piece of software has been developed which essentially replicates the framebuffer from the VM's GPU into the host's GPU, thereby providing 1-frame-behind-realtime visual access into the VM's graphical output. This is the closest a host machine can come to realtime viewing with currently accessible hardware APIs, although if I understood correctly, Nvidia does have a (currently restricted) API call that allows multi-user access to one framebuffer memory device, which would (I suppose) allow actual realtime viewing of the guest VM's graphical output. This software is called Looking Glass, and is still very early in development. However, it does work already, and it is possible for you to access the code and build a version for yourself, if you want to test it out.

{% embed url="https://www.reddit.com/r/linuxquestions/comments/t3dnkz/can_i_run_my_windows_partition_as_a_vm_in_linux/" %}

{% embed url="https://wiki.archlinux.org/title/PCI_passthrough_via_OVMF#Virtio_disk" %}

{% embed url="https://www.reddit.com/r/VFIO/" %}

{% embed url="https://www.reddit.com/r/VFIO/comments/1nmsszd/kvmfr_in_fedora/" %}

{% embed url="https://www.reddit.com/r/VFIO/comments/1njetxa/single_gpu_passthrough_poor_cpu_performance/" %}

{% embed url="https://www.reddit.com/r/VFIO/comments/1nj0u3p/reliablecurrent_nvidia_single_gpu_passthrough/" %}

I don't know anything about ProxMox so I wouldn't recommend it, but this video demonstrates the approximate method for making an existing Windows installation boot up inside a virtual machine application inside another operating system.

I will have dedicated pages for achieving such things soon.

{% embed url="https://www.youtube.com/watch?v=eFDcCxRS5Xk" %}

{% embed url="https://www.linux-kvm.org/images/b/b3/01x09b-VFIOandYou-small.pdf" %}





[^1]: **V**irtual **M**achine
