# Desktop UXUI behaviour

{% hint style="success" %}
Please remember to donate to the developers of these extensions if they have helped you in any way! 🙏
{% endhint %}

After all these years, there are still somehow some serious usability bugs in both Gnome and KDE.

As a result, many desktop "extensions" have popped up to fill these (often ridiculous) gaps.

As with all things Linux, there are usually multiple solutions out there, some are more stable but with few features, some are feature-rich but janky and broken, some are amazing, and some are dead, and some are forks & resurrections of ancient projects.

I'll just include one (or two) for each purpose.

Here are the extensions and settings that I'm using to make my desktop experience usable.

## Gnome

### Hot Corners

Gnome uses a "hot corner" in the top left of the screen to activate the "overview" mode, which shows all the open windows and an app dock, plus a tray of all installed desktop (GUI) apps.

When using a second screen on the right side of the main screen, if the screens' top edges align, the hot corner is not included on the second screen. I have no idea why. There are some tweaks you can make in the **dconf Editor** but after a bit of research I found a great extension that allows all kinds of additional settings for custom hot corners.

{% tabs %}
{% tab title="CHC-E — Custom Hot Corners Extended" %}
👣 Install it from here — [extensions.gnome.org/extension/4167/custom-hot-corners-extended](https://extensions.gnome.org/extension/4167/custom-hot-corners-extended/)&#x20;

😸 Check the GitHub — [github.com/G-dH/custom-hot-corners](https://github.com/G-dH/custom-hot-corners)&#x20;
{% endtab %}
{% endtabs %}



### App Indicators, Status, Tray

Gnome got too minimalistic in their design model. As a result, all the apps which have "system tray" indicators — items in the top bar — now have nowhere to go. App developers would be required to rewrite their code in order to have their apps' indicators visible.

No problem — other developers made extensions that add the old-skool app indicators to the Gnome top bar. It supports old Gnome system tray items, AppIndicator items (I believe developed by Canonical/Ubuntu), and KStatusNotifier items (from KDE apps).

{% tabs %}
{% tab title="AppIndicator and KStatusNotifierItem Support" %}
👣 Install it from here — [extensions.gnome.org/extension/615/appindicator-support](https://extensions.gnome.org/extension/615/appindicator-support/)&#x20;

😸 Check the GitHub — -- [github.com/ubuntu/gnome-shell-extension-appindicator](https://github.com/ubuntu/gnome-shell-extension-appindicator)&#x20;
{% endtab %}
{% endtabs %}

_(Gnome has an official "Status Icons" extension but it appears to provide absolutely nothing.)_



### Input Method Panel

Yeah idk why Gnome doesn't have one of these already. Well it does but it doesn't support any solution other than what's built in to the Gnome keyboard layout settings. Which, frankly, are absolutely useless if you need to type anything other than linear alphabets... Like Vietnamese, Chinese, Japanese, Korean, all of the Brahmic scripts (Thai, Burmese, Devanagari, Tamil, Malayalam, etc etc etc). How very Euro-centric...

I'm using Fcitx5 for Vietnamese Telex input, which is powered by UniKey. Fcitx is an Input Method shell (I guess), which basically provides a container and plugin system for existing IMEs. This removes the need for developers to keep building their IMEs for each OS and distribution and OS update — they can just write their IME, and then the IME can connect to Fcitx via a plugin. Fcitx is even available on Android, so you can actually use the original UniKey software via a virtual keyboard inside Android.

The Gnome extension I use is written by a member of the Fcitx community on GitHub. Ironically (or perhaps not ironic any more because it's blindingly clear where Gnome's priorities aren't), the extension integrates KDE's "kimpanel" protocol into Gnome Shell, allowing you to configure Fcitx, set up multiple IME groups, and set your own keyboard shortcuts for switching between keyboard layouts and IMEs.

{% tabs %}
{% tab title="Input Method Panel (kimpanel)" %}
👣 Install it from here — [extensions.gnome.org/extension/261/kimpanel](https://extensions.gnome.org/extension/261/kimpanel/)&#x20;

😸 Check the GitHub — [github.com/wengxt/gnome-shell-extension-kimpanel](https://github.com/wengxt/gnome-shell-extension-kimpanel)&#x20;
{% endtab %}
{% endtabs %}

_Read my guide on configuring Fcitx (or other input methods):_

{% content-ref url="../making-it-work/keyboard/input-methods-fcitx5-asian-languages.md" %}
[input-methods-fcitx5-asian-languages.md](../making-it-work/keyboard/input-methods-fcitx5-asian-languages.md)
{% endcontent-ref %}



### Raise window if app is already running

This is to solve a very specific issue for me. For most people, it probably doesn't even exist. For some people, with very specific workflow methods, it is a key issue.

My issue:&#x20;

I set <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>Escape</kbd> to launch a system monitor app in Gnome. So far so good.

But if the system monitor is already running behind another app, it doesn't pop to the foreground. A small notification appears, which I have to activate by clicking on it, or with a series of keyboard presses. This is horribly slow.

What I want:

To press <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>Escape</kbd> and for the system monitor app to pop into foreground and take the window focus.

Back in the days of X11, a package called `xdo-tool` allowed you to script all kinds of automated interactions with windows. But the new Wayland protocol has a different security model, and as such, programmes like xdo-tool simply can't work. Several great projects existed that were based on xdo-tool, and sadly these all had to be relegated to the rubbish heap.

A modern project, named Run-or-Raise, is a Gnome extension that resurrects this functionality.

It allows you to set as many custom shortcuts as you want, as well as featuring some special modalities. Unlike some lazier projects, this developer has made the effort to actually document their software so that you and I know how to use it.

{% tabs %}
{% tab title="Run or Raise" %}
👣 Install it from here — [extensions.gnome.org/extension/1336/run-or-raise](https://extensions.gnome.org/extension/1336/run-or-raise/)&#x20;

😸 Check the GitHub — [github.com/CZ-NIC/run-or-raise](https://github.com/CZ-NIC/run-or-raise)&#x20;

_The last real release was 2019, but the developer is still updating the Gnome extension code periodically, in order to meet the ever-moving goalposts of Gnome Shell's extension requirements._

_Thank you to_ [_timcharper_](https://github.com/CZ-NIC/run-or-raise/commits?author=timcharper) _and_ [_e3rd_](https://github.com/CZ-NIC/run-or-raise/commits?author=e3rd) 🙏
{% endtab %}
{% endtabs %}



### Gestures

For some indiscernible reason, Gnome's gestures are hard-coded, and all 3-finger gestures are replicated to the 4-finger gestures too.

The only good solution I've found so far is a Gnome extension, which happened to work when I installed it on Gnome 48, but broke just 3 days later when Gnome 49 was released. The developer has released an update to for "gnome 49 support", but their github page says "support only for gnome 45" and the updated extension doesn't work on my computer anyway.&#x20;

Regardless, here's the links to the extension, in case it works for you, and in case the developer manages to fix things up in the future. It really was the best solution I managed to find, and I hope it works again!

{% tabs %}
{% tab title="Window Gestures" %}
👣 Install it from here — [extensions.gnome.org/extension/6343/window-gestures](https://extensions.gnome.org/extension/6343/window-gestures/)&#x20;

😸 Check the GitHub — [github.com/amarullz/windowgestures](https://github.com/amarullz/windowgestures)&#x20;
{% endtab %}
{% endtabs %}

_Read more on my page:_

{% content-ref url="../making-it-work/mouse-and-touchpad/gestures-on-a-touchpad.md" %}
[gestures-on-a-touchpad.md](../making-it-work/mouse-and-touchpad/gestures-on-a-touchpad.md)
{% endcontent-ref %}

