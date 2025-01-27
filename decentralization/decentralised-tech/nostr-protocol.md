# Nostr Protocol

So, Nostr is quite a beast.

A beast of a concept, anyway.

It's not a network or an app.&#x20;

It's a protocol for sharing content, in an apparently uncensorable way.

{% hint style="info" %}
## [→🌐🔗What is Nostr?](https://nostr.how/en/what-is-nostr)&#x20;

Taken from a guide website on how to get started with Nostr:

> _"Nostr stands for “Notes and Other Stuff Transmitted by Relays”. Like HTTP or TCP-IP, Nostr is a protocol; an open standard upon which anyone can build. Nostr itself is not an app or service that you sign up for."_



I recommend that you explore their website because it has a lot of information on how to set up Nostr. It's not _very_ hard, but it's certainly more involved than we are used to with normal, centralised social networks.
{% endhint %}

## Useful links

<table data-view="cards"><thead><tr><th></th><th data-card-target data-type="content-ref"></th><th></th></tr></thead><tbody><tr><td><strong>What is Nostr?</strong></td><td><a href="https://nostr.how/en/what-is-nostr">https://nostr.how/en/what-is-nostr</a></td><td></td></tr><tr><td><strong>Nostr Apps .com</strong></td><td><a href="https://nostrapps.com/">https://nostrapps.com/</a></td><td><em>Currently down.</em></td></tr><tr><td><strong>Nostr App Manager</strong></td><td><a href="https://nostrapp.link/">https://nostrapp.link/</a></td><td></td></tr></tbody></table>



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

## Nostr tools

<table data-view="cards"><thead><tr><th></th><th data-type="content-ref"></th><th></th></tr></thead><tbody><tr><td><strong>N Sec .app</strong></td><td><a href="https://nsec.app/">https://nsec.app/</a></td><td>Security app for storing your sign-in keys and signing you in to Nostr apps.</td></tr><tr><td><strong>Alby</strong></td><td><a href="https://getalby.com/">https://getalby.com/</a></td><td><em>But I don't fully understand what this is yet, and it seems to do too many things automatically.</em></td></tr><tr><td><strong>Amber</strong></td><td><a href="https://github.com/greenart7c3/Amber/releases">https://github.com/greenart7c3/Amber/releases</a></td><td><em>Security key app for Android (&#x26; iOS?). I haven't worked out how to use it yet.</em></td></tr><tr><td><strong>Nosta.me</strong></td><td></td><td>Seems to present your Nostr ID's data, but this site isn't for posting on. It also provides URLs to your Nostr profiles on other platforms, which is useful.</td></tr><tr><td><strong>nJump.me</strong></td><td></td><td><em>"a HTTP Nostr gateway to browse profiles, notes and relays; to preview a resource and then open it with your preferred client. The typical use of njump is to share a resource outside the Nostr world, where the nostr: schema is not (yet) working."</em> </td></tr></tbody></table>



## Nostr apps

