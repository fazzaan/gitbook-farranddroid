# Input Methods - Fcitx5 (Asian languages)

On this page:

1. Input Method Panel extension for Gnome. (KDE has it already.)
2. Setting up and configuring Fcitx5, an input method _**plugin engine**_ which connects to any input method software that has an Fcitx5 plugin.
3. Screenshots of configuration, because it's horrible.
4. Other problems with input methods, and potentially mention fixes (but idk if there are any).



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

