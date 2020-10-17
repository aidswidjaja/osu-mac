#############################################
Discord Rich Presence (10.15+)
#############################################

.. rst-class:: wineskin-version
    
    | This article is applicable to the following wrappers:
    | • `Technocoder <https://osu.ppy.sh/users/10338558>`_'s `Wineskin with macOS Catalina 10.15 support <https://osu.ppy.sh/community/forums/topics/1106057>`_

.. note::

    This section is for users on macOS 10.15 and later. For information about Rich Presence on 10.14 and earlier, click `here <discord-10-14.html>`_

The **macOS 10.15 Catalina and later** Wineskin already has Discord Rich Presence installed.

If for some reason it isn't working, follow these steps.

****************************************
Resolution
****************************************

This is directly taken from Technocoder's `macOS Updated Wineskin Installation Guide (Catalina support) <https://osu.ppy.sh/community/forums/posts/7560723>`_:

::

    1. Download `bridge.exe <https://github.com/Techno-coder/macOS-wine-bridge/raw/master/bridge.exe>`_
    2. Right click **osu!** > **Show Package Contents**
    3. Go to ``drive_c`` > ``osu!``
    4. Drag the **bridge.exe** file into the osu! folder
    5. Create a new file in the ``osu!`` folder named ``execute.bat``
    6. Add these two lines to the ``execute.bat`` file:

    .. code-block::

        start C:\osu!\bridge.exe
        start C:\osu!\osu!.exe -nosplash

    7. Open **Wineskin** (next to the ``drive_c`` folder)
    8. Click **Advanced**
    9. Change the **Windows EXE field** to (including the outer quotes):

    .. code-block::

        "C:\osu!\execute.bat"

****************************************
If that didn't work
****************************************

Discord Rich Presence at the moment is a bit fiddly. As an FYI, it seems that `other people have been having issues too <https://osu.ppy.sh/community/forums/topics/1046150>`_.

If you're interested in the technical tidbits, see `Discord Rich Presence: Discussion <discord-disc.html>`_.