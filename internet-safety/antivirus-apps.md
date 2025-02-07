# Antivirus apps

You must not rely solely on _one_ antivirus application; nor should you rely entirely upon antivirus software to protect you.

Several times, I have had to chase a virus around my computer, uncovering scripts, tasks in Task Scheduler, the Registry, fake driver entries, and powershell & cmd processes.

Even after all that, _and_ using Windows Security (which detected virus files and quarantined them!), Kaspersky still managed to find more malicious code hiding in the RAM.

* Kaspersky Antivirus — you can get a free 30-day trial with each new account. You can make unlimited new accounts by using email aliases. For Gmail, do this by simply adding a + after your email username, and whatever letters you like. E.g. hello+kspsk01@gamil.com, then after 30 days, hello+kspsk02@gamil.com, etc.
  * Kaspersky is the best AV I've found so far. It actually scans the whole system deeply, INCLUDING scanning the RAM for malicious code: many viruses are programmed to hide themselves in the RAM, making it impossible for you to delete them — they will always return after a reboot.
* Windows Security isn't too bad these days, it finds most malicious code. You should still use Kaspersky occasionally, and especially if you are suspicious.
* MalwareBytes seems to be good too. Check it out.

***

## Quick Antivirus Setup Guide

_Learn more about viruses and antivirus software on_ 📄[antivirus-apps.md](antivirus-apps.md "mention").

_This is the same information as found on the_ [quick-setup-guide.md](quick-setup-guide.md "mention") _page._

{% stepper %}
{% step %}
#### Choose an antivirus application.

I recommend Kaspersky and MalwareBytes.

I mainly recommend Kaspersky, but you need to keep creating a new account every 30 days, or you can just pay for it.

Windows Security does a decent job too, but it isn't perfect. Use it alongside another app.

* Download [🌐Kaspersky](https://www.kaspersky.com/downloads/standard-free-trial) [FREE TRIAL](antivirus-apps.md#user-content-fn-1)\[^1] — ([compare their plans](https://www.kaspersky.com/downloads#compare-table))
* Download [🌐MalwareBytes](https://www.malwarebytes.com/mwb-download)

Register for a Kaspersky account if you choose that. I do recommend it because it's the only antivirus app that managed to find the ransomware malware hiding in my RAM.
{% endstep %}

{% step %}
#### Install the antivirus software.

Kaspersky has a more-involved setup procedure because you have to sign in to your account.
{% endstep %}

{% step %}
#### Run the antivirus scans.

Most antivirus apps have a "quick scan" and a "full scan".

You should run both.

Start with the "quick scan" because that will scan the most likely locations that a virus is hanging out, and it will find it quickly if it is there.

Then run a "full scan". This will scan _everything_ but it will take _ages_.
{% endstep %}

{% step %}
#### Windows Security — double check it

If you are using Windows, go into your Windows Security application.

Double check your scan settings — one virus that I recently had had set Windows Security's antivirus scanning to exclude the entire system C: drive from its scans! The virus was able to go undetected because of this.

<figure><img src="../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

Your Exclusions list MUST look like this:

<figure><img src="../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>
{% endstep %}
{% endstepper %}

***
