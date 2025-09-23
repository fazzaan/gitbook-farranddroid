# Chrome Middle-Click Scroll

Run your Chrome/ium browser from the command line:

```
chromium-browser --enable-blink-features=MiddleClickAutoscroll
```

You can add it to your .desktop launcher file, but I recommend against that because there's a new and better way to add startup flags:

In `~/.config/` create a file called `chromium-flags.conf`.

(Alternatively, name it with the executable name of your chromium-based browser. Idk but this might also work with other apps and browsers. Try it and see! YMMV and I'm not responsible ok)

In the chromium-flags.conf file, paste the same flag line, complete with double-hypen:

```
--enable-blink-features=MiddleClickAutoscroll
```

It should look like this:

<figure><img src="../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

{% hint style="warning" %}
## Heads up:

Your browser is going to give you an annoying warning every time you start it up.

Ignore it if you want middle-click-to-scroll.

I have NO idea why this isn't enabled by default. It's been in Firefox since I was 8 years old? That's 25 years.
{% endhint %}



### Sources

* Reddit/r/linux\_gaming — [Enable Middle Mouse Button Scrolling on Chrome(-ium) and Electron apps (Discord, etc)](https://www.reddit.com/r/linux_gaming/comments/w27h1o/linux_enable_middle_mouse_button_scrolling_on/)&#x20;
* Arch Linux Wiki — [Chromium — Making flags persistent](https://wiki.archlinux.org/title/Chromium#Making_flags_persistent)&#x20;
