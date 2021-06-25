#####################################################################
Discord Rich Presence (64-bit Wineskins / WS-11 WineskinServer)
#####################################################################

.. rst-class:: wineskin-version
    
    | This article is applicable to the following wrappers:
    | • `Technocoder <https://osu.ppy.sh/users/10338558>`_'s `Wineskin with macOS Catalina 10.15 support <https://osu.ppy.sh/community/forums/topics/1106057>`_

.. note::

    This section is for users using Wineskins which use the **WS11WineCX19.0.1-1** or **WS11WineCX64Bit19.0.1-1** Wine engine from `Gcenx <https://github.com/Gcenx/WineskinServer>`_. **To find your Wineskin version:**

    1. Locate where ``osu!.app`` is installed
    2. Right click on it and select **Show Package Contents**
    3. You should now see three files/folders: ``Contents``, ``drive_c`` and ``Wineskin``. Click ``Wineskin``
    4. A window should pop up. Click **Advanced**
    5. It will be displayed under the **Associated Extensions** column, as shown below.

    .. image:: ../assets/wineskin-engine-version.png
        :alt: Wineskin Advanced, highlighting the engine version number:
    
    If you're **not** using one of the two **WS11** engines mentioned above, then the process behind Discord Rich Presence is slightly different - `you will encounter difficulties with getting Discord Rich Presence to work on macOS <discord-10-14.html>`_.


**Technocoder's Wineskin with support for macOS 10.15 Catalina and later** Wineskin should already have Discord Rich Presence installed. Otherwise, follow the Resolution steps below.

****************************************
Resolution
****************************************

This is directly taken from Technocoder's `macOS Updated Wineskin Installation Guide (Catalina support) <https://osu.ppy.sh/community/forums/posts/7560723>`_:

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

Discord Rich Presence at the moment is a bit fiddly, and currently it seems that `other people have been having issues too <https://osu.ppy.sh/community/forums/topics/1046150>`_.

If you're interested in the technical tidbits, see `Discord Rich Presence: Discussion <discord-disc.html>`_.