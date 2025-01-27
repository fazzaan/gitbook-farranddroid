# Nostr Protocol

So Nostr is quite a beast.

A beast of a concept, anyway.

It's not a network or an app.&#x20;

It's a protocol for sharing content, in an apparently uncensorable way.

{% hint style="info" %}
[**→🌐🔗 What is Nostr?**](https://nostr.how/en/what-is-nostr)&#x20;

Taken from a guide website on how to get started with Nostr:

> _"Nostr stands for “Notes and Other Stuff Transmitted by Relays”. Like HTTP or TCP-IP, Nostr is a protocol; an open standard upon which anyone can build. Nostr itself is not an app or service that you sign up for."_



I recommend that you explore their website because it has a lot of information on how to set up Nostr. It's not _very_ hard, but it's certainly more involved than we are used to with normal, centralised social networks.
{% endhint %}

_Here's some notes I've written today, going through my own Nostr initiation:_

## Getting started on Nostr as new type of network

1. Nostr is a protocol of network connectivity. It is not a specific app.
2. You have a Nostr ID. This is how you log in to every app. _Keep it secret. **Non-negotiable.**_
3. You should set up a nostr security service. This will keep your Nostr ID (nsec) key and will allow you to manage new apps that try to connect using your Nostr ID. I am using one called Nsec.app. See _Nostr security_ section for setup instructions.
4. Connect to Nostr network apps by pasting your Nostr ID into the login box. Some apps will request you to log in by scanning a QR code or pasting a "bunker" URL instead (provided by security key manager apps like Nsec.app).
5. You can post on the Nostr network with a variety of post types.

### Nostr Platform Types

* microblogging — like Twitter, sometimes like Facebook
* images — like Instagram, very similar actually&#x20;
  * Olas.app — it is currently quite broken.
  * There don't seem to be many purely image-based apps yet — Olas seems to be the only one.
* group chats — looks a bit like IRC, Discord maybe, but probably less featureful. I haven't explored these apps at all yet.
  * Flotilla&#x20;

### Nostr app list sites

* [Nostr Apps https://nostrapps.com/](https://nostrapps.com/)&#x20;
* [Nostr App Manager https://nostrapp.link/](https://nostrapp.link/)&#x20;

### Nostr tools

* security apps&#x20;
  * [nsec.app](https://nsec.app) — web-app (including mobile); stores keys on your device; nostr activity permission manager for apps; can be self-hosted (but not necessary for security)&#x20;
  * [alby](https://getalby.com/) — I don't understand this one yet, but it seems to be originally a crypto wallet
  * [amber (github)](https://github.com/greenart7c3/Amber/releases) — should be the same as nsec.app but I didn't get it working yet
* gateways — profile viewers, etc
  * [nosta.me](https://nosta.me/) — seems to present your nostr ID data, but this site isn't for posting on. It also provides URLs to your nostr profiles on other platforms, which is useful
  * [njump.me](https://njump.me/npub12vkcxr0luzwp8e673v29eqjhrr7p9vqq8asav85swaepclllj09sylpugg) — _"a HTTP Nostr gateway that allows you to browse profiles, notes and relays; it is an easy way to preview a resource and then open it with your preferred client. The typical use of njump is to share a resource outside the Nostr world, where the nostr: schema is not (yet) working."_&#x20;

### Nostr twitteresque apps

* primal
  * _**note:** I have a weird problem in the web version, it somehow signed in to a random (new) account and I can't find any way to sign out._&#x20;
  * [nostrapps link](https://nostrapps.com/primal)&#x20;
  * [web](https://primal.net/)&#x20;
  * [primal.net download page](https://primal.net/downloads)&#x20;
  * [android](https://play.google.com/store/apps/details?id=net.primal.android\&hl=en)&#x20;
  * [ios](https://apps.apple.com/us/app/primal/id1673134518) — [viet store](https://apps.apple.com/us/app/primal/id1673134518?l=vi)&#x20;
  * [github](https://github.com/PrimalHQ)&#x20;
* coracle
  * nostrapps link https://nostrapps.com/coracle
  * web https://coracle.social/
* nostrmo
  * nostrapps link https://nostrapps.com/nostrmo
* Amethyst
  * nostrapps link https://nostrapps.com/amethyst
  *
* Iris
  * nostrapps link https://nostrapps.com/iris
* OpenVibe
  * Connects to Nostr, Mastodon, BlueSky and Threads (those 2 are questionable though, but could be a good way to bring people into Nostr)
  * Web
  * Android
  * iOS
* Gossip
  * sorry this app is shit

### Messaging apps

* Flotilla -- group chats
  * web https://app.flotilla.social/

### Photo-sharing apps

* Olas.app -- very much like Instagram
  * web -- login doesn't seem to work at all
  * ios app
  * android app

