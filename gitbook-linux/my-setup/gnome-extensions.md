# Gnome extensions

As polished as Gnome is nowadays, there are a tonne of things missing from it.

The devs say that that's by design, and that you can customise it to your preferences & needs with the Gnome Extensions.

However, every Gnome update manages to introduce changes that break most extensions.

That being said, here are the extensions I use.

{% hint style="info" %}
Links will take you to the GitHub or GitLab location, because who knows when an extension might get removed from the Gnome Extensions store?
{% endhint %}

_Click on the name to see details on this page, or click the GitHub link to go to their repo page._

* [#appindicator-and-kstatusnotifieritem-support](gnome-extensions.md#appindicator-and-kstatusnotifieritem-support "mention") — [**GitHub**](https://github.com/ubuntu/gnome-shell-extension-appindicator)&#x20;
* [#chc-e-custom-hot-corners-extended](gnome-extensions.md#chc-e-custom-hot-corners-extended "mention") — [**GitHub**](https://github.com/G-dH/custom-hot-corners-extended)&#x20;
* [#clipboard-indicator](gnome-extensions.md#clipboard-indicator "mention") — [**GitHub**](https://github.com/Tudmotu/gnome-shell-extension-clipboard-indicator)&#x20;
* [#dash-to-panel-or-dash-to-dock](gnome-extensions.md#dash-to-panel-or-dash-to-dock "mention") — [**GitHub**](https://github.com/home-sweet-gnome/dash-to-panel)&#x20;
* [#disconnect-from-wifi](gnome-extensions.md#disconnect-from-wifi "mention") — [**GitHub**](https://github.com/kgshank/gse-disconnect-wifi)&#x20;
* [#emoji-copy](gnome-extensions.md#emoji-copy "mention") — [**GitHub**](https://github.com/felipeftn/emoji-copy)&#x20;
* [#impatience](gnome-extensions.md#impatience "mention") — [**GitHub**](https://github.com/timbertson/gnome-shell-impatience)&#x20;
* [#input-method-panel](gnome-extensions.md#input-method-panel "mention") — [**GitHub**](https://github.com/wengxt/gnome-shell-extension-kimpanel)&#x20;
* [#lilypad](gnome-extensions.md#lilypad "mention") — [**GitHub**](https://github.com/shendrew/Lilypad)&#x20;
* [#quick-settings-tweaks](gnome-extensions.md#quick-settings-tweaks "mention") — [**GitHub**](https://github.com/qwreey/quick-settings-tweaks)&#x20;
* [#run-or-raise](gnome-extensions.md#run-or-raise "mention") — [**GitHub**](https://github.com/CZ-NIC/run-or-raise)&#x20;
* [#tiling-assistant](gnome-extensions.md#tiling-assistant "mention") — [**GitHub**](https://github.com/Leleat/Tiling-Assistant)&#x20;
* [#touchpad-gesture-customization](gnome-extensions.md#touchpad-gesture-customization "mention") — [**GitHub**](https://github.com/HieuTNg/touchpad-gesture-customization)&#x20;
* [#transparent-window-v2](gnome-extensions.md#transparent-window-v2 "mention") — [**GitHub**](https://github.com/pbxqdown/gnome-shell-extension-transparent-window/tree/transparent-window-v2)&#x20;
* [#light-style](gnome-extensions.md#light-style "mention") (built-in)&#x20;
* [#system-monitor](gnome-extensions.md#system-monitor "mention") (built-in)&#x20;
* [#window-navigator](gnome-extensions.md#window-navigator "mention") (built-in)&#x20;

{% hint style="success" %}
And, finally, [**Save Desktop**](https://github.com/vikdevelop/SaveDesktop). It's an app, not an extension, but its primary purpose is to back up all your desktop settings, including extensions, wallpapers, and other settings.
{% endhint %}

## More details

### [AppIndicator and KStatusNotifierItem Support](https://github.com/ubuntu/gnome-shell-extension-appindicator)

Absolutely necessary if you use any apps that have system tray indicators. Somehow (?) the Gnome devs forgot to include support for this. This extension literally imports the function from KDE and Ubuntu.

### [CHC-E (Custom Hot Corners - Extended)](https://github.com/G-dH/custom-hot-corners-extended)

Gnome Shell is famous for its hot corner: hitting the top-left corner with your mouse cursor activates the overview, exposing open windows and an app launcher dock. However, this hot corner does not work on second monitors — and indeed, if you add a monitor to the left of your primary display, the hot corner moves to the _far left corner_. Obviously ridiculous and obviously an oversight, the devs left it to _someone else_ to create an extension to solve this bug. CHC allows customisation of the hot corners, and CHC-E brings more features. I now have three hot corners.

### [Clipboard Indicator](https://github.com/Tudmotu/gnome-shell-extension-clipboard-indicator)

This indicator gives you access to the last x number of Ctrl+C copies you made, a la Windows's Win+V shortcut. It doesn't always work perfectly, but I think the bugs are not in this extension but actually within the apps and how they handle clipboard interaction.

### [Dash to Panel](https://github.com/home-sweet-gnome/dash-to-panel) (or [Dash to Dock](https://github.com/micheleg/dash-to-dock))

[**Dash to Panel**](https://github.com/home-sweet-gnome/dash-to-panel) and [Dash to Dock](https://github.com/micheleg/dash-to-dock) offer similar functionality, although Dash to Panel appears to be far superior in terms of customisability (which makes sense, because it was originally developed by Zorin OS). The only problem I've seen so far is that the font colour is hard to make out when changing between the Dash Overview and the desktop view, and the same case when changing between Light and Dark modes, although this is only when using the "Light Style" Gnome extension that makes the top panel and panel menus use a light theme style.

### [Disconnect from WiFi](https://github.com/kgshank/gse-disconnect-wifi)

Yeah, this really isn't built into Gnome. There is no way to disconnect from a WiFi network without either choosing a new one or disabling your WiFi.

### [Emoji Copy](https://github.com/felipeftn/emoji-copy)

An emoji input panel that works regardless of what app you're in. The system-level inputs are always difficult to sort out properly, because of various teething incompatibilities between display manager (Wayland, X, XWayland, KWin), desktop shell (Gnome, KDE, Hyprland etc), input method (desktop's own, ibus, fcitx5, etc), the app you're trying to use (notable issues with chromium, electron, wine, qt under gnome, gnome under qt), _and_ idk what else but basically it's complicated and messy and you're better off using a desktop shell extension that resides at the user level. **Note that** Emoji Copy works by copying the chosen emoji into your clipboard and pasting it immediately (sometimes doesn't work), so this will replace your most-recently-copied clipboard item.

### [Impatience](https://github.com/timbertson/gnome-shell-impatience)

I just use this to slow down the animations slightly. No reason other than I like to see the animations more slowly, which can (sometimes) serve to make me slow down in my mind. **Note that** Gnome's method of handling keyboard inputs as shell function shortcuts seems to depend upon the current state of the animation, which behaves a bit unexpectedly if you make the interface animations _slower_.

### [Input Method Panel](https://github.com/wengxt/gnome-shell-extension-kimpanel)

As with all other Gnome problems, the _fundamentally necessary_ component of typing _any language that doesn't use a simple linear input mode — **so that'd be languages used by several BILLION PEOPLE** (Chinese, Japanese, Korean, Hindi, Indic languages, Brahmic languages, etc etc etc)_ — the language input method panel, **is simply not available in Gnome**. Some kind soul has written an extension to support the one from KDE, _kimpanel_, thankfully. Good job, Gnome Devs. How very White Patriarchal Colonialist of you.

### [Lilypad](https://github.com/shendrew/Lilypad)

Because, yet again, Gnome itself is lacking in settings, so there's literally no way to re-organise the panel menu items. Lilypad mostly works fine.

### [Quick Settings Tweaks](https://github.com/qwreey/quick-settings-tweaks)

Because — you guessed it — Gnome has no settings for this. This extension allows tweaking of the Quick Settings panel and the Notifications-Date-Time panel. The defaults are "fine" as long as you don't actually _have_ any items in your calendar — if you do, the schedule section is literally too long for the screen. And if you have the Weather app installed, it'll appear here too, on the long side of the panel. This extension lets you move stuff around a bit. It also lets you add things like the media transport widget to the menu and a per-app volume control which connects to the system's per-app volume control.

### [Run or Raise](https://github.com/CZ-NIC/run-or-raise)

If you bind a keyboard shortcut to an application and press it when the application is already running, it will either launch a new instance if the app allows it, or — it will do absolutely nothing. This is stupid af. I bound <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>Esc</kbd> to the system monitor. Run or Raise fixes this stupidity by checking if the app is already running, launching it if it's not, and switching to it if it is. There are a few other parameters you can set too, like choosing if the workspace switches to the location of the app or if the app comes to your location. It is a bit more manual than other extensions, but read the guide and you'll be fine.

### [Tiling Assistant](https://github.com/Leleat/Tiling-Assistant)

Guess what? This enables basic tiling features — snapping windows into quarters — that Windows has had for literally more than 12 years, since Windows 8.1. Linux has also had it since 2014.

### [Touchpad Gesture Customization](https://github.com/HieuTNg/touchpad-gesture-customization)

Finally an extension that actually brings proper gesture support and functionality to Gnome! There have been a variety of apps and extensions in the past, but I only had limited success with each of them, and all got broken after a Gnome update. This one works perfectly on one laptop, running CachyOS, but the overview and workspace switching doesn't work on my Garuda. Not sure if this is due to a conflict with other extensions though — I'll test it out.

### [Transparent Window](https://github.com/pbxqdown/gnome-shell-extension-transparent-window/tree/transparent-window-v2) (v2)

This makes the current window transparent when you click on the item in the Gnome panel. Unfortunately it's not very convenient, as you can only set a transparency percentage in the Extension Settings window and then use that percentage every time. I used to use customisable window transparency all the time in Windows, with the application AltSnap, but unfortunately this hasn't yet been achieved in Wayland (in Gnome anyway).

### Light Style

Light Style is built-in to Gnome's own extensions package. This provides a light theme style for the Gnome panel and panel menus. Idk why this isn't built into Gnome's settings.

### System Monitor

System Monitor is built-in to Gnome's own extensions package. This is a pretty handy way to quickly see the usage of your CPU, RAM, and upload & download speeds. There are other extensions but I found them to be too complicated or heavy, or take up too much horizontal space.

### Window Navigator

Window Navigator is built-in to Gnome's own extensions package. This allows you to use the dash overview with keyboard shortcuts, by selecting windows using <kbd>Alt</kbd>+number and workspaces using <kbd>Ctrl</kbd>+number.

### [Save Desktop](https://github.com/vikdevelop/SaveDesktop)

{% hint style="success" %}
And, finally, [**Save Desktop**](https://github.com/vikdevelop/SaveDesktop). It's an app, not an extension, but its primary purpose is to back up all your desktop settings, including extensions, wallpapers, and other settings such as those managed by dconf keys. I have installed it but I haven't tested how well it transfers between computers yet. It's available as a flatpak on Flathub, but if you're using Arch then it's also available in the repos (perhaps AUR; I can't check cos the AUR is down while I'm writing this).
{% endhint %}

