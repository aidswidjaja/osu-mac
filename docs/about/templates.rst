################################################
Support templates
################################################

.. note::

	Use these BBcode supported templates as a quick and effective initial troubleshooting step for new incidents on the osu! forums. You can rely off support templates once initial diagnostic troubleshooting has been established. 
	
================================================
Initial troubleshooting and diagnostics
================================================

.. code-block::

	Welcome to the support forums to help you get osu! running on macOS. To help us understand your issue a bit better, please perform the following initial troubleshooting & diagnostic steps as listed below (also available at https://osu-mac.readthedocs.io/en/latest/issues/troubleshooting.html).

	[box=Troubleshooting steps]
	[b]Step 1: See whether you can troubleshoot the problem yourself[/b]
	Many issues already have solutions available to them. Check out the [url=https://osu.ppy.sh/community/forums/posts/7560723]installation guide[/url], [url=https://osu-mac.readthedocs.io/en/latest/issues/index.html]osu!mac documentation project[/url] and the outdated [url=https://osu.ppy.sh/community/forums/topics/679205]troubleshooting guide[/url].
	
	If you're still unable to solve your issue, move onto the next step.
	
	[b]Step 2: Report and repair using osu!macOS Agent[/b]
	[list=1]
	[*]Download the latest version of Technocoder's [url=https://osu.ppy.sh/community/forums/topics/1036678]osu!macOS Agent[/url] - older versions may have incompatibilities or bugs, especially with newer wrappers.
	[*]Once it finishes downloading, open [b]osu!macOS Agent[/b].
	[*]If you haven't already done so, click the [b]Select[/b] button and browse to osu!.app's location. The text box should display its filepath (e.g ~/Users/firefly/Desktop/osu!.app) and Wine Engine (e.g WS11WineCX64Bit19.0.1-1)
    [*]Select the [b]Troubleshoot[/b] tab, then click [b]Scan[/b].
	[*]After the scan completes, click [b]Repair[/b].
	[*]If this doesn't fix your issue, click [b]Copy Report[/b]. Copy the contents into a reply to this thread and we'll do our best to help you out! Please don't forget to do a [b]Test Run[/b] as outlined in the next step.
	[/list]
	[b]Step 3: Generating a Test Run through Wineskin[/b]
	[list=3]
	[*]Locate your osu! installation.
	[*]Right click on it, then select [b]Show Package Contents[/b].
	[*]Open [b]Wineskin[/b].
	[*]Click [b]Advanced[/b].
	[*]Click [b]Test Run[/b]. If osu! starts successfully (even with glitches), you can then close the program down. Once the program has either closed or crashed, a dialog will pop up asking you whether you want to view [b]Test Run Logs[/b]. Click [b]Yes[/b].
	[*]Copy the results of your Test Run logs to a pastebin such as url=https://paste.ubuntu.com]paste.ubuntu.com[/url] set to never expire. Then attach the link in a reply to this thread, along with the report from osu!macOS Agent in Step 1.
	[/list]
	If you need any help with any of the steps outlined here, check out https://osu-mac.readthedocs.io/en/latest/issues/troubleshooting.html or feel free to make a reply back here on the forum. Thanks!
	[/box]
	
================================================
osu! on Apple Silicon and Big Sur
================================================

.. code-block::

	[b]Note about Apple Silicon:[/b] We are currently aware of potential issues impacting Apple Silicon users... please follow the troubleshooting steps at https://osu-mac.readthedocs.io/en/latest/issues/troubleshooting.html, including an osu!macOS Agent report and a Wineskin Test Run. It will help us try and fix your issue, and provide better and more stable updates to future wrappers.
	
	[b]Note about macOS Big Sur 11.x:[/b] We are also currently aware of issues on Big Sur for both Intel x86-based systems, and Apple Silicon systems... please follow the troubleshooting steps at https://osu-mac.readthedocs.io/en/latest/issues/troubleshooting.html, including an osu!macOS Agent report and a Wineskin Test Run. It will help us try and fix your issue, and provide better and more stable updates to future wrappers.
	
================================================
exec(number).bat issue
================================================

.. code-block::

	[b]If you are experiencing an error within Wineskin.app that reads "Error while writting file: The folder “exec[number].bat” doesn’t exist."[/b] that prevents you from troubleshooting, download the latest version of osu!macOS Agent. For additional information and solutions, see https://osu-mac.readthedocs.io/en/latest/issues/wineskin.html. If these steps don't fix it, you might be experiencing another issue with the same symptom... please follow the troubleshooting steps at https://osu-mac.readthedocs.io/en/latest/issues/troubleshooting.html, including an osu!macOS Agent report and a Wineskin Test Run. It will help us try and fix your issue, and provide better and more stable updates to future wrappers.
