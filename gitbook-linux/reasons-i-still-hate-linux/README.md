# Reasons I still Hate Linux

_inb4 if you don't like something then fix it:_

_**shut up.**_



on the light side, I'm also going to use this site as a place to explore & record the solutions that I've found. Needless to say, most of them will probably become out of date and invalid after a few weeks.

**that aside,**

## Reasons that Linux is Still Shite

I've been away from Linux for 6+ years.

I used to use it as my main driver, from age 11 to age \~23.

Now it is 2025.

Today (21st September 2025), I decided to install Linux on my second cheapy laptop. I bought it second-hand last year when my real laptop's screen finally bit the dust, but it's really just not strong enough to run Windows 11 these days. I spent weeks trying to decrease the system load to make it run better, but tbh I haven't tried the variety of "debloated" Windowses. Honestly I only use Windows because I need MS Office and Photoshop (amongst other apps), which (last I checked) still run like Jank on Wine, Proton[^1] etc.&#x20;

So today I took the plunge and installed Garuda Linux, a branch of customised Arch btw, and so far it's doing great. However.:

Here is a list of shitty things that STILL DON'T WORK PROPERLY:  

* AUDIO VOLUME IS JUST TOO QUIET ON MY LAPTOP
  * No fix yet; seems like the generic audio driver cannot detect all of the speakers in the laptop.
* TOUCHPAD SCROLLING IS WAY TOO FAST
  * "Fixed" with libinput-conf-git package. Chromium/Electron still handles scrolling in its own way, so you have to strike a happy medium between too-slow in apps and too-fast in Chromium/Electron apps.  
* TOUCHPAD SCROLLING IN CHROMIUM
  * Unreasonably fast, no idea why this is.
* CHROM/IUM DOESN'T HAVE MIDDLE-CLICK SCROLL
  * There is a Chromium flag you can enable.
* GOOGLE DRIVE STILL DOESN'T HAVE A NATIVE SYNC APP
  * No solution still. You can connect using your desktop environment (Gnome, KDE etc)'s file browser app, but the files & directory structure are not synced to your local drive, so accessing things is *always* slow, and you can't edit (or even access) files when your internet is slow or disconnected. This is Google's fault, but also the Linux file manager sync services could/should provide actual file syncing to a local cache.
* INPUT METHOD CONFIGURATION IS HORRIFYING
  * No excuse for this. Quick research will indicate that it's because of Wayland, but deeper research reveals that Wayland actually has IME protocols and it's actually (surprise surprise) (mainly) Gnome which doesn't support Wayland's protocols. Well it's not like billions of people around the world need to write in languages which need an IME, right?
* SWITCHING IME TOO FAST ACTIVATES OTHER SHORTCUTS
* CUSTOM GESTURES REQUIRES SPECIFIC COMMAND LINE
  * 
* GESTURE IMPROVEMENTS ARE ONLY AVAILABLE AS AN EXTENSION FOR A DESKTOP SHELL (GNOME)
  * _And this extension got broken by a Gnome update._
* MY WIFI IS HALF THE SPEED I GET ON WINDOWS
  * This is inconsistent and also seems to depend which laptop I'm using, so it may be hardware driver-dependent.
* CHANGING THEME (sometimes) CAUSES ADMIN-RELATED GTK APPS TO CRASH
* GTK HAS REMOVED CTRL+TAB FOR TAB SWITCHING, REPLACED IT WITH ALT+NUMBER, 
  * AND CTRL+TAB MOVES FOCUS SO THAT ALT+NUMBER DOESN'T EVEN WORK
    * This specific description applies to gedit (not gnome text editor) so it's kinda irrelevant now but it still underscores a continuous deprecation of consistent & predictable usability in Gnome. Qt/KDE still supports Ctrl+Tab for changing tabs in native apps, which really should be preserved forever because this is how web browsers work and how Windows works. Windows has better tab-switching than Gnome. What the heck?
* SNAPPED WINDOW GROUPS STILL DON'T EXIST
  * There's an extension for this which is pretty good, it even handles split-screen resizing of the snapped app windows.
* GNOME DEVELOPERS KEEP MAKING EXTREMELY OPINIONATED DESIGN CHOICES AND REMOVING USER OPTIONS 
  * Like removing the Up button in the Files app
  * Like, Gnome Shell is a Mutter plugin, and Mutter is a Wayland plugin. All GUI applications run as child processes of Gnome Shell. So if Wayland crashes, everything crashes. If you need to restart Wayland, you restart everything. Who the fuck designed this.
* MOUSE CURSOR SIZE CANNOT BE INCREASED IN WAYLAND
  * It can if you edit dconf/gsettings, but why do I have to do this in such a hacky way? Is it really that hard or undesirable to put a simple slider setting in the system settings panel?
* SYSTEM EMOJI PICKER PANEL DOESN'T WORK IN CHROME AND OTHER NON-NATIVE UI APPS
* GNOME SHELL EXTENSIONS CANNOT BE INSTALLED IN GNOME'S OWN WEB BROWSER
* GNOME DOESN'T UNMOUNT VIRTUAL DRIVE FOLDERS AFTER THE SYSTEM UNMOUNTS THE DRIVE

(if this is specific to my system then it shouldn't be)

* ##
Do you understand yet why Normal People are never going to use Linux?

[^1]: The Proton compatibility layer developed by/with Valve (Steam), not Proton the digital security services.
