#############################################
Discord Rich Presence (<10.14)
#############################################

.. rst-class:: wineskin-version
    
    | This article is applicable to the following wrappers:
    | • `slc <https://osu.ppy.sh/users/7978076>`_'s `Wineskin for macOS 10.14 Mojave and earlier <https://osu.ppy.sh/community/forums/topics/682197?start=6919344>`_
    | • `Technocoder <https://osu.ppy.sh/users/10338558>`_'s `unofficial Wineskin for macOS 10.14 Mojave and earlier <https://osu.ppy.sh/community/forums/topics/682197>`_

.. note::

    This section is for users on macOS 10.14 and earlier. If you use macOS 10.15 and later, then the process behind Discord Rich Presence is slightly different - `you actually can enable Discord Rich Presence with relative ease <10-15.html>`_.

****

****************************************
Behaviour
****************************************

osu! is not detected by Discord in the Game Activity menu, nor is it displayed on your profile.

.. image:: ../assets/discord-rpc.png

****

****************************************
Cause
****************************************

`It's complicated. <discord-disc.html>`_ 

`And other people had a few issues too. <https://osu.ppy.sh/community/forums/topics/1046150>`_

**Tl;dr:** noone has made a successful Discord Rich Presence solution running under macOS 32-bit Wineskins.

****

****************************************
Resolution
****************************************

If you read my `Discord Rich Presence discussion article <discord-disc.html>`_ you'll know why I had some trouble with getting Rich Presence to work on my Wineskin. I don't really have time to look into this further, but you can try these instructions and see if they work for you:

.. warning::

    These instructions are for **macOS 10.14 and earlier**. If you are using macOS 10.15 or later, these instructions will not work and you need to use `this one instead <discord-10-15.html>`_.

1. Download `0e4ef622 <https://osu.ppy.sh/users/5405852>`_'s `Wine Discord IPC Bridge <https://github.com/0e4ef622/wine-discord-ipc-bridge>`_. 

**Download (GitHub mirror):** https://github.com/0e4ef622/wine-discord-ipc-bridge/raw/master/winediscordipcbridge.exe

2. Drag and drop the bridge into the same directory as ``osu!.exe``

    - Locate where ``osu!.app`` (your Wineskin) is installed
    - Right click on it and select ``Show Package Contents``
    - You should now see three files/folders: ``Contents``, ``drive_c`` and ``Wineskin``. Click ``drive_c``.
    - From here, click ``osu!``.

3. Rename it ``bridge.exe`` (just to keep things simple)
4. Open TextEdit (it should be in your Applications folder)
5. Create a new text file. Inside it, copy and paste the following:

.. code-block:: bat

    start C:\osu!\osu!.exe
    start C:\osu!\bridge.exe

6. Save it as ``execute.bat`` and place it inside of the ``osu!`` folder that we mentioned above. It should be stored in the same directory as ``osu!.exe`` and ``bridge.exe``.
7. Open your Wineskin options

    - Locate where ``osu!.app`` (your Wineskin) is installed
    - Right click on it and select ``Show Package Contents``
    - You should now see three files/folders: ``Contents``, ``drive_c`` and ``Wineskin``. Click ``Wineskin``.

8. A window like the one below should pop up. Click **Advanced**

.. image:: ../assets/wineskin.png

7. A window like the one below should pop up. 

.. image:: ../assets/wineskin-windows-exe.png

In the **Windows EXE** text box, copy and paste the following:

.. code-block::

    C:\osu!\execute.bat

.. tip::

    Alternatively, you could just click the **Browse..** button and navigate to where you saved your ``execute.bat`` file.

****

****************************************
If that didn't work
****************************************

In theory, this should enable you to connect osu! under Wine, to the Discord client on your Mac, but as previously mentioned, I wasn't able to get it to work.

You can read more about this program on it's `GitHub page <https://github.com/0e4ef622/wine-discord-ipc-bridge>`_ which contains information on how the bridge works and how to use it.

.. note::

    Do you have anything to add? See our `Contributing <../about/contributing.html>`_ to see how you can contribute to these docs.