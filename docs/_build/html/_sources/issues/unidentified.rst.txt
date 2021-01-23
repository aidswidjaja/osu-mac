##########################################################################################
osu! cannot be opened because the developer cannot be verified
##########################################################################################

.. rst-class:: wineskin-version
    
    | This article is applicable to the following wrappers:
    | • `slc <https://osu.ppy.sh/users/7978076>`_'s `Wineskin for macOS 10.14 Mojave and earlier <https://osu.ppy.sh/community/forums/topics/682197?start=6919344>`_
    | • `Technocoder <https://osu.ppy.sh/users/10338558>`_'s `Wineskin with macOS Catalina 10.15 support <https://osu.ppy.sh/community/forums/topics/1106057>`_
    | • `Technocoder <https://osu.ppy.sh/users/10338558>`_'s `unofficial Wineskin for macOS 10.14 Mojave and earlier <https://osu.ppy.sh/community/forums/topics/682197>`_
    | as well as `Technocoder <https://osu.ppy.sh/users/10338558>`_'s `osu!macOS Agent <https://osu.ppy.sh/community/forums/topics/1036678>`_ program

****

****************************************
Behaviour
****************************************

Your Mac displays a warning saying one of either two messages:

- "osu!.app" cannot be opened because the developer cannot be verified.
- "osu!.app" can't be opened because it is from an unidentified developer.

****

****************************************
Cause
****************************************

To directly quote `Apple's support article <https://support.apple.com/en-au/guide/mac-help/mh40616/mac>`_:

    If you try to open an app that isn’t registered with Apple by an identified developer, you get a warning dialogue. This doesn’t necessarily mean that something’s wrong with the app. For example, some apps were written before developer ID registration began. However, the app has not been reviewed, and macOS can’t check whether the app has been modified or broken since it was released.

****

****************************************
Resolution
****************************************

1. Locate ``osu!.app`` in Finder
2. Right-click (or hold the `Control` key while clicking) on ``osu!.app``
3. Click **Open**

On the dialog that reads:

    "osu!.app" is an application downloaded from the Internet. Are you sure you want to open it?

Click **Open**.

****

****************************************
If that didn't work
****************************************

There could be something else going on here, and performing `basic troubleshooting <troubleshooting.html>`_ should help you get to the bottom of it.

If you're still not sure what's going on here, copy any osu! crash logs and `generate a report with osu!macOS Agent <troubleshooting.html#generating-a-report-with-osu-macos-agent>`_, then let us know on the forums with what we can help.