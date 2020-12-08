##########################################################################################
Wineskin.app doesn't open, even if osu! does
##########################################################################################

.. rst-class:: wineskin-version
    
    | This article is applicable to the following wrappers:
    | • `slc <https://osu.ppy.sh/users/7978076>`_'s `Wineskin for macOS 10.14 Mojave and earlier <https://osu.ppy.sh/community/forums/topics/682197?start=6919344>`_
    | • `Technocoder <https://osu.ppy.sh/users/10338558>`_'s `Wineskin with macOS Catalina 10.15 support <https://osu.ppy.sh/community/forums/topics/1106057>`_
    | • `Technocoder <https://osu.ppy.sh/users/10338558>`_'s `unofficial Wineskin for macOS 10.14 Mojave and earlier <https://osu.ppy.sh/community/forums/topics/682197>`_

****

****************************************
Behaviour
****************************************

When attempting to open the Wineskin.app application located inside your osu! wrapper, you receive a warning that reads the following message:

    Error while writting file: The folder “exec2088858072.bat” doesn’t exist.

****

****************************************
Cause
****************************************

There's a number of issues that could be at play here:

- You haven't ran the repair tool on your osu! wrapper yet
- You have a corrupted installation
- You used the in-built Archive Utility instead of The Unarchiver which carries some known issues
- Your anti-virus is removing files from your osu! wrapper without your knowledge

****

****************************************
Resolution
****************************************

1. If you haven't already, run the osu!macOS Agent **repair tool** on your osu! wrapper by following these instructions:

    - Open osu!macOS Agent
    - Go to the **Troubleshoot** tab
    - Click **Scan**
    - Click **Repair**

You still need to do this step on your osu! wrapper, even if osu! itself runs fine.

2. Make sure your antivirus isn't removing anything. Guidelines on how to do this are available `here <malware.html#resolution>`_.
3. Use `The Unarchiver <https://theunarchiver.com/>`_ instead of your in-built Archive Utility.

If you tried all of that and Wineskin.app still won't open, you can try replacing Wineskin.app with a known working version.

1. Download the Wineskin.app replacement from https://minhaskamal.github.io/DownGit/#/home?url=https://github.com/aidswidjaja/osu-mac/tree/main/src/wineskin or https://drive.google.com/drive/folders/1Gz5Y0M4WoMxTTwb5aHUccebO5AlVm3SN?usp=sharing

    - If using Google Drive, click **DOWNLOAD ALL** in the top-right corner of the screen

2. The file will download this as a zip file. Extract the zip file until you just have the Wineskin.app file
3. Inside **osu!.app** (Right click > Show Package Contents) locate **Wineskin.app** - make a backup of it (you can just rename it to say something like Wineskin.app.backup if you want)
4. Replace the old **Wineskin.app** with the replacement version you downloaded from Google Drive

Try and open it and see if everything works out.

.. warning::

    This is an experimental hotfix. Make sure you make a backup of your Wineskin.app before replacing it with this replacement version.

****

****************************************
If that didn't work
****************************************

There could be something else going on here, and performing `basic troubleshooting <troubleshooting.html>`_ should help you get to the bottom of it.

If you're still not sure what's going on here, copy any osu! crash logs and `generate a report with osu!macOS Agent <troubleshooting.html#generating-a-report-with-osu-macos-agent>`_, then let us know on the forums with what we can help.

*****

****************************************
Related links
****************************************

- https://osu.ppy.sh/community/forums/posts/7793479