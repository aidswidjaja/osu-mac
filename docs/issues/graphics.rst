#############################################
osu! was unable to obtain a graphics context
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

osu! crashes on startup, displaying an error message that says *osu! was unable to obtain a graphics context*.

.. image:: ../assets/graphics-context.png
    :alt: Pop-up dialog: osu! was unable to obtain a graphics context.

****

****************************************
Cause
****************************************

This usually occurs because a user enabled Compatibility Mode in osu! settings, or changed to a screen resolution that Wine couldn't handle.

Wine doesn't support Compatibility Mode (aka osu!fallback) since it relies on OpenGL, whereas standard osu! uses DirectX. If you look in the logs, you may notice that osu! will be unable to find an OpenGL file.

.. note::

    If you need to use Compatibility Mode, you can try switching to the X11 driver, though in our own testing this made no observeable difference.

****

****************************************
Resolution
****************************************

1. Find your user profile/configuration file.

    - Locate where ``osu!.app`` (your Wineskin) is installed
    - Right click on it and select ``Show Package Contents``
    - You should now see three files/folders: ``Contents``, ``drive_c`` and ``Wineskin``. Click ``drive_c``.
    - From here, click ``osu!``.
    - From here, locate ``osu!.yourcomputername.cfg`` and open this file in a plain text editor such as TextEdit.

For example, my configuration file is ``osu!.Adrian.cfg`` and it looks like this:

.. image:: ../assets/osu-config.png
    :alt: osu! user configuration file.

.. tip::

    The default name for this file is usually ``osu!.Apple.cfg``

.. note::

    Don't get confused with ``osu!.cfg`` which is a completely different and much smaller configuration file.

.. danger::

    Heed the warning and **don't share this configuration file with anyone else, not even us.** It contains hashed versions of your passwords.

2. You'll need to either delete or change a number of screen resolution options if you don't know which is causing osu! to crash. If you know what option is breaking osu!, then you only need to modify/delete that specific option, as listed below.

****

Compatibility Mode
=======================================

If you enabled Compatibility Mode and now osu! won't start, find the ``CompatibilityContext`` option.

.. tip::

    Use ``Command + F`` in TextEdit to quickly search for ``CompatibilityContext``.

.. note::

	`osu!macOS Agent <https://osu.ppy.sh/community/forums/topics/1036678>`_ will automatically disable Compatibly Mode as part of its troubleshooting steps.

If you *did* enable it, it would look like this:

.. code-block:: 
    
    CompatibilityContext = 1

Change this to:

.. code-block:: 
    
    CompatibilityContext = 0

Then, start osu!

If you can't find ``CompatibilityContext``
------------------------------------------

Add the following line to the bottom of ``osu!.yourcomputername.cfg``:

.. code-block:: 
    
    CompatibilityContext = 0

Then, start osu!

****

Screen Resolution
=======================================

If you changed the screen resolution to something a bit weird, find these options:

- ``Height``
- ``Width``
- ``HeightFullscreen``
- ``WidthFullscreen``

.. tip::

    Use ``Command + F`` in TextEdit to quickly search for these options.

Then, change the values accordingly to your last known previous settings, or to the recommended values as shown below. You can also delete them to have osu! initialise everything for you again.

Preferably:

- ``Height`` and ``Width`` should be Wine's specified screen resolution (or otherwise, a standard screen resolution like ``1920x1080``)
- ``HeightFullscreen`` and ``WidthFullscreen`` should be your computer's effective/scaled screen resolution.

.. raw:: html

    <details>
    <summary><h4 style="display: inline;">Find Wine's specified screen resolution</h4></summary>
    <br>

If you're using Virtual Desktop on the X11 driver and need to modify ``Height`` and ``Width``:

    1. Locate where ``osu!.app`` (your Wineskin) is installed
    2. Right click on it and select ``Show Package Contents``
    3. You should now see three files/folders: ``Contents``, ``drive_c`` and ``Wineskin``. Click ``Wineskin``.
    4. Click **Set Screen Options**
    5. Locate the Screen Resolution dropdown as shown below - what it is set to is Wine's specified screen resolution:

.. image:: ../assets/osu-screen-res.png
    :alt: osu! screen resolution dropdown menu, within the Screen Options menu in Wineskin.

In this example it is ``1920x1080``. Therefore, ``Width = 1920`` and ``Height = 1080``. 

.. raw:: html

    </details>
    <br>

.. raw:: html

    <details>
    <summary><h4 style="display: inline;">Find your fullscreen resolution</h4></summary>
    <br><br>

.. raw:: html

        <!-- I know this is terrible js but this script will never be edited again so it doesn't matter -->
        <script type="text/javascript">
	        var width = window.screen.width;
	        var height = window.screen.height;
        </script>
    <p onload="screenres()">
    To find osu!'s fullscreen resolution, you need to know your <strong>current scaled resolution for the monitor you're playing osu! on.</strong><br><br>Your scaled screen resolution on this monitor is
		<strong>
		<script type="text/javascript">
			document.write(width)
		</script>
			x
		<script type="text/javascript">
			document.write(height)
		</script>
		</strong>
		where:<br>
		<ul>
		<li>Width = <strong>
		<script type="text/javascript">
			document.write(width)
		</script></li></strong>
		<li>Height = <strong>
		<script type="text/javascript">
			document.write(height)
		</script></li></strong>
		</ul>
    </p>
    <br>

Now, replace the corresponding Height and Width values in ``osu!.yourcomputername.cfg`` with those displayed above.

****

****************************************
If that didn't work
****************************************

There could be something else going on here, and performing `basic troubleshooting <troubleshooting.html>`_ should help you get to the bottom of it.

If you're not sure what's going on here, copy any osu! crash logs as well as `generating a report with osu!macOS Agent <troubleshooting.html#generating-a-report-with-osu-macos-agent>`_, and let us know on the forums.

.. note::

   **Random side note that may or may not be useful to you:** (i didn't have anywhere else to put it)
    
    Don't use a .NET version that's too new (`.NET 4.0 is the highest slc's Wineskin will support <https://osu.ppy.sh/community/forums/topics/682197?start=6919370>`_) 