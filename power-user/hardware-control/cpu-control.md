# CPU Control

{% hint style="danger" %}
## HERE BE DRAGONS
{% endhint %}

## 1 — Limit the CPU utilization percentage <a href="#limit-the-cpu-utilization-percentage" id="limit-the-cpu-utilization-percentage"></a>

_This is categorized as Low risk because it does not alter hardware parameters, but it does entail using third party software._

Limit the CPU utilization percentage that the offending process/es have access to.

This can be achieved using a third-party application called BES (Battle Encoder Shirasé).

I'm getting tired of writing all these guides, I need to dedicate more time to biology research.

Go download and test BES for yourself! :)))

<table data-card-size="large" data-view="cards"><thead><tr><th></th><th data-card-target data-type="content-ref"></th></tr></thead><tbody><tr><td>BES homepage</td><td><a href="https://mion.yosei.fi/BES/">https://mion.yosei.fi/BES/</a></td></tr><tr><td>Windows Report site that told me about BES</td><td><a href="https://windowsreport.com/limit-cpu-usage/#h-2-use-bes">https://windowsreport.com/limit-cpu-usage/#h-2-use-bes</a></td></tr><tr><td>Download BES from my drive (I keep backups of useful indie apps just in case)</td><td><a href="https://drive.proton.me/urls/CSP5X4292W#ULiBrglSA21a">https://drive.proton.me/urls/CSP5X4292W#ULiBrglSA21a</a></td></tr></tbody></table>



## 2 — Raise the CPU rate-limiting thresholds

_High risk, but fine if you're careful._

This is risky because it is possible that your CPU is overheating. However, many mobile CPUs have their temperature threshold set much lower than necessary. So, check the real temperature of your CPU and decide if it's ok to raise the limiter thresholds.

Physically, most CPUs can reach 90-95°C before having any problems. My laptop's CPU started rate-limiting at around 75°C, which is unnecessary and frustrating.

Ok for now I'll just put the link here, you can probably work most of it out :)))

[https://gitlab.com/ryzen-controller-team/ryzen-controller/-/releases](https://gitlab.com/ryzen-controller-team/ryzen-controller/-/releases)&#x20;

{% embed url="https://gitlab.com/ryzen-controller-team/ryzen-controller/-/releases" %}

And a link to the file in my Proton Drive, just in case the repository goes offline (because this project is now defunct and archived):

[https://drive.proton.me/urls/A4MEG5H3RW#0ZFEmpkCtJm9](https://drive.proton.me/urls/A4MEG5H3RW#0ZFEmpkCtJm9)&#x20;

{% embed url="https://drive.proton.me/urls/A4MEG5H3RW#0ZFEmpkCtJm9" %}
