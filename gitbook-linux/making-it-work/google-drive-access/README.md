# Google Drive access

So there truly seems to be no free way to have a _**synchronising**_ Google Drive solution.

You can "stream" it though, via what is essentially a network drive.

This isn't great, because there isn't a dedicated cache of recent or selected files.

It's not very elegant, it has a bunch of issues which would be associated with a network drive.

It shouldn't have, but there we go.

Google, who make A VARIETY OF LINUX-BASED OPERATING SYSTEMS USED BY THE ENTIRE PLANET, AND USE LINUX INTERNALLY, ARE INCAPABLE OF MAKING A LINUX CLIENT FOR THEIR OWN CLOUD STORAGE SYNC SERVICE, GOOGLE DRIVE.



There are somewhat-shoddy solutions, and they're different for different desktop shells...

* **rclone** — rather manual, connects to your file system, but you have to configure a lot of stuff and some things don't seem to work unless you pay someone (but I think that was for proton drive access, not google drive).
* **Gnome** — it kinda works already but the files are not _synced_ per se, so you can't access cached files when the network is down or unstable like you can in the official sync app on Windows and MacOS.
* **KDE** — the integration appears to be a bit smoother than in Gnome but guess what? Google broke their key access, and have made the developer verification process way more complicated. So it's technically Google's fault, as FOSS developers don't really have the impetus to keep jumping through arbitrarily complex hoops designated by one of the largest monopolistic corporations that are destroying the free world.
* Set up your own ClientID for your own Google account and put it into the Google Account connection configuration file. This should allow you to connect to Google Drive in file browsers in KDE, apps which use the `kio-gdrive` backend.&#x20;