<table data-view="cards"><thead><tr><th>App name</th><th>Type</th><th>Nostr App Manager</th><th>Home page</th><th>Web app</th><th>Android app</th><th>iOS app</th><th>Windows app</th><th>MacOS app</th><th>GitHib site</th><th data-hidden>NostrApps.com</th></tr></thead><tbody><tr><td><strong>Amethyst</strong></td><td>Microblogging</td><td><a href="https://nostrapp.link/a/naddr1qqxnzd3cx5urqv3nxymngdphqgsyvrp9u6p0mfur9dfdru3d853tx9mdjuhkphxuxgfwmryja7zsvhqrqsqqql8kavfpw3">Nostr App Manager</a></td><td><a href="https://amethyst.social/">amethyst.social</a></td><td></td><td><a href="https://play.google.com/store/apps/details?id=com.vitorpamplona.amethyst">Google Play</a> — <a href="https://f-droid.org/packages/com.vitorpamplona.amethyst/">F-droid</a> — <a href="https://github.com/ImranR98/Obtainium">Obtanium</a> — <a href="https://zap.store/">Zap.store</a> </td><td></td><td></td><td></td><td><a href="https://github.com/vitorpamplona/amethyst/releases">GitHub site</a> </td><td><a href="https://nostrapps.com/amethyst">NostrApps.com</a></td></tr><tr><td><strong>OpenVibe</strong> </td><td>Microblogging, cross-platform</td><td>Nostr App Manager</td><td><a href="https://openvibe.social/">openvibe.social</a></td><td></td><td><a href="https://play.google.com/store/apps/details?id=com.plebstr.client">Google Play</a> </td><td><a href="https://apps.apple.com/cz/app/openvibe-to-nostr-beyond/id1666230916">App Store</a> </td><td></td><td></td><td></td><td><a href="https://nostrapps.com/openvibe">NostrApps.com</a></td></tr><tr><td><strong>Coracle</strong></td><td>Microblogging</td><td>Nostr App Manager</td><td></td><td></td><td></td><td></td><td></td><td></td><td></td><td><a href="https://nostrapps.com/coracle">NostrApps.com</a></td></tr><tr><td><strong>Primal</strong></td><td>Microblogging</td><td><a href="https://nostrapp.link/a/naddr1qqxnzd3exycrwwphxgunjve4qgsrx4k7vxeev3unrn5ty9qt9w4cxlsgzrqw752mh6fduqjgqs9chhgrqsqqql8kw4vkcq">Nostr App Manager</a></td><td><a href="https://primal.net/">primal.net</a></td><td><a href="https://primal.net/">primal.net</a></td><td></td><td></td><td></td><td></td><td></td><td><a href="https://nostrapps.com/primal">NostrApps.com</a></td></tr><tr><td><strong>Iris</strong></td><td>Microblogging</td><td><a href="https://nostrapp.link/a/naddr1qqxnzd3cx5mnyvec8qungvenqgsrx4k7vxeev3unrn5ty9qt9w4cxlsgzrqw752mh6fduqjgqs9chhgrqsqqql8ks78ejl">Nostr App Manager</a></td><td><a href="https://iris.to/">iris.to</a></td><td><a href="https://iris.to/">iris.to</a></td><td></td><td></td><td></td><td></td><td><a href="https://github.com/irislib">GitHub site</a> </td><td><a href="https://nostrapps.com/iris">NostrApps.com</a></td></tr><tr><td><strong>NostrMo</strong></td><td>Microblogging</td><td>Nostr App Manager</td><td></td><td><a href="https://web.nostrmo.com/">web.nostrmo.com</a></td><td><a href="https://play.google.com/store/apps/details?id=com.github.haorendashu.nostrmo">Google Play</a> </td><td></td><td></td><td></td><td></td><td><a href="https://nostrapps.com/nostrmo">NostrApps.com</a></td></tr><tr><td><strong>Olas.app</strong></td><td>Photo sharing</td><td><a href="https://nostrapp.link/a/naddr1qqxnzdenxyur2vpkxyur2vp4qgs04xzt6ldm9qhs0ctw0t58kf4z57umjzmjg6jywu0seadwtqqc75srqsqqql8k7ygv3x">Nostr App Manager</a></td><td><a href="https://olas.app/">olas.app</a></td><td><a href="https://olas.app/">olas.app</a></td><td></td><td></td><td></td><td></td><td></td><td>NostrApps.com</td></tr><tr><td><strong>Flotilla</strong></td><td>Group chat</td><td><a href="https://nostrapp.link/a/naddr1qqxnzdenxucr2wp48ymnqdfsqgsf03c2gsmx5ef4c9zmxvlew04gdh7u94afnknp33qvv3c94kvwxgsrqsqqql8k0gu2vz">Nostr App Manager</a></td><td><a href="https://flotilla.social/">flotilla.social</a></td><td><a href="https://app.flotilla.social/">app.flotilla.social</a></td><td></td><td></td><td></td><td></td><td></td><td></td></tr><tr><td><strong>Snort</strong></td><td>Microblogging</td><td>Nostr App Manager</td><td><a href="https://snort.social/">snort.social</a></td><td><a href="https://snort.social/">snort.social</a></td><td></td><td></td><td></td><td></td><td></td><td></td></tr><tr><td><strong>Nostter</strong></td><td>Microblogging</td><td>Nostr App Manager</td><td><a href="https://nostter.app/">nostter.app</a></td><td><a href="https://nostter.app/">nostter.app</a></td><td></td><td></td><td></td><td></td><td></td><td></td></tr><tr><td><strong>NoStrudel</strong></td><td>All post types?</td><td></td><td><a href="https://nostrudel.ninja/">nostrudel.ninja</a></td><td><a href="https://nostrudel.ninja/">nostrudel.ninja</a></td><td></td><td></td><td></td><td></td><td></td><td></td></tr></tbody></table>



