# Chrome Middle-Click Scroll

Run your Chrome/ium browser from the command line:

```
chromium-browser --enable-blink-features=MiddleClickAutoscroll
```

## Making it stick

There are two ways to do this. One works on Arch, and is way better, and the other way is clunky and awkward but it works on all the other GNU/Linuxes.

1. You duplicate the .desktop launcher file and add the flag in there, or
2. You create a dedicated flags file in \~/.config.

The second way is better so we'll start with that, but it probably only works on Arch-based systems (I can't work out why) so [skip to Method 1 if you're not on Arch](chrome-middle-click-scroll.md#method-1).

### Method 2

In `~/.config/` create a file called `chromium-flags.conf`.

(Alternatively, name it with the executable name of your chromium-based browser. Idk but this might also work with other apps and browsers. Try it and see! YMMV and I'm not responsible ok)

In the chromium-flags.conf file, paste the same flag line, complete with double-hyphen:

```
--enable-blink-features=MiddleClickAutoscroll
```

It should look like this:

<figure><img src="../../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>



### Method 1

* Go to `/usr/share/applications`&#x20;
* Find the launcher file for your chosen browser, e.g. `chromium.desktop`&#x20;
* Copy it to \~/.local/share/applications
* Edit the new file
* Edit the "name" parameters slightly so that you can tell if the right `.desktop` file is being used in your desktop shell's application launcher
* Find the `exec=` line and add your chosen flag/s to it

It should look like this:

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (28).png" alt=""><figcaption></figcaption></figure></div>

<div data-with-frame="true"><figure><img src="../../.gitbook/assets/image (29).png" alt=""><figcaption></figcaption></figure></div>



{% hint style="warning" %}
## Heads up:

Your browser is going to give you an annoying warning every time you start it up.

Ignore it if you want middle-click-to-scroll.

I have NO idea why this isn't enabled by default. It's been in Firefox since I was 8 years old? That's 25 years.
{% endhint %}



### Sources

* Reddit/r/linux\_gaming — [Enable Middle Mouse Button Scrolling on Chrome(-ium) and Electron apps (Discord, etc)](https://www.reddit.com/r/linux_gaming/comments/w27h1o/linux_enable_middle_mouse_button_scrolling_on/)&#x20;
* Arch Linux Wiki — [Chromium — Making flags persistent](https://wiki.archlinux.org/title/Chromium#Making_flags_persistent)&#x20;
