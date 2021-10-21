.. osu!mac documentation master file, created by
   sphinx-quickstart on Fri Oct  2 16:03:45 2020.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.


.. rst-class:: index-align-center h1

#######################################
osu!mac
#######################################
   
.. rst-class:: index-align-center h3

************************************************************
let's get you set up with osu! on your macOS-powered device!
************************************************************

.. image:: assets/osu-mac.gif
   :alt: osu! running on macOS 10.14 Mojave.

****

.. note::

	**Thursday 21 October:**
	
	Due to a termination of service from MEGA, download links for some Wineskins are unavailable, while others have changed.
	
	- Download links for the [b]Rosetta[/b] Wineskin are currently available only through Google Drive
	- Download links for Technocoder's Catalina and Intel Wineskins are **currently not available**
	- osu!macOS Agent can still be downloaded through GitHub but not MEGA
	
	**The Rosetta Wineskin will work on all platforms and OS versions**, including Apple Silicon and x86.
	
	Technocoder is continuing to work with MEGA to resolve this issue, and we hope this issue is resolved within the next 48 hours. For new download links and further updates, please visit the `macOS Wineskin thread <https://osu.ppy.sh/community/forums/topics/1106057>`_. 

Getting started
=======================================

These community-developed osu! `Wineskins <http://wineskin.urgesoftware.com/tiki-index.php>`_ are the best way to play osu-stable on your Mac.

Not sure which wrapper you should get? Check out `Which Wineskin should I get? <install/choose.html>`_

- `Get Technocoder's osu! Wineskin with support for Apple Silicon running under Rosetta 2 <install/silicon.html>`_ 
- `Get Technocoder's osu! Wineskin with support for macOS Catalina 10.15 and later <install/10-15.html>`_ 
- `Get slc's osu! Wineskin for macOS 10.14 Mojave and earlier <install/10-14.html>`_

Some wrappers will only work on specific macOS versions or hardware specifications. Not sure which version of macOS you're using? Check out this `Apple support article <https://support.apple.com/en-au/HT201260>`_ to find out. Furthermore, `here is a list <https://support.apple.com/en-us/HT211814>`_ of Apple computer models that utilise the new ARM-based Apple Silicon chip technology.

Need help?
=======================================

Getting Windows applications to run smoothly on macOS can be a challenge, and if you're experiencing issues feel free to reach out to the community. We're most active on the osu! community help forums. Visit us on the `macOS Wineskin thread <https://osu.ppy.sh/community/forums/topics/1106057>`_ or start your own in the `Help subforum <https://osu.ppy.sh/community/forums/5>`_. 

- Along with a detailed description of your issue, attach your log files from `Troubleshooting <issues/troubleshooting.html>`_ in a never-expire pastebin such as `paste.ubuntu.com <https://paste.ubuntu.com/>`_ or `bpaste <https://bpa.st/>`_.
- If creating a thread, put **macOS** and **Wineskin** in your thread title.
- Our commmunity support members are volunteers, ranging from osu! support team members to people helping out in their free time. A response may take upwards to a week, although generally you should receive one within a day or two.

Other options
=======================================

If you prefer, other options are available, including the official (but abandoned) Wineskin from ppy, or other alternatives (that won't let you play ranked). These docs won't cover these options in great detail but they're pretty straightforward to get started with.

- `Use peppy's official Wineskin <https://github.com/ppy/osu-wine>`_
- `Try out osu!lazer, which is the upcoming major release to osu! that runs natively on macOS and Linux <https://github.com/ppy/osu>`_
- `Download opsu! - an unofficial osu! client that runs natively on macOS and Linux <https://itdelatrisu.github.io/opsu/>`_

Disclaimers
=======================================

.. warning::

   This information is supplied by volunteers in good faith. However, **we are not responsible if it doesn't work, your computer sets on fire, or you start the next nuclear war.** We do our best to make sure the information here is safe for you, your osu! account and your computer, but **you proceed at your own risk.**

.. tip::

   Don't play osu! in maths class.

****

#######################################
Sitemap
#######################################

.. toctree::
   :maxdepth: 1
   :caption: Installation

   install/choose
   install/silicon
   install/10-15
   install/10-14

.. toctree::
   :maxdepth: 1
   :caption: Welcome to osu!

   welcome/index
   welcome/screen
   welcome/import
   welcome/transfer

.. toctree::
   :maxdepth: 1
   :caption: Common issues

   issues/index
   issues/troubleshooting
   issues/applesilicon-bigsur
   issues/dotnet
   issues/commandprompt
   issues/gdiplus-cjkfonts
   issues/unidentified
   issues/monterey
   issues/start
   issues/wineskin
   issues/graphics
   issues/dualmonitor
   issues/retina
   issues/input
   issues/wontclose
   issues/malware
   issues/macos-agent
   issues/agent-crash
   issues/discord-10-14
   issues/discord-10-15
   issues/discord-disc

.. don't forget to also update `issues/index.rst`

.. toctree::
   :maxdepth: 1
   :caption: Advanced troubleshooting

   advanced/index
   advanced/silentcrash

.. toctree::
   :maxdepth: 1
   :caption: About osu!mac

   about/resources
   about/templates
   about/logs
   about/contributing
   about/acknowledgements
   about/contact
   about/license

