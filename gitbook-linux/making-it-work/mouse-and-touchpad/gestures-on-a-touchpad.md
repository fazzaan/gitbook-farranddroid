# Gestures on a touchpad

_So far I've only explored GNOME._

{% tabs %}
{% tab title=""Window Gestures"" %}
👣 Install it from here — [extensions.gnome.org/extension/6343/window-gestures](https://extensions.gnome.org/extension/6343/window-gestures/)&#x20;

😸 Check the GitHub — [github.com/amarullz/windowgestures](https://github.com/amarullz/windowgestures)&#x20;
{% endtab %}
{% endtabs %}

Gnome and libinput can indeed detect and distinguish between 3, 4 and 5-finger swipe gestures, in all directions and shapes, but you'd never know it.

For some indiscernible reason, Gnome's gestures are hard-coded, and all 3-finger gestures are replicated to the 4-finger gestures too. Wild.

There are myriad alternative projects but honestly most of them are janky and nasty, and don't provide the one-to-one functionality where the gesture animations are locked into the movement of your fingers.

The only good solution I've found so far is a Gnome extension, which happened to work when I installed it on Gnome 48, but broke just 3 days later when Gnome 49 was released.&#x20;

The developer has released an update to for "gnome 49 support", but their github page says "support only for gnome 45" and the updated extension doesn't work on my computer anyway.&#x20;

(Perhaps I need to troubleshoot it more deeply, maybe there are some remnant config files from the previous version or something? idk but I've kinda got used to just not using gestures any more.)

Regardless, try the extension, in case it works for you, and in case the developer manages to fix things up in the future. It really was the best solution I managed to find, and I hope it works again!
