#############################################
osu! doesn't run on macOS Monterey
#############################################

.. rst-class:: wineskin-version
    
    | This article is applicable to the following wrappers:
    | • `slc <https://osu.ppy.sh/users/7978076>`_'s `Wineskin for macOS 10.14 Mojave and earlier <https://osu.ppy.sh/community/forums/topics/682197?start=6919344>`_
    | • `Technocoder <https://osu.ppy.sh/users/10338558>`_'s `Wineskin with macOS Catalina 10.15 support <https://osu.ppy.sh/community/forums/topics/1106057>`_
    | • `Technocoder <https://osu.ppy.sh/users/10338558>`_'s `unofficial Wineskin for macOS 10.14 Mojave and earlier <https://osu.ppy.sh/community/forums/topics/682197>`_

****

****************************************
Behaviour
****************************************

macOS doesn't run on macOS Monterey 12.0.

****

****************************************
Cause
****************************************

An upstream thread 0 exception is the cause of this bug, and is currently being looked at by CodeWeavers and Apple. More information is available at `Gcenx/WineskinServer#139 <https://github.com/Gcenx/WineskinServer/issues/139>`_

****

****************************************
Resolution
****************************************

Update your version of macOS Monterey to any version after Beta 5.

macOS Monterey should work with the latest version of osu! wrappers when using versions of macOS Monterey after Beta 5, but if you are experiencing issues then please let us know in the `forums <https://osu.ppy.sh/community/forums/topics/1106057>`_.

****

****************************************
If that didn't work
****************************************

There could be something else going on here, and performing `basic troubleshooting <troubleshooting.html>`_ should help you get to the bottom of it.

If you're still not sure what's going on here, copy any osu! crash logs and `generate a report with osu!macOS Agent <troubleshooting.html#generating-a-report-with-osu-macos-agent>`_, then let us know on the forums with what we can help.