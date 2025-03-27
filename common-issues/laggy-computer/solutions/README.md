# Solutions

One reason could be the over-usage of the CPU, causing the clock speed to be limited.

There are a couple of solutions to this.



{% stepper %}
{% step %}
### Limit the number of CPU cores

_<mark style="color:green;">No risk.</mark>_

Limit the number of CPU cores that the offending process/es have access to.&#x20;

This can be achieved from inside Windows Task Manager.
{% endstep %}

{% step %}
### Limit the CPU utilization percentage

_<mark style="color:yellow;">Low risk.</mark>_

Limit the CPU utilization percentage that the offending process/es have access to.&#x20;

This can be achieved using a third-party application called BES (Battle Encoder Shirasé).
{% endstep %}

{% step %}
### Raise the CPU rate-limiting thresholds

_<mark style="color:red;">High risk, but fine if you're careful.</mark>_

This is risky because it is possible that your CPU is overheating. However, many mobile CPUs have their temperature threshold set much lower than necessary. So, check the real temperature of your CPU and decide if it's ok to raise the limiter thresholds.

Physically, most CPUs can reach 90-95°C before having any problems. My laptop's CPU started rate-limiting at around 75°C, which is unnecessary and frustrating.
{% endstep %}
{% endstepper %}

{% hint style="success" %}
### **Solution 1 —** Limit the number of CPU cores

**Solution 1 is the safest option** for you to use because it is a feature built into Windows, and it doesn't alter any hardware configurations.

  → Solution 1: [set-processor-affinity.md](set-processor-affinity.md "mention") (no risk)
{% endhint %}

> Solution 2 uses third-party software, but it doesn't risk any physical damage to the hardware. Visit my [Power User](https://app.gitbook.com/o/HGV4O8QFvR73oXn7Uxww/s/qA7gVdU3GXPI3OOuI1Ep/ "mention") website to use this method.
>
> Solution 3 also uses third-party software, _**and**_ risks damaging the CPU (and motherboard!) if you configure it incorrectly. It can also cause OS instability. Visit my [Power User](https://app.gitbook.com/o/HGV4O8QFvR73oXn7Uxww/s/qA7gVdU3GXPI3OOuI1Ep/ "mention") website to use this method.&#x20;

{% hint style="danger" %}
## <mark style="color:red;">YOU HAVE BEEN WARNED!!!</mark>

&#x20;[Power User](https://app.gitbook.com/o/HGV4O8QFvR73oXn7Uxww/s/qA7gVdU3GXPI3OOuI1Ep/ "mention") (main site)

  → Solution 2: Limit CPU percentage (low-risk)&#x20;

  → Solution 3: Raise CPU thresholds (high-risk)&#x20;
{% endhint %}



***

