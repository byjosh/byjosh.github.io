## Better font anti-aliasing on 1080p or low resolution monitors on recent macOS versions
Problem: after macOS Mojave [apparently Apple removed sub-pixel anti-aliasing](https://discussions.apple.com/thread/250998388?sortBy=rank) - an effect that makes fonts smoother and less pixelated/jaggy.

My workaround: use a VGA connection - and maybe a DisplayPort connection.

### The story:
If the edges of your fonts looked jagged or pixelated then one will end up finding that anti-aliasing as part of [font rasterization](https://en.wikipedia.org/wiki/Font_rasterization) is part of what needs to happen for smooth fonts.
If using Microsoft Windows then the [ClearType](https://en.wikipedia.org/wiki/ClearType) [settings in Windows](https://uk.pcmag.com/migrated-3765-windows-10/140321/how-to-manage-your-fonts-in-windows) are something to investigate.

But in recent macOS versions Apple seems to base the system behaviour on folks using HiDPI monitors and so one can see jagged fonts on a full HD monitor. I discovered this connected to a 1080p Full HD monitor using a Mini DisplayPort to DVI adapter.

### Mitigation: try a VGA connection (and maybe a DisplayPort connection)
However I usually used a Mini DisplayPort to VGA adapter to connect to that monitor - and switching back from Mini DisplayPort to DVI to Mini DisplayPort to VGA confirmed that the VGA connection saw better font rendering (Mini DisplayPort adaptors were connecting to Thunderbolt 2 port on the Mac). 

This was on macOS Monterey - so cannot confirm for all newer versions of macOS. But if you use a 1920 x 1080 (1080p) monitor or a lower resolution one then I suggest trying a VGA adapter and seeing if the VGA output has better anti-aliasing and font display than a digital input to the monitor such as HDMI or DVI.

A Mini DisplayPort to DisplayPort connection on a 1920 by 1200 pixel monitor also looked comparatively good - suggesting trying a DisplayPort connection if you have a monitor with a DisplayPort input. 

What definitely looked bad for font rendering was Mini DisplayPort to DVI.

### Comment: why?
In terms of a logic to why things might be better on VGA at this resolution:- I have seen rendering speed being mentioned as a reason to turn off sub-pixel antialiasing in a context in which monitors can have much higher refresh rates as well as higher pixel counts. [This Apple Developer talk](https://developer.apple.com/videos/play/wwdc2021/10147/) covers ways in which displays might handle higher refresh rates. So while I cannot draw confident links between what I have observed and Apple changes it does seem to fit issues discussed in [more than](https://osxdaily.com/2022/04/06/change-remove-font-smoothing-macos/) [the Apple forums post](https://discussions.apple.com/thread/250998388?sortBy=rank) and digital monitor connections having to handle HiDPI monitors (that do not need subpixel rendering) and faster refresh rates (that put a premium on faster graphics rendering especially in context of HiDPI displays) it does make speed seem plausible cause for a change in font treatment.

So it does make a little more sense that VGA output might get a font treatment that takes more time but looks better at lower resolutions. Because in this situation - due to the age of VGA - the developers can be confident:-
* the monitor does not have a high refresh rate they are neglecting to utilise by doing things the slower way
* that any rendering techniques used, that are flagged as applying to VGA connections, will not be called on to render ultra high definition screens (again due to the age).
