# Torrenting

“_Where there's a will, there's a way.”_&#x20;

Or, I <mark style="color:yellow;">can't stop you</mark> doing things, so it's <mark style="color:yellow;">better to teach you the safest ways to do it</mark> and how to be careful, than to try to prevent you from doing it altogether.

**Education over prohibition.**

_<mark style="color:purple;">If only our governments thought this way too.</mark>_

## Contents

1. [#what-is-torrenting](torrenting.md#what-is-torrenting "mention")
2. [#risks](torrenting.md#risks "mention")
3. [#best-practices-when-searching-for-torrents](torrenting.md#best-practices-when-searching-for-torrents "mention")
4. [#desktop-apps](torrenting.md#desktop-apps "mention")
5. [#mobile-apps](torrenting.md#mobile-apps "mention")

## What is torrenting?

Torrents are a fairly old technology nowadays.

Basically, the files are stored on someone else's computer, and their software broadcasts the files' availability. The broadcasting happens via some dark magic, and then websites and other apps can detect these broadcasts. With the right instructions (more dark wizardry), the app on your computer can receive the files directly from their computer.&#x20;

This is known as _P2P_, peer-to-peer file sharing.

Another layer of this dark magic is the trackers, which collate file listings from many many people. Each person may have all, or part, of the required files, and the application co-ordinates the transfers such that your computer can receive parts of the files from whichever computer is ready to upload it to yours at that moment.

You see? Dark magical wizardry.

People who don't believe in magic are delulu.

## Risks

There are serious and very real risks associated with torrenting.

Torrenting is often used for sharing software and media that is illegal, be it pirated, cracked, or illegal content itself. You are responsible for checking the law in your country and making the right choices; and if you decide to use it for illegal purposes, you should protect yourself and prepare to suffer the consequences.

{% hint style="info" %}
If you decide to use torrenting for immoral, debased purposes, you are going to whichever hell claims your disgusting soul.
{% endhint %}

Here I could shill for a VPN service, but I'm not going to. Well, even VPN services come with their own slew of risks!

#### <mark style="color:yellow;">The risks</mark>

* Your network traffic may be being watched by your ISP[^1], the police, your government, etc.
* <mark style="color:red;">Files may contain malicious code that steals information about your computer, your identity, your security, your cameras, and more.</mark> _<mark style="color:yellow;">This is more dangerous than the police watching you — you can lose your email accounts, social media accounts, bank accounts, your money, your identity.</mark>_&#x20;

#### Due Diligence

* Don't make rash decisions&#x20;
* For **apps**:&#x20;
  * Check what the app installers should look like — _any_ deviation means that it is probably fake&#x20;
  * Block installers from the internet if possible&#x20;
  * Block installed apps from the internet&#x20;
  * Use a VM[^2] to test out the installation of apps before deciding to install them on your actual OS&#x20;
  * Cancel installation at first feeling of doubt&#x20;
  * Have Task Manager open, ready to kill the installation app if it seems to be rogue&#x20;
* For **video**:&#x20;
  * Open the media app _first_, then drag the video file into the app.&#x20;
  * Don't open the video file by double-clicking it in the file browser, because it might be an [executable file](#user-content-fn-3)[^3] disguised as a video.&#x20;



## Best practices when searching for torrents

* <mark style="color:yellow;">DON'T TRUST ANYTHING</mark>&#x20;
* how to choose a torrent index / search website&#x20;
* look at link URLs before clicking on them&#x20;
* order by seeder quantity&#x20;
* check details!!!:
  * check for torrent creator username and their reputation&#x20;
  * check torrent date&#x20;
  * check other torrent metadata&#x20;
  * check torrent title&#x20;
  * look for comments on the torrent's page&#x20;
  * compare the file list on the page with the file list shown in your torrent client app&#x20;
* use the magnet 🧲 link instead of downloading the `.torrent` file&#x20;
* install an adblocker to try to prevent getting caught by annoying & malicious ads, invisible clickjackers (fullscreen invisible buttons), etc.&#x20;
  * use → uBlock ORIGIN   <mark style="color:red;">(not uBlock.org)</mark>&#x20;
    * [→ 🔗 Chrome extension](https://chromewebstore.google.com/detail/cjpalhdlnbpafiamejdnhcphjbkeiagm)&#x20;
    * [→ 🔗 Firefox extension](https://addons.mozilla.org/en-US/firefox/addon/ublock-origin/)&#x20;
    * [→ 🔗 Edge extension](https://microsoftedge.microsoft.com/addons/detail/odfafepnkmbhccpbejgmiehpchacaeak) (current reviews indicate it isn't working)
    * [→ 🔗GitHub link](https://github.com/gorhill/uBlock)&#x20;
    * Why not uBlock.org? (explain later)
    * Why is Chrome Store warning me about it? (look on their GitHub page for the info)

### How to choose a website

* <mark style="color:yellow;">DON'T TRUST ANYTHING OR ANYONE.</mark>&#x20;
* Try <mark style="color:orange;">**Reddit**</mark> first. There's a lot of chat on there, regularly updated.
* Many websites get **cloned**, their URL[^4]s get mimicked with similar names and TLD[^5]s.&#x20;
* Many websites get **hacked**, so they look identical, have the same URL, and even function the same as before, but their torrents have been replaced with malicious torrents — the files may even look like the original files, but the installers will install malicious software instead. This is scary but you can avoid it by paying close attention. [<mark style="color:blue;">\[ ? \]</mark>](#user-content-fn-6)[^6]&#x20;
* _<mark style="color:red;">**Search**</mark>_ <mark style="color:red;"></mark><mark style="color:red;">for the website address</mark> BEFORE _going_ to the website itself. Google ([etc](../web-browser-setup/alternatives-to-google-and-bing.md)) should show you posts from others who are warning if a site is malicious or has been compromised.&#x20;



## Desktop apps

### DON'T USE UTORRENT

utorrent is just an advertising platform these days.

And fuq knows what data it is tracking and gathering about you and your devices.

### qBittorrent

[→ 🔗 qBittorrent homepage](https://www.qbittorrent.org/)&#x20;

Open source, free, quite customisable. qBittorrent does probably everything you could want from it.

It runs on the main computer OSes: Linux, macOS and Windows; and even OS/2, FreeBSD and Haiku[^7].

It supports dark mode.

Its UI is built in QT, hence the name _&#x71;_&#x42;ittorrent.

### Transmission

[→ 🔗 Transmission homepage](https://transmissionbt.com/)&#x20;

Transmission is a very lightweight app and runs on all the major OS platforms.&#x20;

It also has a web UI, and can run a background daemon service.

On Linux, it has a dark mode that matches the GTK settings (and maybe QT settings under KDE). On Windows it doesn't seem to have a dark mode.

### Deluge

[→ 🔗 Deluge homepage](https://deluge-torrent.org/)&#x20;



## Mobile apps

I haven't found many torrenting apps for mobile devices, but I do recall one called Flud on Android.

### Flud (Android)

[→ 🔗 Flud on Google Play Store](https://play.google.com/store/apps/details?id=com.delphicoder.flud) or [→ 🔗 Flud+ (paid, no ads) on Google Play Store](https://play.google.com/store/apps/details?id=com.delphicoder.flud.paid)&#x20;

I don't remember using this app much but who torrents on a mobile device?





[^1]: internet service provider

[^2]: Virtual machine

[^3]: Any file that can run code and therefore affect your computer system (OS) in some way.

[^4]: website address — Universal Resource Locator&#x20;

[^5]: the bit on the end of the main website URL, after the last dot. TLD = Top Level Domain. Examples: .com, .co.uk, .net, .org, .to, etc.

[^6]: (This happened to me only once in >15 years.)

[^7]: wtf is Haiku
