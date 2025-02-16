---
description: Fighting MaleficAms.C and Quasar.GG!MTB // 30th January 2025
---

# MaleficAms & Quasar

This torrent: rarbgo dot to/torrent/fontlab-8-0-0-8222-neverb-5320179.html , contains a crack.zip file. The crack is a virus. It didn't flash anything up on my screen for 2 days but when it did, I spent several hours chasing it around my system. <mark style="color:red;">**DO NOT USE IT.**</mark> It seems to be one of the new virus types that collects your browser's logged-in session tokens and sends them to a hacker.

The crack file doesn't contain much, but it activates a remote script, which then downloads other files and hides them around your system.

It also created two tasks in Task Scheduler, which ran every time the computer woke up from sleep.

## IMPORTANT FIRST STEPS

* Make sure you activate tasks history: **Task scheduler → Action menu → Enable All Tasks History**.&#x20;
* Also **get ProcExp from Microsoft's SysInternals**, it's more powerful than Task Manager (and also way more lightweight, who even made Task Manager heavy?). _Run it as administrator._&#x20;
* Disable your internet connection. If you don't trust that your wifi is fully off, create a firewall block rule that **blocks&#x20;**_**everything**_**&#x20;outbound**.&#x20;
* Check **Windows Security → Virus & threat protection settings → Exclusions**. Make sure that NO folders or files are excluded. (Check the same thing in your antivirus app if you're using something else.)

## All the files that I found

Here I'll list all the places I found files. The file names may be different for you.&#x20;

<details>

<summary>Task Scheduler → "<mark style="color:red;"><strong>WindowsUpdate_Service</strong></mark><strong>"</strong> </summary>

## **WindowsUpdate\_Service**

There is a task in Task Scheduler. It was called **WindowsUpdate\_Service**, and it was in the main tasks list (not in a Windows or Microsoft list).

Needless to say, it is not the real Windows update service.

</details>

<details>

<summary>Task Scheduler → <mark style="color:red;"><strong>8026C5C2-</strong>...</mark>...</summary>

Later, there was another task in there too, with a crazy numeric name.&#x20;

## _**8026C5C2-B019-46B0-B0F4-0583866B9AC8**_

The Task Scheduler app is crap, it'll show you a list of tasks in the Task Status section but clicking the tasks doesn't take you to the task entry.&#x20;

Mine was called _**8026C5C2-B019-46B0-B0F4-0583866B9AC8**_. It might have a different name in your situation.&#x20;

Use [**Everything**](https://www.voidtools.com/downloads/) (or similar search indexer), type the task name in, it will display its file.&#x20;

Delete it via Everything.&#x20;

It was hiding in Task Scheduler under Microsoft/Windows/Management/Provisioning.&#x20;

It interacted with a registry key (details below).

</details>

<details>

<summary>Startup → <mark style="color:red;">dwm.bat</mark> </summary>

## **dwm.bat**

There is a bat script disguised as DWM in your startup apps.&#x20;

</details>

<details>

<summary>C:\Users\Public\ → <mark style="color:red;">5.vbs</mark> </summary>

## 5.vbs&#x20;

There is a vbs script in c/users/public.&#x20;

</details>

<details>

<summary>%LOCALAPPDATA%\Temp\ → <mark style="color:red;">c.bat</mark></summary>

## c.bat&#x20;

There is a bat script in C:\Users\\<mark style="color:blue;">username</mark>\AppData\Local\Temp.

You can reach the Local AppData directory by putting its "shortcut" in the file browser address bar:&#x20;

<pre><code><strong>%LOCALAPPDATA%
</strong></code></pre>

And directly reach the Temp directory with:&#x20;

```
%LOCALAPPDATA%\Temp 
```

</details>

<details>

<summary>%LOCALAPPDATA%\Temp\ → <mark style="color:red;"><strong>xjLsh7ECs8mU.exe</strong></mark> </summary>

## **xjLsh7ECs8mU.exe**&#x20;

It also put another file into appdata/local/temp after I dealt with the virus a couple of times, before I found the task scheduler entries.&#x20;

This file name looks randomly generated; yours will likely have a different name.&#x20;

```
%LOCALAPPDATA%\Temp
```

</details>

There may have been some more files but I forgot where they were.

There's also a registry key masquerading as a Realtek device entry. **HKey Local Machine / Software / RealtekgaNtkX0 / NtkX0rW**.

<details>

<summary>Registry → <mark style="color:red;"><strong>RealtekgaNtkX0 / NtkX0rW</strong></mark></summary>

There's also a registry key masquerading as a Realtek device entry.&#x20;

**HKey Local Machine / Software / RealtekgaNtkX0 / NtkX0rW**.

_I recommend using_ [_**Registry Finder**_](https://registry-finder.com/) _to edit your registry, because it has undo built into the app. As far as I can tell, you can undo something that you changed previously, even days or weeks ago._&#x20;

Paste this address into the address bar in your registry editor app. In your case, it might have a different name.&#x20;

```
HKEY_LOCAL_MACHINE\SOFTWARE\RealtekgaNtkX0
```

I found this name via the task in the Task Scheduler — read the actions tab, it'll show you what commands are to be executed when the task is triggered. This is where I found the name of the registry key. Yours may be masquerading as a different device or brandname.&#x20;

</details>

## Defence

### You, fighting it in realtime

The rogue code kept launching new **powershell** instances, and sometimes **CMD** instances.

Watch for them in ProcExp.&#x20;

You can sort the processes by PID so the newest processes should appear at the top of the list.&#x20;

### Windows Security

The virus also added `powershell.exe` and my entire `C:\` drive to the Windows Security antivirus exclusions list, so I was getting notifications from Windows Security that no threats had been found. Once I removed all exclusions from the list, it detected one virus, then later, the other one.&#x20;

<figure><img src="../../../.gitbook/assets/Screenshot 2025-01-30 151824.png" alt=""><figcaption></figcaption></figure>

Windows Security finally detected two viruses:

1. Win32/**MaleficAms.C** — _This program is dangerous and executes commands from an attacker._&#x20;
2. MSIL/**Quasar.GG!MTB** — _This program provides remote access to the computer it is installed on._&#x20;

This was after I had deleted the other files by myself, so your antivirus software may detect more than mine did. I also uploaded the virus files to VirusTotal, and it shows that some antivirus software doesn't detect these files at all! Check out the links to pages on VirusTotal below.

## Files checked on VirusTotal:

1. **LbuDYVey.ps1** — This seems to be the originating file from which the chain of events started — [https://www.virustotal.com/gui/file/5afdc33f02df4604b5610fe0c31131a889df29687353b1c0f300c1cf791192cb](https://www.virustotal.com/gui/file/5afdc33f02df4604b5610fe0c31131a889df29687353b1c0f300c1cf791192cb)
2. **5.vbs** (base64 powershell directives) — [https://www.virustotal.com/gui/file/a63181dff0f68b98712247f51c8a6e7761f8a84261928c297b12f438272c1492](https://www.virustotal.com/gui/file/a63181dff0f68b98712247f51c8a6e7761f8a84261928c297b12f438272c1492)
3. **c.bat** AND **dwm.bat** —  [https://www.virustotal.com/gui/file/d2ca5cb28153f404d84cad9dd6b28725015527625a262d3b6471e0458f5ecb85](https://www.virustotal.com/gui/file/d2ca5cb28153f404d84cad9dd6b28725015527625a262d3b6471e0458f5ecb85)
4. _**8026C5C2-B019-46B0-B0F4-0583866B9AC8**_ (in Task Scheduler) — [https://www.virustotal.com/gui/file/257a73e0adedae700e848f36cbcf4198d478fb8cb4aab2855ebef496c7fca60d](https://www.virustotal.com/gui/file/257a73e0adedae700e848f36cbcf4198d478fb8cb4aab2855ebef496c7fca60d)
5. _**RealtekgaNtkX0 / NtkX0rW**_ — The registry key that was added — [https://www.virustotal.com/gui/file/bf0814ba984aac3d577d45da9b06da36443c523241ec083120874cdacf65bf6c](https://www.virustotal.com/gui/file/bf0814ba984aac3d577d45da9b06da36443c523241ec083120874cdacf65bf6c)&#x20;
6. **crack.zip file** — The crack.zip that was contained as the cracking method — [https://www.virustotal.com/gui/file/d2b9cbc27e4328493cc918110de5d2c3339f79075466311b3b45a72faf86fe76](https://www.virustotal.com/gui/file/d2b9cbc27e4328493cc918110de5d2c3339f79075466311b3b45a72faf86fe76/detection) &#x20;
7. **Patch.exe** — The activator executable inside the crack.zip file — [https://www.virustotal.com/gui/file/7dbc709cf291f300f458170fa4552e8a85187afc56b72ad073ffc4ea0d026c61](https://www.virustotal.com/gui/file/7dbc709cf291f300f458170fa4552e8a85187afc56b72ad073ffc4ea0d026c61)&#x20;
8. **evbda.sys** — A benign system file, distributed by Microsoft. It was included in the crack.zip file. [https://www.virustotal.com/gui/file/48d9f61e943a7855562950ff26b866bd51a27d980757b065504fcd3f1a1d6f07](https://www.virustotal.com/gui/file/48d9f61e943a7855562950ff26b866bd51a27d980757b065504fcd3f1a1d6f07)&#x20;

<details>

<summary>The magnet URI for the torrent that contains this crack. <mark style="color:red;">Do NOT USE IT</mark>. I have included it only for you to check if you are downloading a bad torrent. </summary>

magnet:?xt=urn:btih:28ED2F2AC95B9326D10647D012B5A07F1D2BBEF2\&dn=FontLab+8.0.0.8222+%5BNeverb%5D\&tr=udp%3A%2F%2Ftracker.openbittorrent.com%3A80%2Fannounce\&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce\&tr=udp%3A%2F%2Ftracker.pirateparty.gr%3A6969%2Fannounce\&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce\&tr=udp%3A%2F%2Ftracker.torrent.eu.org%3A451%2Fannounce\&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce\&tr=udp%3A%2F%2Fipv4.tracker.harry.lu%3A80%2Fannounce\&tr=udp%3A%2F%2Fopen.stealth.si%3A80%2Fannounce\&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce\&tr=udp%3A%2F%2Ftracker.cyberia.is%3A6969%2Fannounce\&tr=udp%3A%2F%2Ftracker.internetwarriors.net%3A1337%2Fannounce\&tr=udp%3A%2F%2Ftracker.open-internet.nl%3A6969%2Fannounce\&tr=udp%3A%2F%2Ftracker.zer0day.to%3A1337%2Fannounce\&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce\&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce\&tr=http%3A%2F%2Ftracker.openbittorrent.com%3A80%2Fannounce\&tr=udp%3A%2F%2Fopentracker.i2p.rocks%3A6969%2Fannounce\&tr=udp%3A%2F%2Ftracker.internetwarriors.net%3A1337%2Fannounce\&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce\&tr=udp%3A%2F%2Fcoppersurfer.tk%3A6969%2Fannounce\&tr=udp%3A%2F%2Ftracker.zer0day.to%3A1337%2Fannounce

</details>

