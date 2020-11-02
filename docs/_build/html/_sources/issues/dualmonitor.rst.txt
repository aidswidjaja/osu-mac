####################################################
osu! captures my monitor/my second monitor is black
####################################################

.. rst-class:: wineskin-version
    
    | This article is applicable to the following wrappers:
    | • `slc <https://osu.ppy.sh/users/7978076>`_'s `Wineskin for macOS 10.14 Mojave and earlier <https://osu.ppy.sh/community/forums/topics/682197?start=6919344>`_
    | • `Technocoder <https://osu.ppy.sh/users/10338558>`_'s `Wineskin with macOS Catalina 10.15 support <https://osu.ppy.sh/community/forums/topics/1106057>`_
    | • `Technocoder <https://osu.ppy.sh/users/10338558>`_'s `unofficial Wineskin for macOS 10.14 Mojave and earlier <https://osu.ppy.sh/community/forums/topics/682197>`_

****

****************************************
Behaviour
****************************************

osu! has made all other windows inaccessible, and if a secondary monitor is connected, only your primary one is available.

****

****************************************
Cause
****************************************

When using the Mac driver with osu!, osu! will go into fullscreen mode and prevent other applications or system elements (like the volume control) from drawing on top of it. It's great for performance, but can be annoying to play with osu! (especially since you won't be able to drag and drop beatmaps into your Songs folder)

Learn more `at the Apple Developer Quartz documentation website.<https://developer.apple.com/library/content/documentation/GraphicsImaging/Conceptual/QuartzDisplayServicesConceptual/Articles/DisplayCapture.html>`_.

****

****************************************
Resolution
****************************************

These instructions are directly taken from Technocoder's `macOS troubleshooting guide <https://osu.ppy.sh/community/forums/topics/679205>`_.

    1. Click "Registry Editor" (Under the "Tools" tab in Wineskin in the left column)
    2. Go to this registry folder: HKEY_CURRENT_USER > Software > Wine > Mac Driver
    3. Double click on "CaptureDisplaysForFullscreen"
    4. Change "Y" to "n" in the text box
    5. Click "OK"
    6. Close the "Registry Editor" window

****

****************************************
If that didn't work
****************************************

There could be something else going on here, and performing `basic troubleshooting <troubleshooting.html>`_ should help you get to the bottom of it.

If you're still not sure what's going on here, copy any osu! crash logs and `generate a report with osu!macOS Agent <troubleshooting.html#generating-a-report-with-osu-macos-agent>`_, then let us know on the forums with what we can help.