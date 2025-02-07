# Firewalls

Most computer OS[^1]es come with firewalls pre-installed and activated.

But if you dig into the firewall app and its configuration, you'd probably be dismayed.

The default settings are usually extremely permissive, and rarely will you see a pop-up alerting you that an app is trying to send data outward, nor that an inbound connection is being made.

This excessive permissivity is based on pre-set configurations, built on the assumption that everything in the system is safe and thus should be implicitly trusted. But such implicit trust provides an easy foundation for disguised attacks, and indeed, many common attacks work by a script injecting malicious code into a part of the OS[^2] that is implicitly trusted, thus enabling the malicious code to "phone home" and send your private data — like passwords, [session tokens](#user-content-fn-3)[^3], keystrokes — to a remote server, where they collect masses of private data from hacks. They then sell your data to the highest bidder, who might do _anything_ with your data.

By default, firewalls _**should**_ be configured in "whitelist" mode; that is, _**everything is blocked**_ until it requests network access and you grant — or deny — it access to the internet.

Here we'll cover some better firewall tools that can grant you real peace of mind.

* SimpleWall — [github](https://github.com/henrypp/simplewall)
* Binisoft MalwareBytes firewall — [homepage](https://www.binisoft.org/wfc)
  * It appears that MalwareBytes acquired Binisoft in 2018.
  * This software is still in active development. The changelog is posted on MalwareBytes's own forum, [check it here](https://forums.malwarebytes.com/topic/296798-malwarebytes-windows-firewall-control-wfc/) for updates.
* NextDNS — [homepage](https://nextdns.io/)
  * A DNS service that also provides some firewalling capabilities.
  * I haven't explored this yet so I'll update these pages when I know more.
  * The firewalling appears to operate via _DNS filtering_, and this is disabled (on the free account?) after 300,000 queries in one month, so **do not rely on this as your primary/sole method of firewall protection**.

For the information in this _Internet Safety_ section, I'm finding a lot of great guidance from another website, [_**Privacy Guides .Org**_](https://www.privacyguides.org).

{% embed url="https://www.privacyguides.org/en/dns" %}

***

## Quick Firewall Setup Guide

_Learn more about firewalls on_ 📄[firewalls.md](firewalls.md "mention").

_This is the same information as found on the_ [quick-setup-guide.md](quick-setup-guide.md "mention") _page._

{% stepper %}
{% step %}
#### Choose a firewall application.

I recommend SimpleWall Download and Binisoft MalwareBytes Windows Firewall Control.

* Download [🌐SimpleWall](https://github.com/henrypp/simplewall)
* Download [🌐Binisoft MalwareBytes Windows Firewall Control](https://www.binisoft.org/wfc)

(I actually use both at the same time.)
{% endstep %}

{% step %}
#### Install the firewall.
{% endstep %}

{% step %}
#### Activate the firewall.

**SimpleWall firewall**

SimpleWall is fairly simple.

It allows you to block all of Microsoft's spying and telemetry on your computer.

<figure><img src="../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

I have it set to block ALL connections by default. Then it will pop up a notification each time an app/process tries to create a new connection.

<figure><img src="../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

Don't forget to click _**Enable filters**_!!! This activates the SimpleWall firewall.

<figure><img src="../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
I had some trouble with SimpleWall at first, I guess because the pop-up notifications weren't appearing 🤷

I allowed a bunch of system processes through the firewall at random (educated guesses) until the internet connection was working again.

Hopefully you won't run into this issue. If you do, search the internet for tips — you can probably find some guidance on [🌐 SimpleWall's intro guide](https://github.com/henrypp/simplewall) too.
{% endhint %}

**MalwareBytes firewall**

MalwareBytes firewall is not set to block everything by default.

{% hint style="success" %}
Switch to the _Profiles_ tab and set it to **Medium Filtering (recommended)**.
{% endhint %}

{% hint style="warning" %}
Do not set it to High Filtering unless you want to completely sever your computer from the internet.
{% endhint %}

Also check the **Automatically set Medium Filtering after X minutes**.

<figure><img src="../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

Go to the _Notifications_ tab and set it to **Display Notifications**. This will ensure that you get a pop-up notification for every application (including system processes) that attempts to connect to the internet.

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

If you are concerned that some virus or malware might be connecting to the internet during boot-up, go to the _Security_ tab and enable **Secure Boot**.

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

Finally, return to the _Dashboard_ tab to check the firewall status — it should look like this:

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

And that should be enough!

I actually have both SimpleWall _and_ Binisoft MalwareBytes firewall running. I don't know if it's necessary, but it gives me some peace of mind knowing that every process has to get through _two_ firewalls in order to connect to the internet.
{% endstep %}
{% endstepper %}

***

[^1]: Operating Systems

[^2]: Operating System

[^3]: The information that your browser uses to stay logged in to your accounts on all the websites that you use. If these are stolen, someone else can _connect_ to your currently logged-in sessions without anyone knowing — not you, nor the company who own the website. Additionally, some websites make it extremely hard to reset these session tokens, so it's hard or even impossible to kick the hackers out of your account. During this time, the hackers can change your email address and password and 2FA account.
