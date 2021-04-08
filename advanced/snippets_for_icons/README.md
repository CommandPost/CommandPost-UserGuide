# Snippets for Icons
---

The Loupedeck CT and Loupedeck Live Preferences panels now have the ability to use Lua Snippets to generate icons for the Loupedeck devices.

This gives you incredible freedom, to programatically make the icons appear however you want.

CommandPost is also compatible with Hammerspoon, so you can also use helpful extensions such as [`hs.canvas`](http://www.hammerspoon.org/docs/hs.canvas.html).

You can learn more about Lua on the [CommandPost Developers site](https://dev.commandpost.io/lua/lua-overview).

---

# Examples

## Use a built-in system icon

```lua
return hs.image.imageFromName("NSAdvanced")
```

---

## Display the first FCPX Keyword Shortcut Value

```lua
local v = hs.canvas.new{x = 0, y = 0, w = 90, h = 90 }
v[1] = {
    frame = { h = "100%", w = "100%", x = 0, y = 0 },
    fillColor = { alpha = 1, red = 0, green = 0, blue = 0 },
    type = "rectangle",
}

v[2] = {
    frame = { h = "100%", w = "100%", x = 0, y = 0 },
    text = "\n\n" .. cp.apple.finalcutpro.preferences.FFKeywordGroups[1][1],
    textAlignment = "center",
    textColor = { white = 1.0 },
    textSize = 15,
    type = "text",
}

return v:imageFromCanvas()
```