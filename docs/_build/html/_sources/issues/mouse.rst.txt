##############################################
Performance issues with high-polling rate mice
##############################################

.. rst-class:: wineskin-version
    
    | This article is applicable to the following wrappers:
    | • `slc <https://osu.ppy.sh/users/7978076>`_'s `Wineskin for macOS 10.14 Mojave and earlier <https://osu.ppy.sh/community/forums/topics/682197?start=6919344>`_
    | • `Technocoder <https://osu.ppy.sh/users/10338558>`_'s `Wineskin with macOS Catalina 10.15 support <https://osu.ppy.sh/community/forums/topics/1106057>`_
    | • `Technocoder <https://osu.ppy.sh/users/10338558>`_'s `unofficial Wineskin for macOS 10.14 Mojave and earlier <https://osu.ppy.sh/community/forums/topics/682197>`_

****

****************************************
Behaviour
****************************************

Users may encounter issues when using high-polling rate computer mice with osu!, due to incompatibilities between higher polling rates with macOS and Wine. This includes increased lags and instability when using mice above 500Hz.

****

****************************************
Cause
****************************************

`Mouse polling rates are a known issue with Wine. <https://wiki.archlinux.org/title/mouse_polling_rate#Polling_rate_resulting_in_lag_with_wine>`_, and although it has been marked as ``CLOSED NOTOURBUG``  on the `WineHQ Bugzilla page <https://bugs.winehq.org/show_bug.cgi?id=46976>`_, users have been experiencing issues with high polling rates and Wine. macOS has also been known to suffer from incompatibilities with high polling rates, `including CPU spikes <https://discussions.apple.com/thread/252038691>`_ and `game incompatibilities <https://www.reddit.com/r/macgaming/comments/nwxa8d/comment/h1d4cdf/?utm_source=share&utm_medium=web2x&context=3>`_.

****

****************************************
Resolution
****************************************

There is no known fix for this issue, but there are different steps which have worked for different users.

- Update osu!
- Update macOS
- Decrease polling rate from 1000Hz to 500Hz
- Switch from a USB3 to USB2 port
- Avoid the macOS Mojave 10.14.6 Security Update (user-suggested, unconfirmed)

****

****************************************
User reports
****************************************

- `User report #1 <https://osu.ppy.sh/community/forums/posts/8311721>`_

****

****************************************
If that didn't work
****************************************

There could be something else going on here, and performing `basic troubleshooting <troubleshooting.html>`_ should help you get to the bottom of it.

If you're still not sure what's going on here, copy any osu! crash logs and `generate a report with osu!macOS Agent <troubleshooting.html#generating-a-report-with-osu-macos-agent>`_, then let us know on the forums with what we can help.