# Frequently Asked Questions
---

## Why did you remove "Moveable Markers"?

Moveable Markers was [first discovered](http://alex4d.com/notes/item/fcpx-movable-markers) by Alex Goldner back in June 2014.

To enable it, you basically just need to toggle a boolean hidden within a preference file inside the Final Cut Pro Library.

In the early days of [FCPX Hacks](https://latenitefilms.com/blog/fcpx-hacks) we added an option for Moveable Markers which enables them using the same technique Alex found, except it allowed users to easily toggle the feature on and off using the menu bar or shortcut keys.

When we transitioned FCPX Hacks to CommandPost, we kept this feature, however we've since decided that it's probably a bad idea to modify the contents of the Final Cut Pro application bundle, so we removed this feature all together, along with other features that modify the contents of the Final Cut Pro application bundle (such as inserting our commands into the Final Cut Pro Command Editor).

We want CommandPost to be as safe and reliable as possible, and we want to avoid using "hacks" to make things happen.

The easiest way to enable Moveable Markers is via Terminal.

The below assumes you have Final Cut Pro installed within the `/Applications` folder.

This will enable them:

`sudo /usr/libexec/PlistBuddy -c "Set :TLKMarkerHandler:Configuration:'Allow Moving Markers' true" '/Applications/Final Cut Pro.app/Contents/Frameworks/TLKit.framework/Versions/A/Resources/EventDescriptions.plist'`

This will disable them:

`sudo /usr/libexec/PlistBuddy -c "Set :TLKMarkerHandler:Configuration:'Allow Moving Markers' false" '/Applications/Final Cut Pro.app/Contents/Frameworks/TLKit.framework/Versions/A/Resources/EventDescriptions.plist'`