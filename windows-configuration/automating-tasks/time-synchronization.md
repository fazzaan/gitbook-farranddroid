# Time Synchronization

Time synchronization.

Why is this not automated already?

It kind of is, but it often fails, and also fails to sync with enough accuracy.

I teach online and our calls always cut off 10-20 seconds sooner than the in-call countdown timer.

When comparing the system clock with an online clock (one that uses their server's computer time instead of my computer's clock), I found it to be 10+ seconds off! This is ridiculous.

{% hint style="info" %}
[Clock.zone](https://clock.zone/), “a website where you can find **real exact time**.”&#x20;

_“This clock shows time from our dedicated server synchronised with atomic clock.”_
{% endhint %}

The "sync now" button in Windows Settings just doesn't seem to do the job properly. There are various possible reasons for this, but if it works _sometimes_, I really don't care about those reasons. It's a computer, it should keep trying to sync the time until it succeeds. Instead, my calls — timed by the second — are consistently inconsistent.

## How to synchronize the system clock manually

Windows has a setting in the Control Panel for synchronizing to any time server you like, and already has two options included. You can choose what you like, as some time servers may be blocked in your country or region, or by your ISP[^1].

To find this, go to:

{% hint style="info" %}
Windows Settings → Time & language → Date & time → Additional clocks
{% endhint %}

<figure><img src="../../.gitbook/assets/image (5).png" alt=""><figcaption><p>Click "Additional clocks"</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (1) (1).png" alt=""><figcaption><p>Choose the "Internet Time" tab, then click "Change settings..."</p></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (2) (1).png" alt=""><figcaption><p>Select or paste your chosen time server URL, then click "Update now".</p></figcaption></figure>

Select or paste your chosen time server address into the server text box, then click "Update now" and wait for a few moments. If it fails, click it a few more times, and if it still fails, find a new time server. You can also check if the URL is alive by using a terminal/CMD app to ping the server:

```bash
ping time.nist.gov 
```

And there you have it!

If it worked, now your clock should be accurate to within a second, hopefully within a few milliseconds.

Here's a screenshot comparing the real-time clock website with my system clock:

<figure><img src="../../.gitbook/assets/image (3) (1).png" alt=""><figcaption><p>From <a href="https://clock.zone/">Clock.Zone</a> </p></figcaption></figure>

You can see that they are near-enough identical.

***

## Automating time synchronization

Ok, now to automate this synchronization task.

Windows should already do this, but apparently it does not.

Let's explore Task Scheduler.

Task Scheduler is an incredibly powerful automation tool, it can be triggered by thousands of system event hooks so you can automatically run any command for practically any event.

Search online to find out more about Task Scheduler and all that you can do with it!

How to do it:

{% hint style="info" %}
Task Scheduler → "Action" menu → **Create Basic Task**
{% endhint %}

### Create Basic Task

Add a name as you like. Add a description if you want.

<figure><img src="../../.gitbook/assets/image (4) (1).png" alt=""><figcaption></figcaption></figure>

Tell it to start when the computer starts — or whenever you want.

<figure><img src="../../.gitbook/assets/image (5) (1).png" alt=""><figcaption></figcaption></figure>

Tell it that you want to start a program.

<figure><img src="../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Type <mark style="color:red;">`w32tm`</mark> in the Program box, and <mark style="color:red;">`/resync`</mark> in the Add arguments box.
{% endhint %}

<figure><img src="../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

Check the summary on the Finish page.

Tick the checkbox for "Open the Properties dialog for this task when I click Finish",

then click Finish.

<figure><img src="../../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

### General tab

When the Properties dialog opens, set it to:

* Run whether user is logged on or not
* Run with highest privileges
* Configure for: Windows 10

<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

### Triggers tab

Change to the Triggers tab and click New to add a new trigger.

Set:

* Log: Microsoft-Windows-NetworkProfile/Operational
* Source: NetworkProfile
* Event ID: 10000
* Delay task for: 30 seconds
* Enabled

<figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

Press OK to close the window.

### Conditions tab

Change to the Conditions tab:

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

### Settings tab

Finally, check the Settings tab.

* Allow task to be run on demand
* If the task fails, restart every: **1 minute**
* Stop if the task runs longer than: **1 hour**
* If the running task does not end when requested, force it to stop

<figure><img src="../../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

Press OK to close the window.

Your time synchronization task is complete!

I can't remember clearly but I _think_ Windows asked me for my password on the first time the task was automatically run. This is because the programme <mark style="color:red;">`w32tm`</mark> needs Administrator privileges to operate.

[^1]: Internet Service Provider
