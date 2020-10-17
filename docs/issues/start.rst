#############################################################
osu! runs perfectly, but it has some trouble when starting up
#############################################################

.. rst-class:: wineskin-version
    
    | This article is applicable to the following wrappers:
    | • `Technocoder <https://osu.ppy.sh/users/10338558>`_'s `Experimental Wineskin with macOS Catalina 10.15 support <https://osu.ppy.sh/community/forums/posts/7367239>`_

****

****************************************
Behaviour
****************************************

osu! has some trouble starting up, for example:
- `it updates each time you open it <https://osu.ppy.sh/community/forums/topics/1036678?start=7540911>`_
- `you need to launch the game twice, since the first time always crashes <https://osu.ppy.sh/community/forums/topics/1036678?start=7540911>`_

****

****************************************
Cause
****************************************

osu!'s startup sequence causes it to perform actions on startup that shouldn't happen, like it might occassionally crash or it does something annoying (usually because it's not entirely friendly with Wine).

****

****************************************
Resolution
****************************************

You can bypass the startup sequence entirely. Technocoder found a `workaround <https://osu.ppy.sh/community/forums/topics/682197?start=7443024>`_ that will hopefully mitigate your startup troubles:

.. warning::

	**This section only applies to users using the** `experimental macOS Catalina Wineskin <https://osu.ppy.sh/community/forums/posts/7367239>`_.

	You are recommended to use the `latest macOS Catalina Wineskin <https://osu.ppy.sh/community/forums/posts/7560723>`_ instead.

::

    1. Open the ``osu!`` folder (Right click osu! > Show Package Contents > drive_c > osu!)
    2. Create a new file in this location named ``execute.bat`` (with .bat as the extension)
    3. Type in: ``start C:\osu!\osu!.exe -nosplash``
    4. Save ``execute.bat``
    5. Open **Wineskin** (Right click osu! > Show Package Contents > Wineskin)
    6. Click **Advanced**
    7. Change the **Windows EXE** field to: ``"C:\osu!\execute.bat"`` (including the outer quotes)
    8. Close Wineskin

****

****************************************
If that didn't work
****************************************

`This method isn't fullproof <https://osu.ppy.sh/community/forums/topics/682197?start=7443024>`_, but it's certainly the best one currently available. If you're still having trouble, visit the `Troubleshooting <troubleshooting.html>`_ page and let us know on the `forums <https://osu.ppy.sh/community/forums/5>`_.
