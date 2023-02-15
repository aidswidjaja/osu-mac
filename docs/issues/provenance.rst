####################################################
Unexpected attribute data com.apple.provenance
####################################################

.. rst-class:: wineskin-version
    
    | This article is applicable to:
    | • `Technocoder <https://osu.ppy.sh/users/10338558>`_'s `Wineskin with Apple Silicon support <https://osu.ppy.sh/community/forums/topics/1106057>`_

****

****************************************
Behaviour
****************************************

When completing a report and troubleshooting process through `osu!macOS Agent <https://osu.ppy.sh/community/forums/topics/1036678>`_, you receive the following errors.

.. code-block:: bash

	[Warning][Failed] Unexpected attribute data (bundle):
	com.apple.provenance
	[Warning][Failed] Unexpected attribute data (wrapper):
	com.apple.provenance

This occurs on macOS Ventura 13.0 and higher.

****

****************************************
Cause
****************************************

A new undocumented internal API and codesigning requirement separate to the existing quarantine system has seemingly been introduced into macOS Ventura.

****

****************************************
Resolution
****************************************

This warning is safe to ignore on macOS Ventura 13.2. Please update to the latest version of macOS Ventura, and download a clean version of the most recently-available wrapper from the `osu! forums <https://osu.ppy.sh/community/forums/topics/1106057>`_.

****

****************************************
If that didn't work
****************************************

Please make a reply on `this osu! forum thread <https://osu.ppy.sh/community/forums/topics/1036678>`_ with a detailed explanation of your issue.

****

****************************************
Related links
****************************************

- https://osu.ppy.sh/community/forums/topics/1106057?n=620