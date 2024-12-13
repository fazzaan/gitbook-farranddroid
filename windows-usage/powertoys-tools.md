# PowerToys Tools

PowerToys is an amazing set of freeware tools to extend and improve your experience of Windows.

The tools are intended for any kind of user who wants to customize their computer usage for specific purposes, and it goes a long way for making Linux users feel more at home.

I use several of the tools on a daily basis, they are indispensible to my workflow.

* [Color Picker ↴](powertoys-tools.md#color-picker)
* [Keyboard Manager ↴](powertoys-tools.md#keyboard-manager) — remapping keys and shortcuts.
* [Always On Top ↴](powertoys-tools.md#always-on-top) — keey selected windows on top.
* [Awake ↴](powertoys-tools.md#awake) — keep the computer awake.
* Mouse Without Borders ↴ — Share your mouse _and keyboard_ with another computer.

Others I use occasionally:

* Advanced Paste — features mainly useful for developers.
* FancyZones (largely deprecated by Windows 11's new snapping features)
* File Locksmith — for discovering which apps/processes are using a file and gaining access to it.
* Image Resizer
* Peek
* PowerRename — batch-rename files using rules, patterns and RegEx.
* PowerToys Run (like MacOS's Spotlight and Linux desktops' launchers.)
* Screen Ruler
* Text Extractor (you are recommended to use the text extraction feature in Snipping Tool instead.)

***

## Color Picker

I use Color Picker for my graphic design work.

Press 🪟+Shift+C to launch Color Picker.

<figure><img src="../.gitbook/assets/image (6) (1).png" alt=""><figcaption></figcaption></figure>

Its settings page allows you to enable a wide range of colour format, as well as define your own.

<figure><img src="../.gitbook/assets/image (7) (1).png" alt="" width="563"><figcaption></figcaption></figure>

***

## Keyboard Manager

Keyboard Manager can be used to remap keys to send different key signals, and to remap shortcuts to send different shortcuts.

I use Keyboard Manager to re-map the arithmetic keys (+, -, /, \*) to Home/End/PgUp/PgDn, as my laptop doesn't have dedicated keys for these keys.

I also use it to remap several shortcut sequences:&#x20;

<table data-full-width="true"><thead><tr><th width="174">New</th><th width="128">Standard</th><th>Function</th><th>Reason</th></tr></thead><tbody><tr><td><code>🪟+A</code></td><td><code>🪟+N</code></td><td>Open the Windows notification tray</td><td></td></tr><tr><td><code>🪟+S</code></td><td><code>🪟+A</code></td><td>Open the Windows Quick Settings panel</td><td></td></tr><tr><td><code>🪟+Z</code></td><td>Menu key</td><td>Open the context menu wherever the cursor or focus is</td><td>No context menu key on most modern keyboards, but the context menu has lots of mnemonic keys.</td></tr><tr><td><code>Ctrl+Shift+Z</code></td><td><code>Ctrl+Y</code></td><td>Redo</td><td>Should be "Redo" in every app but Microsoft disagrees. Some apps use  Ctrl+Y for a different function: you can choose which apps to alter in the config.</td></tr><tr><td><code>Ctrl+W</code></td><td><code>Alt+F4</code></td><td>Close window</td><td>Some apps refuse to use Ctrl+W for closing, like FB's Messenger app.</td></tr></tbody></table>

***

## Always On Top

<mark style="color:yellow;">`🪟+Ctrl+T`</mark> is the shortcut to pin a window on top of all the others.

A pinned window will also have a thick border outlining it, which you can customize.

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

***

## Awake

Sometimes I stream media from my laptop to my TV or Android devices, but the media software doesn't keep Windows awake. There are numerous other reasons to keep your computer awake too! You can use this PowerToys module to keep your computer awake indefinitely, for a time interval, or until a specific expiration time.

Check out the screenshots below to see how you can configure Awake to work for you.

<figure><img src="../.gitbook/assets/image (1) (1) (1) (1) (1).png" alt=""><figcaption><p>Awake modes</p></figcaption></figure>

<figure><img src="../.gitbook/assets/image (2) (1) (1).png" alt=""><figcaption><p>Awake for time interval setting</p></figcaption></figure>

<figure><img src="../.gitbook/assets/image (3) (1) (1).png" alt=""><figcaption><p>Awake until expiration settings</p></figcaption></figure>

<figure><img src="../.gitbook/assets/image (4) (1) (1).png" alt=""><figcaption><p>Choose if the screen should stay on or not</p></figcaption></figure>

***

## Mouse Without Borders

This module is honestly incredible!

I just had to buy a second laptop because my primary machine is starting to break 😢 The screen cable is damaged so sometimes the screen flickers. I decided to stop driving around with it in my backpack.&#x20;

My new laptop is a very cheap, refurbished laptop, so it's not powerful enough for my regular work, which includes Photoshop and Blender and DaVinci and BitWig, all of which are rather heavy to run.

So now I find myself sometimes needing to use two laptops at the same time 🤨

_How did we come to this..._

Anyway,

I'll post some screenshots and explanations of my setup soon.

But the settings page is really quite self-explanatory. Some of the settings automatically sync between the connected machines.

Here you can see its Behaviour settings:

<figure><img src="../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

It even captures my custom touchpad gestures!

Well, the gestures which invoke keyboard shortcuts — which I can see is the case, because the remote touchpad can control administrator windows, whereas the local touchpad cannot. Therefore, the software must be sending the touchpad gestures which are based on keyboard shortcuts. Strange though that the local gestures get prevented...
