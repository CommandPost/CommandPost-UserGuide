# Uninstalling CommandPost
---

To remove CommandPost from your system, simply drag the CommandPost application to the trash.

If you have enabled "Control CommandPost Shortcuts within Final Cut Pro", "Enable Moving Markers", or changed the "Smart Collection Label" or "Backup Interval", you should change these settings back to their defaults prior to uninstalling CommandPost.

The CommandPost preferences are located at:

`~/Library/Preferences/org.latenitefilms.CommandPost.plist`

This file can also be dragged to the Trash to remove CommandPost’s Preferences.

Any user created Extensions, Plugins, Shortcuts or Tangent Settings are stored within:

`~/Library/Application Support/CommandPost`

These can be also be removed if required.

CommandPost's WebKit, Crashlytics & Sparkle caches are stored within:

```
~/Library/Application Support/org.latenitefilms.CommandPost
~/Library/Caches/org.latenitefilms.CommandPost
~/Library/WebKit/org.latenitefilms.CommandPost
```

These folders can also be removed if required.