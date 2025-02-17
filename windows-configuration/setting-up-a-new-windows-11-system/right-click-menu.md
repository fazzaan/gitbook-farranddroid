# Right-Click Menu

The new Windows 11 ~~file explorer~~ everything is _abysmal_.

Windows's very own file explorer app runs like dogshit and opens like dogshit and even the "new" "smaller" context menu (often called the _right-click menu_) takes a month to appear.

It's got weird JTL (just too late) lazy-loading of "open with" apps that support each file type, resulting in the most fucking idiotic menu apparition known to humankind:



Anyway,

## Reviving the old Context Menu

Open Windows Terminal (or whatever terminal app you use)

Run this:

```
reg.exe add "HKCU\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}\InprocServer32" /f /ve
```

This command adds a key to the Windows registry that sets the "old style" full context menu as the default menu. No more Right-Click → Show more options, or Shift+Right-Click. Just a single Right-Click is all you need, to see the full context menu!

## Restoring the standard Windows 11 Context Menu

Open Windows Terminal (etc.) again.

Run this:

```
reg.exe delete "HKCU\Software\Classes\CLSID\{86ca1aa0-34aa-4e8b-a509-50c905bae2a2}\InprocServer32" /f
```

This command deletes the same key that we just created.

