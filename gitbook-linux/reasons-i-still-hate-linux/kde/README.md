# KDE

{% hint style="info" %}
_First: KDE is the application suite, **Plasma** is the desktop shell._
{% endhint %}

I installed Plasma yesterday thinking that it was going to solve all my Gnome woes.

Lo and behold, it did!

Plasma felt like a veritable holy grail.

Then I started to run into a different slew of problems.

As wonderful as Plasma and KDE are, the problems I ran into are arguably worse than those in Gnome because they actually make _using_ the computer _impossible_.

Problems I've hit already:

* **KWallet is an absolute headache**, even when I unlock it manually before launching a browser, the browser cannot connect to it (soon enough?) and thus the "secret storage" isn't accessible and none of the login keys are used. All my logged in websites are now logged out, and I use 2FA on all of them.
* **Site preferences are lost in web browsers** (Chromium-based anyway), e.g. YouTube doesn't remember the video size setting or that I've disabled "ambient mode".
* **Audio output doesn't change automatically** when I plug a cable into the headphone jack. Admittedly this problem also exists under Gnome, so it's a problem at the system level, but also I'm under the impression that a desktop shell is able to control that kind of thing and a) it doesn't and b) there isn't a setting for defining a switch rule.
* **Keyboard shortcuts!** Wtf. Default shortcuts work just fine, but some of the shortcut choices are weird and break my muscle memory from Windows. That's fine but at least let me modify them. Well, we can modify shortcuts, but broadly, none of the customised shortcuts work. Actually, _some_ of them _do_ work, somewhat randomly, and also intermittently (as of right now, none of them work). For example:
  * Ctrl+Alt+T launches Konsole, but after replacing the flatpak version with the native package version, it wouldn't work. A reboot resolved this. However, in the meantime, I tried to set Ctrl+Alt+T to launch a custom launcher command, for `konsole`. It straight up didn't work.
  * Meta+E launches Dolphin. I set Meta+Z to do the same and it worked!
  * So I tried Meta+Z to launch my custom command. Nothing.
  * But, Meta+Shift+Z _did_ work for my custom command.
  * Oh but, now, this morning, it doesn't.
  * wtf
  * So I researched it a LOT and it turns out that the global keyboard shortcut settings has been intermittently broken for _**years**_.
* **Gestures** — I've not yet found a decent gesture configuration for Plasma/KDE but I... hope there is one.
* **App store** "Discover" _only_ connects to the Flatpak store (in my Arch installation), which it doesn't inform you if you launch the installation from the "Start" menu in Plasma. That's how I ended up with the flatpak version of Konsole before. Probably Discover connects to other package management systems and probably there's a handle to make it connect to PacMan or Yay, but it didn't OOTB[^1] and it didn't warn me that it was installing a Flatpak. Well at least it isn't fucking Snaps
* **Chrome-based browsers don't restore their windows after logging out.** Plasma's logout signal doesn't send "sigterm" to apps, instead telling apps to "close their windows" or something like that. Therefore, when logging in again, apps (whether launched manually or restored by the desktop shell session restorer) launch into the wrong state. This is primarily visible in Chromium-based browsers (Chrome, Brave) which interpret Plasma's "we're logging out" signal as "close each of your windows" and thus, the browsers' session restore feature only restores the last window that was open. This is a NIGHTMARE.
  * Apparently this is _Chromium_'s fault for not handling the termination signal sent by Plasma correctly. But this doesn't happen in any other desktop shell environment, including Windows, MacOS, Gnome and Hyprland. Possibly they are all doing it "wrong", which is likely tbh, but the end result is that I _keep losing my browser sessions in Plasma and therefore shall not continue to use it_. This is a **fundamental deal-breaker** and I don't understand how this hasn't been handled yet.
* **Clipboard history** is WEIRD and BROKEN. Meta+V opens the clipboard history, like in Windows. Great. It's more featureful than the apology of a clipboard history that they have in Gnome. However, when selecting an item from the history list, _it doesn't do anything_. Actually, it does — it sets it as the current clipboard item, but doesn't actually paste it until you press Ctrl+V. Wtf

[^1]: Out Of The Box
