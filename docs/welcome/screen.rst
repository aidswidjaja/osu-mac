########################################
Setting up your screen options
########################################

.. rst-class:: wineskin-version
    
    | This article is applicable to the following wrappers:
    | • slc's `Wineskin for macOS 10.14 Mojave and earlier <https://osu.ppy.sh/community/forums/topics/682197?start=6919344>`_

This section will help you adjust your screen options to your liking. Even if you're happy with the default settings, it's a good idea to familiarise yourself with the other alternatives available.

Your osu! wrapper by slc comes with two graphics drivers:

- **Mac driver** - a modern window system that has better performance than its X11 counterpart
- **X11 driver** - the legacy window system that features better compatibility and customisation

By default, slc's Wineskin wrapper uses the **Mac driver**. To configure this, you will need to access the Wineskin settings by performing the following:

.. note::

    If you get an error saying "Wineskin cannot be opened because it is from an unidentified developer", right click on ``Wineskin`` and click Open, then proceed through the warning dialog.

1. Locate where ``osu!.app`` is installed
2. Right click on it and select **Show Package Contents**
3. You should now see three files/folders: ``Contents``, ``drive_c`` and ``Wineskin``. Click ``Wineskin``
4. A window like the one below should pop up. Click **Set Screen Options**

.. image:: ../assets/wineskin.png
    :alt: Wineskin settings.

Now, you should now be able to edit your **Screen Options**.

.. image:: ../assets/screen-options.png
    :alt: Wineskin screen options.

From here, you'll be able to choose between the Mac driver or the X11 driver, as well as modify a number of other options. 

.. important:: 

    If you intend on using the X11 driver, you should install `XQuartz 2.7.11 <https://www.xquartz.org/index.html>`_ or higher.

- If you want to play at near-native performance, choose the **Mac driver**. You will lose configurability in exchange for performance, including difficulties in playing in non-fullscreen display modes.

    - When you first play with the Mac driver you'll be unable to access any other applications or system UI elements (and it will blank out your second monitor too) - something that can be worked around but not entirely perfected. You can view the workaround `here <../issues/dualmonitor.html>`_.

- If you need legacy support, would like to play osu! in a window, or need the extra customisation, choose the **X11 driver**.

    - Need to make configuration changes? Change the **Default Settings** radio buttons to **Override**. You'll then be able to play around with your configuration to suit your preferences.
    - Using the X11 driver? You can also try enabling Direct3D Boost - some users have reported better graphics with this turned on.

To save your changes, click the red circular close icon in the top-left corner of the window, then click **Quit** in the Wineskin window.

.. raw:: html

    <details>
    <summary>
    <h4 style="display: inline;">Detect your screen's current resolution</h4></summary>
        <!-- I know this is terrible js but this script will never be edited again so it doesn't matter -->
        <script type="text/javascript">
	        var width = window.screen.width;
	        var height = window.screen.height;
        </script>
        <br>
    <p onload="screenres()">Your scaled screen resolution on this monitor is
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
    </details>
    <br>

.. note::

    **Case studies:**

    I like to play osu! in a window, so I'm using the **X11 driver** with Virtual Desktop enabled, Windowed mode, with a standard resolution of ``1920x1080``. 

    If I wanted to play osu! fullscreen, I'd choose the **Mac driver**, and since I have a Retina MacBook Pro, I would enable the Retina display option.

.. danger::

    Turning on Compatibility Mode in osu! may crash your game.
    
    If you turned on Compatibility Mode and now osu! crashes on startup, see `Common issues: osu! was unable to obtain a graphics context. <../issues/graphics.html>`_.

.. warning::

    It is generally advised not to modify the osu! in-game resolution since it will usually automatically adjust to what you have set in Wine (or if you need to adjust it, set it to osu!'s detected native resolution). Modifying otherwise may cause your osu! to crash.

    .. image:: ../assets/graphics-context.png
        :alt: osu! was unable to obtain a graphics context.
        :height: 200px

    |
    | If your osu! crashes after a graphics settings modification in-game, see `Common issues: osu! was unable to obtain a graphics context. <../issues/graphics.html>`_.

.. image source: https://www.reddit.com/r/osugame/comments/cfv3td/compatibility_mode_crashes_osu_on_mac/