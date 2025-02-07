# Firewalls

Most computer OS[^1]es come with firewalls pre-installed and activated.

But if you dig into the firewall app and its configuration, you'd probably be dismayed.

The default settings are usually extremely permissive, and rarely will you see a pop-up alerting you that an app is trying to send data outward, nor that an inbound connection is being made.

This excessive permissivity is based on pre-set configurations, built on the assumption that everything in the system is safe and thus should be implicitly trusted. But such implicit trust provides an easy foundation for disguised attacks, and indeed, many common attacks work by a script injecting malicious code into a part of the OS[^2] that is implicitly trusted, thus enabling the malicious code to "phone home" and send your private data — like passwords, [session tokens](#user-content-fn-3)[^3], keystrokes — to a remote server, where they collect masses of private data from hacks. They then sell your data to the highest bidder, who might do _anything_ with your data.

By default, firewalls _**should**_ be configured in "whitelist" mode; that is, _**everything is blocked**_ until it requests network access and you grant — or deny — it access to the internet.&#x20;

Here we'll cover some better firewall tools that can grant you real peace of mind.

* SimpleWall — [github](https://github.com/henrypp/simplewall)&#x20;
* Binisoft MalwareBytes firewall — [homepage](https://www.binisoft.org/wfc)&#x20;
  * It appears that MalwareBytes acquired Binisoft in 2018.
  * This software is still in active development. The changelog is posted on MalwareBytes's own forum, [check it here](https://forums.malwarebytes.com/topic/296798-malwarebytes-windows-firewall-control-wfc/) for updates.
* NextDNS — [homepage](https://nextdns.io/)&#x20;
  * A DNS service that also provides some firewalling capabilities.
  * I haven't explored this yet so I'll update these pages when I know more.
  * The firewalling appears to operate via _DNS filtering_, and this is disabled (on the free account?) after 300,000 queries in one month, so **do not rely on this as your primary/sole method of firewall protection**.

For the information in this _Internet Safety_ section, I'm finding a lot of great guidance from another website, [_**Privacy Guides .Org**_](https://www.privacyguides.org).

{% embed url="https://www.privacyguides.org/en/dns" %}



[^1]: Operating Systems

[^2]: Operating System

[^3]: The information that your browser uses to stay logged in to your accounts on all the websites that you use. If these are stolen, someone else can _connect_ to your currently logged-in sessions without anyone knowing — not you, nor the company who own the website. Additionally, some websites make it extremely hard to reset these session tokens, so it's hard or even impossible to kick the hackers out of your account. During this time, the hackers can change your email address and password and 2FA account.
