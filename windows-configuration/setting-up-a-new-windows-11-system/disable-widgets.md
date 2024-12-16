# Disable Widgets

You can go to different levels of disabling Widgets.

The most extreme would be to uninstall them, but I'm not sure if future Windows updates and OS version updates would reinstall them, so there are a few steps you can take.

* Disable the feed (app setting or [registry edit](#user-content-fn-1)[^1])
* Remove the widgets inside the Widgets panel
* Disable the Widgets keyboard shortcut
* Disable it from GPE (Group Policy Editor — [only in non-Home editions](#user-content-fn-2)[^2])
* Uninstall it using WinGet

## Disable the feed

## Remove the widgets

## Disable the Widgets keyboard shortcut

## Disable Widgets from Group Policy Editor

## Uninstall Widgets using WinGet

Go to Terminal or CMD and run this command:

```powershell
Winget uninstall "Windows Web Experience pack"
```

<figure><img src="../../.gitbook/assets/image (32).png" alt=""><figcaption></figcaption></figure>



[^1]: See page on using Registry Finder instead of RegEdit&#x20;

[^2]: See [upgrade-windows-edition.md](upgrade-windows-edition.md "mention") to escape the gaol of Windows Home!
