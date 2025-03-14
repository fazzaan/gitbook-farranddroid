# What do I need for getting started?

## Things to accept:

1. accept that you will need to pay for some things.
2. accept that most services will be less convenient and more awkward.
3. accept that you can never be sure that you have full security and privacy and anonymity and encryption: you should _always_ assume that you might be being watched.
4. accept that you might need to buy new devices that are better supported by what you need.
5. accept that you might have to sacrifice power & convenience by using virtual machines etc.
6. accept that you will probably need to change vendors at least twice in your privacy & security.

## Principles:

1. "**As Much As Reasonably Possible**". Follow the concept of "harm reduction" — don't go for the "all or nothing" approach — if there are some things that you must use, use them. It's better that some/most of your activities are through secure channels than none. If you need Google Drive & Docs & Sheets (etc) and can't find a good alternative then use them.
2. "**Zero Trust**". Many companies offer encrypted storage (etc.), but your data is encrypted using _their_ platform. Your data might be safe from hackers, but the company themselves hold the encryption key and they _will_ relinquish control of the key and your data if ordered to do so. **Zero Trust** is when you encrypt your data for yourself _**before**_ uploading it to someone else's server, that way the server company cannot decrypt your data even if a govt or military demand it. (Do be aware that LLMs \[AI] has already worked out how to decrypt 56-bit encryption, although I just went to research this and either the search engines are suppressing it or the news was fake or I was dreaming...)

## Things to get:

### Internet space

* email — encrypted, burnable handles, etc — NOTHING from Google etc
* calendar solution (i really don't know)
* notes service
* decentralised media — Nostr, etc (BlueSky is not decentralised afaik[^1])
* federated social media — Mastodon, etc (Meta's Threads _does not count_)
* encrypted communication methods — no "end to end" shite from mega corporations, that's all blatantly false. Telegram also doesn't count.
* anonymous communication methods — MUST be paired with VPNs, Tor, etc

### Computer use

* web browser — Firefox etc, NO CHROMIUM-BASED ANYTHING
* Tor browser if anonymity is required&#x20;
* firewalls — block connections by default&#x20;
* VPN&#x20;
* DNS and/or WARP&#x20;
* good antivirus&#x20;
* file storage — local backup, cloud backup if you want — NOT GOOGLE etc
* safe operating system —&#x20;
  * no Apple (especially not since their latest M CPUs with crazy undetectable memory access security issues)
  * no Windows unless you manage to find sane & up-to-date guides on how to disable all the spyware and telemetry — this seems to be possible, especially if you're running a stripped-down version of Windows or have tight firewall configurations
  * no Linux that has been tainted by corporate fingers (Ubuntu/Canonical are suspicious)&#x20;
  * Linux distros like _Tails_ are probably best for anonymity, but aren't ideal as daily drivers. Most _Tails_ users just boot it up as and when required. (Actually this is best practice anyway.)&#x20;
* F/OSS apps for your personal & work life, such as office, desktop publishing, graphic editing, etc. All the proprietary apps are closed-source, so you _cannot_ know what information they are collecting about you and your devices, nor who they're giving/selling it to.

### Phone use

* no iphone. I'm dead serious.
* No stock Android. Research first, choose a phone that has a stable and well-supported AOSP ROM, then install your chosen ROM to replace the stock ROM on your phone. (Follow the instructions and read the recent forum posts, else you may brick your phone.)&#x20;
* Keep your phone in aeroplane mode as much as possible — although idk if this actually disables the mobile radio devices or not

## if you're a programmer, you'll also need:

* code IDE — VSCodium is the exact codebase of VS Code, just without Microsoft's spyware
* github alternatives — gitlab, bitbucket, etc
* programming languages that aren't distributed by google etc

[^1]: as far as i know
