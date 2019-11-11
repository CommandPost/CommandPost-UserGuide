# Snippets
---

CommandPost allows you to trigger code snippets as an action.

For example, to launch Final Cut Pro, you can write:

`cp.apple.finalcutpro:launch()`

CommandPost is compatible with Hammerspoon, so you can also use any of the examples on the Hammerspoon website:

http://www.hammerspoon.org/go/

---

# Examples

## Select all even clips in a timeline

```lua
cp.apple.finalcutpro:launch()
local clips = cp.apple.finalcutpro:timeline():contents():clipsUI()
table.sort(clips, function(a, b) return a:position().x < b:position().x end)
local evenClips = {}
for i, clip in ipairs(clips) do
    if (i % 2 == 0) then
        table.insert(evenClips, clip)
    end
end
cp.apple.finalcutpro:timeline():contents():selectClips(evenClips)
```

## Go back 500 frames and play

```lua
hs.eventtap.keyStroke({}, "-")
hs.eventtap.keyStrokes("2000")
hs.eventtap.keyStroke({}, "return")
cp.apple.finalcutpro:doShortcut("JogForward"):Now()
```