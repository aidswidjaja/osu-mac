#######################################################################
Installing osu!
#######################################################################

This guide will walk you through how to install `Technocoder <https://osu.ppy.sh/users/7978076>`_'s latest Wineskin, which will let you play osu! on macOS.

.. raw:: html

    <details>
    <summary><h4 style="display: inline;">Using macOS Catalina 10.15.0 to 10.15.4?</h4></summary>
    <br>

.. warning::

    **This section only applies to users who are using macOS Catalina 10.15.0 to 10.15.4**

    If you don't know what specific macOS version you're using, `use this Apple support article <https://support.apple.com/en-au/HT201260>`_ to learn how to find out.

.. danger::

    Although your computer will not be harmed from disabling SIP, it may compromise the integrity of your computer's security.

    Please be informed about the risks of disabling SIP. Consider updating macOS instead. We are not responsible if something goes wrong.

    You can learn more about SIP in this `Apple support article <https://support.apple.com/en-us/HT204899>`_.

Apple recently introduced changes to how macOS works. New Macs come with **System Integrity Protection (SIP)**.

Therefore, in order to run osu!mac on macOS Catalina **10.15.0 to 10.15.4** you need to disable SIP.
These instructions are quoted from the `Apple Developer documentation <https://developer.apple.com/documentation/security/disabling_and_enabling_system_integrity_protection>`_.

To disable SIP, do the following:

    1. Restart your computer in `Recovery mode <https://support.apple.com/en-gb/HT201314>`_.

        - Turn on your Mac and immediately press and hold these two keys: Command (⌘) and R. 
        - Release the keys when you see an Apple logo, spinning globe or other startup screen.
        - You may be prompted to enter a password, such as a firmware password or the password of a user who is an administrator of this Mac. Enter the requested password to continue.

    2. Launch **Terminal** from the **Utilities** menu. It should be in the menu bar at the top of your screen.
    3. Run the command ``csrutil disable``.
    4. Restart your computer. You can do so from the top menu bar (just like you would normally)

Once you have SIP disabled, you can begin to install osu!.

.. raw:: html

    </details>
    <br>

****

****************************************
Step 1: Download the Wineskin
****************************************

1. Download Technocoder's **Rosetta Wineskin** from the `osu! forums <https://osu.ppy.sh/community/forums/posts/7560723>`_
2. Extract the ``.zip`` file
3. Move the extracted folder outside of your Downloads folder (to avoid `sandboxing <https://en.wikipedia.org/wiki/Sandbox_(computer_security)>`_)
4. Download Technocoder's osu!macOS Agent program from the `osu! forums <https://osu.ppy.sh/community/forums/topics/1036678>`_


.. note::

    The **Rosetta Wineskin** is the best Wineskin for playing osu! on macOS, and works on all systems and most macOS versions, including Intel and Apple Silicon computers.

    You can learn more about different Wineskins available at `Choosing a Wineskin <../install/choose.html>`_


.. note::

    Downloading `Technocoder <https://osu.ppy.sh/users/10338558>`_'s osu!macOS Agent program is **recommended but optional**. It's a great tool that every macOS Wineskin player should have. However, alternative instructions using the Terminal are provided for those who are comfortable with digging deeper.


****

****************************************
Step 2: Repair the Wineskin
****************************************

.. image:: ../assets/osu-broken.png
    :alt: 'osu!.app is damaged and can't be opened. You should move it to the Bin.

If you try to open the Wineskin immediately, macOS might say that it's broken. If it does, let's fix that.

1. Open osu!macOS Agent
2. Click the **Troubleshoot** tab
3. Click **Scan**
4. Once the scan is complete, click **Repair**

If it was successful, you should see a **Fixed** indicator next to ``Quarantine attribute is present`` in the log.

.. image:: ../assets/osu-agent-log.png
    :alt: 'osu!.app is damaged and can't be opened. You should move it to the Bin.'

.. note::

    If you are using a Mac with Apple Silicon, then you might be prompted to install Rosetta (if you haven't already). Just go ahead and click **Install**.

    .. image:: ../assets/rosetta.jpg
        :alt: 'To open "App", you need to install Rosetta. Do you want to install it now?'

.. raw:: html

    <details>
    <summary><h4 style="display: inline;">Alternative option: Using the Terminal</h4></summary>
    <br>

On the bleeding edge? You can also use the Terminal to repair your Wineskin.

1. Open Terminal. It should be in your ``Applications/Utilities`` folder.
2. Type the following command.

.. code-block:: bash

    sudo xattr -rd com.apple.quarantine "~/path/to/my/osu\!.app"

where ``~/path/to/my/osu\!.app`` is the filepath to your osu! install. 

.. note::
    
    For tips on using the terminal, `go here <../issues/using-terminal.html>`_.

.. warning::

    Using the terminal with ``sudo`` will allow you to perform commands as admin. Improper use of the terminal can negatively affect your computer. Please don't type something you don't completely understand - ask us a question instead!

.. raw:: html

    </details>
    <br>

****

****************************************
Step 3: Updating osu!
****************************************

If osu! is stuck in an update loop when you first open it, try these steps. Otherwise, feel free to skip it.

.. tip::

    If you ever have trouble closing osu! once it's stuck in an update loop, see `Common issues: osu! won't close <../issues/wontclose.html>`_.

1. Open osu!macOS Agent
2. Click the **Other** tab
3. Click **Update osu!**

.. image:: ../assets/osu-agent-update.png

This will download the latest executable from the osu! servers and replace the existing ``osu!.exe`` inside your Wineskin wrapper. 

.. raw:: html

    <details>
    <summary><h4 style="display: inline;">Alternative option: Manually installing the latest version of osu!</h4></summary>
    <br>

1. Download ``osu.exe`` from `osu.ppy.sh/home/download <https://osu.ppy.sh/home/download>`_
2. Locate where ``osu!.app`` (your Wineskin) is installed
3. Right click on it and select ``Show Package Contents``
4. You should now see three files/folders: ``Contents``, ``drive_c`` and ``Wineskin``. Click ``drive_c``.
5. From here, click ``osu!``.
6. From here, locate ``osu!.exe`` and replace this file with the updated version that you just downloaded - make sure you keep the filename the same

.. raw:: html

    </details>
    <br>

****

****************************************
Step 4: Run osu!
****************************************

Now everything should be good to go! Open ``osu!.app`` and try it out!

- Did things not go to plan? Check out `Common issues <../issues/index.html>`_ for fixes to commonly-experienced problems
- Ask a question on the `osu! forum thread <https://osu.ppy.sh/community/forums/posts/7560723>`_ if you need help
- If everything turned out fine, check out `Welcome to osu! <../welcome/index.html>`_ to improve your osu! experience before you start clicking circles
- Learn how to `import beatmaps and skins <../welcome/import.html>`_
- `Transfer your data <../welcome/transfer.html>`_ from previous versions of osu!

