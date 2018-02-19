<h1>27.7.2 (2018-02-01)</h1>
This is a security and stability update.
<h2>Changes/fixes:</h2>
* Changed the X-Content-Type-Options: nosniff behavior to only check "success" class server responses, for web compatibility reasons.
* Changed the performance timer resolution once more to a granularity of 1 ms, after evaluating more potential ways of abusing Spectre.
* This takes the most cautious approach possible lacking more information (because apparently NDAs have been signed over this between mainstream players), follows Safari's lead, and should make it not just infeasible but downright impossible to use these timers for nefarious purposes in this context.
* Improved the debug-only startup cache wrapper to prevent a rare crash.
* Fixed a crash in the XML parser.
* Added a check for integer overflow in AesTask::DoCrypto() (CVE-2018-5122) DiD
* Fixed a potential race condition in the browser cache.
* Fixed a crash in HTML media elements (CVE-2018-5102)
* Fixed a crash in XHR using workers.
* Fixed a crash with some uncommon FTP operations.
* Fixed a potential race condition in the JAR library.

<strong>DiD</strong> This means that the fix is "Defense-in-Depth": It is a fix that does not apply to a (potentially) actively exploitable vulnerability in Pale Moon, but prevents future vulnerabilities caused by the same code when surrounding code changes, exposing the problem, or when new attack vectors are discovered.

<h2>27.7.1 (2018-01-18)</h2>
This is a minor emergency update to address website breakage and a theme issue.
<h3>Changes/fixes:</h3>
* Added support for Array.prototype[@@unscopables].
* Unfortunately, the addition of Javascript's ES6 Unscopables in 27.7.0 was incomplete, which caused a number of websites (e.g. Chase on-line banking, some Russian government sites) to display blank or not complete loading after updating to that version of the browser. This update should fix the problem by adding the missing part of the feature.
* Fixed an issue with the default theme causing tab borders to be drawn too thick at higher settings for visual element scaling (125%/150%) in Windows.

<h2>27.7.0 (2018-01-15)</h2>
This is a stability and bugfix release, as well as adding a number of new features to further improve web compatibility.
<h3>Changes/fixes:</h3>
* Reorganized access to preferences (moved to the Tools menu on Linux, and renamed from "Options" to "Preferences" on Windows).
* Renamed "Restart with add-ons disabled" to "Restart in Safe Mode" to better reflect what it does.
* Worked around an issue with some improperly-encoded PNG files not decoding after our libpng update.
* Fixed an issue on Mac builds not properly populating the application menu.
* Added "My home page" as an option for new tabs.
* Added an option to disable the 4th and 5th mouse buttons (Windows).
* (mouse.button4.enabled and mouse.button5.enabled, respectively)
* Improved the resetting of non-default profiles.
* Fixed an issue with details/summary having the incorrect height if floated, breaking layouts.
* Made several more improvements to the details/summary tags to align them with the current spec and fix some additional bugs.
* Implemented support for flex/columnset contents inside buttons to align its behavior with other browsers.
* (this should fix layout issues with Twitch's new web interface)
* Fixed an issue where CSS clone operations would draw a border.
* Changed the way fractional border widths are rounded to provide more natural behavior.
* Fixed an issue where number inputs would incorrectly be flagged as read-only.
* Added assets for tile display in the Windows start panel.
* Finished sync infra swapover by adding a one-time pref migration for server used.
* Improved WebAudio API: Return the connected audio node from AudioNode.connect()
* Added support for a default playback start position in media elements.
* Fixed an assert in cubeb-alsa code (Linux).
* Added support for media cue-change events (e.g. subtitles).
* Updated SQLite to 3.21.0.
* Fixed a crash when trying to use the platform embedded.
* Fixed devtools (gcli) screenshots on vertical-text pages.
* Fixed devtools copy as cURL for POST requests.
* Improved the HTML editor component (several bugfixes).
* Added support for ES7's exponentiation a ** b operator.
* Fixed an issue with arrow functions incorrectly creating an 'arguments' binding.
* Added Javascript's ES6 "unscopables".
<h3>Security/privacy fixes:</h3>
* Disabled automatic filling in of log-in details by default to prevent potential risks of credentials being abused (e.g. for tracking) or stolen.
* Added a preference (in the category security) to easily enable or disable automatic filling in of log-in data.
* Removed the sending of referrers when opening a link in a new private window.
* Added an option to disable the page visibility Web API (dom.visibilityAPI.enabled), allowing users to prevent pages from knowing whether they are being actively displayed to the user or not.
* Removed the "ask every time" policy for cookies. For granular control, please use any of the excellent available extensions to regulate cookie use on a per-site or per-url basis.
* Added support for X-Content-Type-Options: nosniff (for scripts).
* Changed the resolution of performance timers to a level where any future potential abuse for hardware-timing attacks becomes impractical. DiD
