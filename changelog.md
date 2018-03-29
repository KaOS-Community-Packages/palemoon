<h1>27.8.3 (2018-03-28)</h1>
This is a small update to address a pervasive crashing issue.
<h2>Changes/fixes:</h2>
* Backed out some responsive layout code that caused intermittent but not uncommon crashes in the browser depending on window sizes and page content.

<h1>27.8.2 (2018-03-22)</h1>
This is a security update.
<h2>Changes/fixes:</h2>
* Privacy fix: prevented update checks for the default theme.
* Added a user-agent override for Dropbox to improve compatibility with their service.
* Fixed an issue with mouseover handling related to (CVE-2018-5103). DiD
* Disabled the Mac OSX Nano allocator. DiD
* Fixed (CVE-2018-5129) OOB Write.
* Updated the lz4 library to 1.8.0 to solve potential issues. DiD
* Fixed (CVE-2018-5137) Path traversal on chrome:// URLs
* Fixed several memory safety an synchronicity hazards.

<strong>DiD</strong> This means that the fix is "Defense-in-Depth": It is a fix that does not apply to a (potentially) actively exploitable vulnerability in Pale Moon, but prevents future vulnerabilities caused by the same code when surrounding code changes, exposing the problem, or when new attack vectors are discovered.

<h1>27.8.1 (2018-03-06)</h1>
This is a small update to address some breaking issues.
<h2>Changes/fixes:</h2>
* Backed out the NSPR/NSS update from 27.8.0 for causing crashes, general operational instability and handshake issues.
* Disabled TLS 1.3 draft support by default, because with the NSS backout we only support an older draft right now that is no longer current and may cause connectivity issues. You can manually re-enable it at your own risk in about:config by setting security.tls.version.max to 4.

<h1>27.8.0 (2018-03-02)</h1>
This is a development update with new and improved features and bugfixes.
<h2>Changes/fixes:</h2>
* Added support for emojis on Windows systems that have relatively poor support for them with standard font sets by including our own font (EmojiOne based for now).
* Added a setting in preferences to select the use of tab previews with Ctrl+Tab.
* Added Eyedropper menu entry to the AppMenu.
* Added a preference to control whether the text cursor (caret) should be thicker when dealing with CJK characters or not (default = yes).
* Added URL fix-ups for schemes (mis-typed "ttp://" etc.).
* Added support for ES6 "Symbol species".
* Updated our TLS 1.3 support to the latest (probably final) draft.
* Fixed gap inconsistency in the tabstrip.
* Fixed a number of browser crashes.
* Fixed a crash with the exponentiation operator "**"
* Set the performance timer granularity to 1 ms.
* Updated the kiss-fft library to our forked 1.4.0 version.
* Disabled a potentially problematic optimization on Win 8+ with high contrast themes in use.
* Removed the notification bar when in full screen to prevent unwanted visible screen elements.
* Removed unmaintained and insecure WebRTC code - building with WebRTC enabled is no longer an option.
* Removed redundant checks for "Vista or later" since that is all we support.
* Added display of the http status to raw request displays.
* Added a workaround for cloned videos not retaining their muted state.
* Added a temporary workaround to avoid crashes on trackless media.
* Removed some superfluous ellipses from menu labels.
* Fixed undesired shrinking of line heights as a result of setting minimum font size in preferences.
* Fixed some issues with setting the new tab preference (regression).
