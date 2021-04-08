# Snippets for LED Colors
---

The Loupedeck CT and Loupedeck Live Preferences panels now have the ability to use Lua Snippets to set what color you want an LED button to use.

The Snippet should return a [`hs.drawing.color`](http://www.hammerspoon.org/docs/hs.drawing.color.html) object.

You can learn more about Lua on the [CommandPost Developers site](https://dev.commandpost.io/lua/lua-overview).

---

# Examples

## Return the color red

```lua
return hs.drawing.color.asRGB({hex="#FF0000"})
```