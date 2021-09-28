https://github.com/Techno-coder/osu-macOS-Agent/commit/f722c9d6e0a933ed14c65025c182b8068407890f

####################################################
osu!macOS Agent crashes on startup
####################################################

.. rst-class:: wineskin-version
    
    | This article is applicable to:
    | • `Technocoder <https://osu.ppy.sh/users/10338558>`_'s `osu!macOS Agent <https://osu.ppy.sh/community/forums/topics/1036678>`_

****

****************************************
Behaviour
****************************************

osu!macOS Agent crashes when you attempt to start it. 

To diagnose the issue, move osu!macOS Agent to the Desktop and run the following command in Terminal.

.. code-block::

    ~/Desktop/osu\!macOS\ Agent.app/Contents/MacOS/osu\!macOS\ Agent

Versions of osu!macOS Agent affected by this bug will receive the following output.

.. code-block::

    zsh: killed ~/Desktop/osu!macOS\ Agent.app/Contents/MacOS/osu!macOS\ Agent

****

****************************************
Cause
****************************************

Older versions of osu!macOS Agent may crash on newer versions of macOS due to a `build environment variable <https://github.com/Techno-coder/osu-macOS-Agent/commit/f722c9d6e0a933ed14c65025c182b8068407890f>`_.

****

****************************************
Resolution
****************************************

Please download the latest version of osu!macOS Agent. This issue was fixed on 27 September 2021.

- **osu! forum thread:** `community/forums/topics/1036678 <https://osu.ppy.sh/community/forums/topics/1036678?n=1>`_

****

****************************************
If that didn't work
****************************************

Please make a reply on `this osu! forum thread <https://osu.ppy.sh/community/forums/topics/1036678>`_ with a detailed explanation of your issue.