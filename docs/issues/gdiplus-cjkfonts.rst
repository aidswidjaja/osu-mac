########################################################################
osu! has graphical glitches, or isn't rendering icons/CJK fonts properly
########################################################################

.. rst-class:: wineskin-version
    
    | This article is applicable to the following wrappers:
    | • `slc <https://osu.ppy.sh/users/7978076>`_'s `Wineskin for macOS 10.14 Mojave and earlier <https://osu.ppy.sh/community/forums/topics/682197?start=6919344>`_
    | • `Technocoder <https://osu.ppy.sh/users/10338558>`_'s `Wineskin with macOS Catalina 10.15 support <https://osu.ppy.sh/community/forums/topics/1106057>`_
    | • `Technocoder <https://osu.ppy.sh/users/10338558>`_'s `Wineskin with Apple Silicon support <https://osu.ppy.sh/community/forums/topics/682197>`_
    | • `Technocoder <https://osu.ppy.sh/users/10338558>`_'s `unofficial Wineskin for macOS 10.14 Mojave and earlier <https://osu.ppy.sh/community/forums/topics/682197>`_

****

****************************************
Behaviour
****************************************

You're experiencing graphical glitches, including:

    - black bars
    - icons not loading
    - Chinese/Japanese/Korean fonts being replaced with X's or boxes

****

****************************************
Cause
****************************************

This arises out of minor incompatibilities. Specifically,

- gdiplus is required to reduce graphical glitches. gdiplus is not included for stability and compatibility reasons.
- cjkfonts is included, but will not work under gdiplus.
- osu! generally experiences graphical glitches not linked to either one of the above dependencies.

****

****************************************
Resolution
****************************************

The best way to mitigate this issue is to adjust your in-game settings. Some users find that enabling native resolution, or changing the screen resolution, leads to a better experience. **Do not enable Compatibility Mode as this will break your wrapper!!**

If adjusting in-game graphics settings doesn't work, options are provided below, but as stated, these are not advised and we do not recommend them.

Generally we recommend not to mess with anything unless you're sure what you're doing. If the graphical glitches are affecting your experience, there is a way to remove them, but this will cause CJK fonts not to load, and potentially cause more instability. 

.. danger::

    The following steps are not generally recommended. Perform at your own risk.

.. danger::

    If, despite our advice, you choose to enable gdiplus, make a backup before performing anything below. Ideally, work on a duplicate version.

=======================================
Enabling gdiplus
=======================================

.. danger::

    These steps will cause incompatibilities with cjkfonts.

1. Right click osu!.app
2. Click **Show Package Contents**
3. Click **Wineskin**
4. Click **Advanced**
5. Click the **Tools** tab
6. Click **Winetricks** under **Utilities**
7. Search for **gdiplus** which will be under the ``dlls`` section
8. Enable the checkbox next to it
9. Click the **Run** button, then the Yes in the dialog box that appears
10. You can click **Close** once it has finished, then close Wineskin

=======================================
Removing gdiplus (& keeping cjkfonts)
=======================================

1. Right click osu!.app
2. Click **Show Package Contents**
3. Navigate to ``drive_c/windows/system32/gdiplus.dll``
4. Rename ``gdiplus.dll`` to ``gdiplus.donotuse`` so Wine can't use it - make sure you change the file extension from ``dll`` to ``donotuse``

****

****************************************
If that didn't work
****************************************

There could be something else going on here, and performing `basic troubleshooting <troubleshooting.html>`_ should help you get to the bottom of it.

If you're still not sure what's going on here, copy any osu! crash logs and `generate a report with osu!macOS Agent <troubleshooting.html#generating-a-report-with-osu-macos-agent>`_, then let us know on the forums with what we can help.

****

****************************************
Related links
****************************************

- https://osu.ppy.sh/community/forums/posts/7929179
- https://osu.ppy.sh/community/forums/posts/7921057
- https://osu.ppy.sh/community/forums/posts/7922372