#############################################
Performance Troubleshooting
#############################################

.. rst-class:: wineskin-version
    
    | This article is applicable to the following wrappers:
    | • `slc <https://osu.ppy.sh/users/7978076>`_'s `Wineskin for macOS 10.14 Mojave and earlier <https://osu.ppy.sh/community/forums/topics/682197?start=6919344>`_
    | • `Technocoder <https://osu.ppy.sh/users/10338558>`_'s `Wineskin with macOS Catalina 10.15 support <https://osu.ppy.sh/community/forums/topics/1106057>`_
    | • `Technocoder <https://osu.ppy.sh/users/10338558>`_'s `unofficial Wineskin for macOS 10.14 Mojave and earlier <https://osu.ppy.sh/community/forums/topics/682197>`_

Performance issues are often difficult to isolate, and fixes and problems will vary for various users. If you are experiencing performance or stability issues, try following this guide step by step.

.. note::

    Close all programs when troubleshooting performance issues, as they often interfere with the running game.

.. note::

    Using a high polling rate is known to cause performance issues on osu!. For information, see `Performance issues with high-polling rate mice <../issues/mouse.html>`_

****

****************************************
Modify in-game settings
****************************************

Try adjusting your in-game osu! settings, using the default skin. Try experimenting with lower graphics settings.

.. note::

    You can monitor latency and framerate with the FPS counter, which can be enabled under Graphics in the in-game options.

========================================
Using MyPcSucks
========================================

You can modify your ``osu!.User.cfg`` file and insert ``MyPcSucks=0`` to the bottom of the file, which will automatically optimise osu! for performance.

1. Right click on osu!
2. Click **Show Package Contents**
3. Navigate to ``drive_c/osu!/osu!.User.cfg`` where ``User`` is the name of your current user account name
4. Open in TextEdit
5. At the bottom of the file, add ``MyPcSucks = 0``

.. danger::

    Never share this file with anyone, as it contains your (hashed) username and password.

****

****************************************
Try a clean or alternative wrapper
****************************************

- Sometimes, you can isolate whether a performance-heavy skin or toggle performance setting by simply downloading again. 
- Or, you can see if you reach better performance using an alternative wrapper (like the Intel or Catalina wrapper).

If you'd like to try re-downloading, just follow the steps in the `installation guide <../install/install.html>`_ again.

****

****************************************
Set priority and affinity
****************************************

We recommend osu! runs on all available cores and is set to a priority of High. To ensure this, follow the below steps to use the WINE Task Manager to set priority and affinity.

.. note::

    By defaut, osu! runs at a priority of High.

1. Make sure osu! is currently running
2. Locate your osu! installation
3. Right click on osu!, then select **Show Package Contents**
4. Open **Wineskin** > **Advanced** > **Tools**
5. Click on **Task Manager (taskmgr)** - it may take some time before the window opens
6. Find osu!.exe in the list that appears.

	- To set priority, right click, then select **Set priority**.
    - By default, osu! is on High. Ensure the option is selected to High.

7. To set affinity, right click, then select **Set affinity...**
8. In the window that appears, select the number of cores you would like to use

    - **More cores** = greater performance for gamplay (recommended)
    - **Less cores** = greater stability for better troubleshooting, especially if there are issues with multithreading
    - Choosing specific cores may positively or negatively impact your game's performance or stability

.. note::

    For information on what priority and affinity is, see this `Stack Exchange answer <https://superuser.com/a/181947>`_.

****

****************************************
Reinstall .NET
****************************************

Reinstalling .NET may provide better stability. For reinstallation steps, visit the `.NET runtime issues <../issues/dotnet.html>`_ page.

****

****************************************
Ask for help
****************************************

There can often be many reasons for why users suffer from performance issues, such as...

- a faulty update introduced into osu!
- incapable system specifications
- software or hardware configuration changes

It can be really difficult to isolate performance issues, but we're happy to help. If *none* of these steps worked for you, then you should run through the steps at `Troubleshooting Basics <../issues/troubleshooting.html>`_ and contact us in our `osu! community thread <https://osu.ppy.sh/community/forums/posts/7560723>`_.