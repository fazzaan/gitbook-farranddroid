# Microsoft's Bloatware

## Phone Link

Nobody actually knows what Phone Link is for. They have been loitering in dark alleys and shadowy corners for years now, but still it won't come clean about their intentions.

Regardless, like a true ex, we have no need, desire or reasonable reason otherwise to stick around and try to find out.

Let's off it while we can.

If you open Task Manager, you'll see that it has launched itself, even if you've disabled it from Startup Apps _and_ disabled it in Services. It uses CPU fairly regularly. No idea why. Probably just wants attention.



Open PowerShell from the Start menu as Administrator:

{% hint style="info" %}
Start → PowerShell → Run as Administrator

![](<../../.gitbook/assets/image (11).png>)
{% endhint %}

Paste this command in PowerShell, then press enter:

{% code title="Uninstall Phone Link" %}
```powershell
Get-AppxPackage Microsoft.YourPhone -AllUsers | Remove-AppxPackage
```
{% endcode %}

Et voilà!

[_Source_](https://learn.microsoft.com/en-us/answers/questions/963543/uninstall-phone-link)&#x20;



## Superlist of uninstall commands

{% code title="Uninstall Phone Link" %}
```powershell
Get-AppxPackage Microsoft.YourPhone -AllUsers | Remove-AppxPackage
```
{% endcode %}

