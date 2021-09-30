#############################################################
Startup issues
#############################################################

.. rst-class:: wineskin-version
    
    | This article is applicable to the following wrappers:
    | • `Technocoder <https://osu.ppy.sh/users/10338558>`_'s `Experimental Wineskin with macOS Catalina 10.15 support <https://osu.ppy.sh/community/forums/posts/7367239>`_

****

****************************************
Behaviour
****************************************

osu! has some trouble starting up, for example:

- `It updates each time you open it <https://osu.ppy.sh/community/forums/topics/1036678?start=7540911>`_
- `You need to launch the game twice, since the first time always crashes <https://osu.ppy.sh/community/forums/topics/1036678?start=7540911>`_
- `Startup will take 1-2 minutes <https://osu.ppy.sh/community/forums/posts/8162613>`_

or the game will refuse to start up at all.

****

****************************************
Cause
****************************************

There could be a large number of factors causing this issue. The best way to understand what's going on is to diagnose it through basic `Troubleshooting Steps <troubleshooting.html>`_, especially an osu!macOS Agent Report and Wineskin Test Run.

We are currently aware of a number of known issues that may be affecting your ability to start the game consistently, so let us know about your issues and troubleshooting steps on the `osu! forum thread <https://osu.ppy.sh/community/forums/topics/1106057>`_.

****

****************************************
Resolution
****************************************

Firstly, ensure that your Wineskin isn't corrupt by reinstalling it, and extracting the .zip file with `The Unarchiver <https://theunarchiver.com/>`_. You should also ensure that no anti-virus software is intefering with osu!, and try downloading a different Wineskin if one isn't working. Kill any osu! or wine related processes in Activity Monitor in case they are hanging over after you shut down osu!.

========================================
.NET runtime issues
========================================

Our `.NET runtime issues <dotnet.html>`_ troubleshooting page contains a number of steps you can attempt if you're explicitly having trouble with the .NET runtime behind osu!

========================================
Bypassing the startup sequence
========================================

.. warning::

	**This section only applies to users using the** `experimental macOS Catalina Wineskin <https://osu.ppy.sh/community/forums/posts/7367239>`_.

	You are recommended to use the `latest Wineskin with Apple Silicon support <https://osu.ppy.sh/community/forums/posts/7560723>`_ instead.

In older Wineskins, you can bypass the startup sequence entirely. Technocoder found a `workaround <https://osu.ppy.sh/community/forums/topics/682197?start=7443024>`_ that will hopefully mitigate your startup troubles:

1. Open the ``osu!`` folder (Right click osu! > Show Package Contents > drive_c > osu!)
2. Create a new file in this location named ``execute.bat`` (with .bat as the extension)
3. Type in: ``start C:\osu!\osu!.exe -nosplash``
4. Save ``execute.bat``
5. Open **Wineskin** (Right click osu! > Show Package Contents > Wineskin)
6. Click **Advanced**
7. Change the **Windows EXE** field to: ``"C:\osu!\execute.bat"`` (including the outer quotes)
8. Close Wineskin

In newer Wineskins, this feature is already built in.

****

****************************************
If that didn't work
****************************************

`This method isn't fullproof <https://osu.ppy.sh/community/forums/topics/682197?start=7443024>`_, but it's certainly the best one currently available. If you're still having trouble, visit the `Troubleshooting <troubleshooting.html>`_ page and let us know on the `forums <https://osu.ppy.sh/community/forums/5>`_.
