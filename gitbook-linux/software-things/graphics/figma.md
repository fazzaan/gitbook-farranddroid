# Figma

{% hint style="info" %}
There's no _perfect_ Figma client yet.

* Figma web can't see the fonts on your computer
* Figma desktop needs chromium flag tweaks to make WebGL actually work
* Figma desktop should be able to see local fonts but it can't currently
* There's a few "figma connect" projects in the AUR which are supposed to provide the Figma website with access to local fonts, but none of them work
{% endhint %}

## Option 1

Use Figma in the web browser. It's basically fine.&#x20;

The Figma devs still haven't made a Linux app to access local fonts, which is why we need to use a font connector app (none of them work) or a local desktop app of Figma (whose font access also doesn't work).

Luckily Figma comes with a tonne of fonts already, including access to Google Fonts, so this is only an issue if you have a specific font that you want to use.

I'm sure this'll be rectified in the near future, as it used to work, and the F/OSS world is wiley and adaptable.



## Option 2

Install "Figma Linux", essentially an Electron wrapper app for the web version of Figma. It provides additional GPU acceleration, as well as local font access. Well, the local font access doesn't work currently (21st Dec 2025). And the GPU acceleration is broken by default, but you can make it work by passing some custom launch flags.

If it doesn't work for you, then follow these steps to make it work:

{% stepper %}
{% step %}
### Make a custom app launcher file

Go to `/usr/share/applications` .

Copy `figma-linux.desktop` to your `~/.local/share/applications` .
{% endstep %}

{% step %}
### Edit the launcher

Rename the file to `figma-custom.desktop` .

Edit the Name to say `Figma Custom` (or whatever you want).
{% endstep %}

{% step %}
### Add the launch flags

Comment out the existing `Exec=...` line by adding a hash <kbd>#</kbd> at the start of the line.

Write a new `Exec=` line and paste the following string of text in the same line:

<details>

<summary>paste this</summary>

{% code overflow="wrap" %}
```
/usr/bin/figma-linux --no-sandbox --enable-oop-rasterization --ignore-gpu-blacklist -enable-experimental-canvas-features --enable-accelerated-2d-canvas --force-gpu-rasterization --enable-fast-unload --enable-accelerated-vpx-decode=3 --enable-tcp-fastopen --javascript-harmony --enable-checker-imaging --v8-cache-options=code --v8-cache-strategies-for-cache-storage=aggressive --enable-zero-copy --ui-enable-zero-copy --enable-native-gpu-memory-buffers --enable-webgl-image-chromium --enable-accelerated-video --enable-gpu-rasterization --enable-vulkan --enable-unsafe-webgpu --enable-gpu-compositing --disable-features=UseChromeOSDirectVideoDecoder --enable-accelerated-video-decode --enable-accelerated-video-encode --enable-features=Vulkan --enable-hardware-overlays --ignore-gpu-blocklist --use-cmd-decoder=passthrough 
```
{% endcode %}

</details>

{% hint style="success" %}
If it works perfectly now, then well done, you've finished!
{% endhint %}

{% hint style="danger" %}
If not, then read on:
{% endhint %}
{% endstep %}

{% step %}
### Test the launch flags

It is possible that some of those launch flags will cause Figma to fail to launch, or to not successfully activate WebGL and GPU acceleration. If that's the case, you should open a terminal application, type `/usr/bin/figma-linux` , and add each flag one by one so that you can test which flags are responsible for making Figma not launch or for enabling or disabling WebGL and GPU acceleration.

There are a few more flags which were recommended to be used a few years ago, but when I used them, they caused Figma to fail. They are here, feel free to experiment with them too — if they work, you may get extra performance out of your system:

<details>

<summary>try these</summary>

All of these broke the app's functionality in some way, but they're supposed to make it run better. In the future they may help again.

```
--enable-features=VaapiVideoDecoder
```

```
--enable-features=VaapiVideoEncoder
```

```
--enable-features=VaapiIgnoreDriverChecks
```

```
--enable-features=RawDraw
```

{% code overflow="wrap" %}
```
--use-angle=vulkan --enable-features=UseOzonePlatform --ozone-platform=wayland
```
{% endcode %}

```
--use-cmd-decoder=passthrough
```

</details>

{% hint style="info" %}
_Note that some flags influence each other. Use your gumption: look at the meanings of the flags and wonder to yourself (or research!) if perhaps one flag broke the app because it should be used together with another flag._
{% endhint %}
{% endstep %}

{% step %}
### Check the GPU page in Figma

Each time Figma successfully launches, you need to check two things.

1. Open a file for editing. If it fails to load, it will show you a message explaining why.
2. Open the GPU internals page. It shows a report of rendering engine's condition. Find it by going to the top right menu button, down to Help, and click on GPU:

<figure><img src="../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

You will see a page like this. If your files aren't loading, several more of the Features will say <mark style="color:red;">Disabled</mark> in red. Use these to help you research what other launch flags to try, or to diagnose what perhaps may be wrong with your system — it could be a hardware issue, a driver issue, or a software issue.

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

Keep testing launch flags until you get as many green statuses as possible, and until you are able to open your Figma files for editing.
{% endstep %}

{% step %}
### Add the good flags to your launcher

Once you've identified the best list of launch flags — and tested them multiple times in the terminal — paste that list of flags into your `figma-custom.desktop` launcher file. Save it.

Run this in a terminal to force the system to update the app drawer with your newly edited launcher file:

```
xdg-desktop-menu forceupdate
```

Open your app drawer and search for `Figma Custom` . Launch it.

If you did everything right, it should launch exactly the same as when you ran it from the terminal.

{% hint style="success" %}
Congratulations! _(probably)_
{% endhint %}
{% endstep %}
{% endstepper %}

And that's just an hour in the life of living on Linux.

Yeah, it do be like this.

