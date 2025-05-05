# Linux on Windows - WSL2

* WSL2 installation guide — what to _not_ do too
* WSL2 uninstallation & removal guide — sometimes it gets installed and stuck in ways that won't go away



## Uninstalling & Removing WSL2

In the end I just had to delete some of the system files because they wouldn't go away.

I do NOT RECOMMEND THIS cos it's dangerous but basically you're gonna have to take full control of the WSL2 system files and then delete them.



Still got "Linux" stuck in the File Explorer sidebar?

* Open your registry editor (I recommend [Registry Finder](https://app.gitbook.com/s/SvMwDma3YIsN6hmiEFs1/windows-configuration/third-party-apps/registry-editors))
* Go to `HKEY_`<mark style="color:red;">`LOCAL_MACHINE`</mark>`\SOFTWARE\Classes\CLSID{B2B4A4D1-2754-4140-A2EB-9A76D9D7CDC6}` or `HKEY_`<mark style="color:red;">`CURRENT_USER`</mark>`\Software\Classes\CLSID{B2B4A4D1-2754-4140-A2EB-9A76D9D7CDC6}`&#x20;
* Set `System.IsPinnedToNameSpaceTree` to `0`&#x20;
* You can probably delete the whole CLSID key tbh but don't take my word for it.
