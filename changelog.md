<h1>27.9.0 (2018-04-17)</h1>
This is the last major development update for the v27 milestone (codenamed "Tycho").
After this, we will be focusing our efforts for new features entirely on UXP and the new v28 milestone building on it. We will continue to support v27.9 with security and stability updates for a while, but no major new features will be added from this point forward.
<h2>Changes/fixes:</h2>
* Fixed a number of spec compliance issues in our media subsystem.
* Added a trailing slash to referrers when policy is set to fix some web compatibility issues.
* Fixed the property order in Object.getOwnPropertyNames(string) and others for web compatibility.
* Updated RegExp(RegExp object, flags) to the ES6 standard specification.
* Changed the embedded font from the no longer free EmojiOne to the open-licensed Twemoji (with additional fixes). This also further extends unicode support to Unicode 10 emoji(s). Please note that as a result, color emoji(s) will look different than before.
* Adjusted some things in our memory allocator code to provide, among other things, better allocation alignment on Windows.
* Made the attempt to migrate people from the old sync server domain name to the current one more aggressive. We will be retiring the old pmsync.palemoon.net Sync server address shortly to remove the need for us to maintain a security certificate for it; this preference migration should automatically put everyone on the correct server address (pmsync.palemoon.org) when upgrading.
* Made reading of the sessionstore synchronous, to speed up startup and prevent the homepage from being loaded when restoring a session.
* Added a fix to switch to the correct window/tab when a web notification is clicked.
* Changed the placeholder text to not include "Search" when all search functions from the address bar are disabled.
* Enabled the use of Skia for canvas on Linux and OSX.
* Worked around a potential cause for some non-standard bitmapped fonts ending up with incorrect line heights (I'm looking at you, Noto fonts!).
* Added a workaround for incorrectly-encoded JPEG-XR images with planar alpha. Ultimately, the jxrlib reference implementation should be fixed to encode according to spec.
* Aligned XCTO:nosniff allowed script MIME types with the updated spec.
* Improved the logic for storing vector images in the surface cache.
* Fixed character set handling for XMLHttpRequests.