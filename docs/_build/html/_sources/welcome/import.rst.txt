#############################
Importing beatmaps and skins
#############################

.. rst-class:: wineskin-version
    
    | This article is applicable to the following wrappers:
    | • `slc <https://osu.ppy.sh/users/7978076>`_'s `Wineskin for macOS 10.14 Mojave and earlier <https://osu.ppy.sh/community/forums/topics/682197?start=6919344>`_
    | • `Technocoder <https://osu.ppy.sh/users/10338558>`_'s `Wineskin with macOS Catalina 10.15 support <https://osu.ppy.sh/community/forums/topics/1106057>`_
    | • `Technocoder <https://osu.ppy.sh/users/10338558>`_'s `unofficial Wineskin for macOS 10.14 Mojave and earlier <https://osu.ppy.sh/community/forums/topics/682197>`_

****

.. note::

    If you're new to osu! and don't know how all this beatmap and skin stuff work:

    - `Adding beatmapsets on osu! knowledge base <https://osu.ppy.sh/help/wiki/Installation#adding-beatmapsets>`_
    - `Skinning FAQ on osu! knowledge base <https://osu.ppy.sh/help/wiki/Skinning/FAQ>`_

.. note::

    osu!macOS Agent can automatically move beatmaps and skins from your Downloads folder. Just make sure to enable the checkboxes inside osu!macOS Agent settings.

***************************************
Importing beatmaps
***************************************

Importing beatmaps into osu! is quite easy, but you can't exactly drag and drop files into osu! like you can on Windows.

To import a beatmap into osu!, follow the following instructions:

1. Find your ``Songs`` directory

    - Locate where ``osu!.app`` (your Wineskin) is installed
    - Right click on it and select ``Show Package Contents``
    - You should now see three files/folders: ``Contents``, ``drive_c`` and ``Wineskin``. Click ``drive_c``.
    - From here, click ``osu!``.
    - From here, locate ``Songs``

.. tip::

    You can create an alias or shortcut pointed to your Songs directory, in somewhere handy like your Desktop. Then you can quickly access the folder whenever you want to drop beatmaps in.

    To create an alias, click on the ``Songs`` folder, then go to **File** > **Make Alias** - then put this alias somewhere where you can easly access it.

2. Find a beatmap on `osu.ppy.sh <https://osu.ppy.sh/beatmapsets>`_. For this example, we'll use `Ryofuka's crossing field <https://osu.ppy.sh/beatmapsets/68500>`_.
3. Just like you would normally, click the **Download** button to download the beatmap.
4. You should now have a ``.osz`` file in your Downloads file. Drag and drop this file into the ``Songs`` directory we located before.

.. image:: ../assets/osu-beatmap.gif
    :alt: Dragging and dropping a beatmap into the Songs directory.

.. tip::

    To avoid potential import issues, remove any non-alphabetical characters (numbers and hyphens are fine)

.. note::

    Yes, my beatmap folder is very empty (but yours won't be! Unless it is, of course..)

5. If you don't have osu! open already, open it now. Then in-game, press ``F5``

.. note::

    Unless you have function keys enabled, you may need to press the ``Fn`` button at the same time.

    .. raw:: html

        <br>
        <details>
        <summary><h4 style="display: inline;">Use F1, F2, etc. as standard function keys</h4></summary>
        <br>


    1. Locate where ``osu!.app`` is installed
    2. Right click on it and select **Show Package Contents**
    3. You should now see three files/folders: ``Contents``, ``drive_c`` and ``Wineskin``. Click ``Wineskin``
    4. A window like the one below should pop up. Click **Advanced**

    .. image:: ../assets/wineskin.png
        :alt: Wineskin settings.

    5. Click the **Options** tab
    6. Select **Use F1, F2, etc. as standard function keys**

    .. raw:: html

        </details>
        <br>

.. tip::

    You can do all of this while leaving osu! running open in the background!

****

***************************************
Importing skins
***************************************

Importing skins is largely the same process, except instead of the ``Songs`` directory, use the ``Skins`` directory, and to reload osu! use ``Ctrl-Alt-Shift-S`` instead of ``F5``.

You can then select your skin as normal from the osu! in-game settings menu.

.. note::

    Treat this as if you were working on a Windows system. If the skin is compressed, you'll probably need to uncompress it. You can use something like `The Unarchiver <https://theunarchiver.com/>`_ or even your in-built Archive Utility to do this (though Archive Utility might not have so much fun with ``.rar`` or ``.7zip`` files)

    See the `osu! knowledge base <https://osu.ppy.sh/help/wiki/Installation#adding-skins>`_ for more info.

