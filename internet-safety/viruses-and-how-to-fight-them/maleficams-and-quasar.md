---
description: Fighting MaleficAms.C and Quasar.GG!MTB // 30th January 2025
---

# MaleficAms & Quasar

This torrent: rarbgo dot to/torrent/fontlab-8-0-0-8222-neverb-5320179.html , contains a crack.zip file. The crack is a virus. It didn't flash anything up on my screen for 2 days but when it did, I spent several hours chasing it around my system. <mark style="color:red;">**DO NOT USE IT.**</mark> It seems to be one of the new virus types that collects your browser's logged-in session tokens and sends them to a hacker.

The crack file doesn't contain much, but it activates a remote script, which then downloads other files and hides them around your system.

* Make sure you activate tasks history: **Task scheduler → Action menu → Enable All Tasks History**.&#x20;
* Also **get ProcExp from Microsoft's SysInternals**, it's more powerful than Task Manager (and also way more lightweight, who even made Task Manager heavy?).&#x20;
* Disable your internet connection. If you don't trust that your wifi is fully off, create a firewall block rule that **blocks&#x20;**_**everything**_**&#x20;outbound**.&#x20;
* Check **Windows Security → Virus & threat protection settings → Exclusions**. Make sure that NO folders or files are excluded.

Here I'll list all the places I found files. The file names may be different for you.&#x20;

There is a task in Task Scheduler. It was called **WindowsUpdate\_Service**, and it was in the main tasks list (not in a Windows or Microsoft list).

Later, there was another task in there too, with a crazy numeric name. The Task Scheduler app is crap, it'll show you a list of tasks in the Task Status section but clicking the tasks doesn't take you to the task entry. Use Everything (or similar search indexer), type the task name in, it will display its file. Delete it via Everything. Mine was called **8026C5C2-**... It was hiding in Task Scheduler under Microsoft/Windows/Management/Provisioning. It interacted with a registry key (details below).

There is a bat script disguised as DWM in your startup apps. **dwm.bat**&#x20;

There is a vbs script in c/users/public. **5.vbs**&#x20;

There is a bat script in appdata/local/temp. **c.bat**&#x20;

There may have been some more files but I forgot where they were.

It also put another file into appdata/local/temp after I dealt with the virus a couple of times, before I found the task scheduler entries. **xjLsh7ECs8mU.exe**&#x20;

There's also a registry key masquerading as a Realtek device entry. **HKey Local Machine / Software / RealtekgaNtkX0 / NtkX0rW**.

The rogue code keeps launching new **powershell** instances, and sometimes **CMD** instances. Watch for them in ProcExp. You can sort the processes by PID so the newest processes should appear at the top of the list. It also added my entire C drive to the Windows Security antivirus exclusions list, so I was getting notifications from Security that no threats were found.

Windows Security finally detected it as:

1. Win32/**MaleficAms.C** — _This program is dangerous and executes commands from an attacker._&#x20;
2. MSIL/**Quasar.GG!MTB** — _This program provides remote access to the computer it is installed on._&#x20;

Files checked on VirusTotal:

1. **LbuDYVey.ps1** — This seems to be the originating file from which the chain of events started — https://www.virustotal.com/gui/file/5afdc33f02df4604b5610fe0c31131a889df29687353b1c0f300c1cf791192cb
2. **5.vbs** (base64 powershell directives) — https://www.virustotal.com/gui/file/a63181dff0f68b98712247f51c8a6e7761f8a84261928c297b12f438272c1492
3. **c.bat** AND **dwm.bat** —  https://www.virustotal.com/gui/file/d2ca5cb28153f404d84cad9dd6b28725015527625a262d3b6471e0458f5ecb85
4. _**8026C5C2-B019-46B0-B0F4-0583866B9AC8**_ (in Task Scheduler) — https://www.virustotal.com/gui/file/257a73e0adedae700e848f36cbcf4198d478fb8cb4aab2855ebef496c7fca60d
5. _**RealtekgaNtkX0 / NtkX0rW**_ — The registry key that was added — https://www.virustotal.com/gui/file/bf0814ba984aac3d577d45da9b06da36443c523241ec083120874cdacf65bf6c&#x20;

<details>

<summary>The magnet URI for the torrent that contains this crack. <mark style="color:red;">Do NOT USE IT</mark>. I have included it only for you to check if you are downloading a bad torrent. </summary>

magnet:?xt=urn:btih:28ED2F2AC95B9326D10647D012B5A07F1D2BBEF2\&dn=FontLab+8.0.0.8222+%5BNeverb%5D\&tr=udp%3A%2F%2Ftracker.openbittorrent.com%3A80%2Fannounce\&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce\&tr=udp%3A%2F%2Ftracker.pirateparty.gr%3A6969%2Fannounce\&tr=udp%3A%2F%2Ftracker.tiny-vps.com%3A6969%2Fannounce\&tr=udp%3A%2F%2Ftracker.torrent.eu.org%3A451%2Fannounce\&tr=udp%3A%2F%2Fexplodie.org%3A6969%2Fannounce\&tr=udp%3A%2F%2Fipv4.tracker.harry.lu%3A80%2Fannounce\&tr=udp%3A%2F%2Fopen.stealth.si%3A80%2Fannounce\&tr=udp%3A%2F%2Ftracker.coppersurfer.tk%3A6969%2Fannounce\&tr=udp%3A%2F%2Ftracker.cyberia.is%3A6969%2Fannounce\&tr=udp%3A%2F%2Ftracker.internetwarriors.net%3A1337%2Fannounce\&tr=udp%3A%2F%2Ftracker.open-internet.nl%3A6969%2Fannounce\&tr=udp%3A%2F%2Ftracker.zer0day.to%3A1337%2Fannounce\&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce\&tr=udp%3A%2F%2Ftracker.opentrackr.org%3A1337%2Fannounce\&tr=http%3A%2F%2Ftracker.openbittorrent.com%3A80%2Fannounce\&tr=udp%3A%2F%2Fopentracker.i2p.rocks%3A6969%2Fannounce\&tr=udp%3A%2F%2Ftracker.internetwarriors.net%3A1337%2Fannounce\&tr=udp%3A%2F%2Ftracker.leechers-paradise.org%3A6969%2Fannounce\&tr=udp%3A%2F%2Fcoppersurfer.tk%3A6969%2Fannounce\&tr=udp%3A%2F%2Ftracker.zer0day.to%3A1337%2Fannounce

</details>

