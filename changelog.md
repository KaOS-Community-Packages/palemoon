<h1>27.5.1 (2017-10-10)</h1>
This is a security and stability update to the browser, as well as fixing some issues users have indicated.
<h2>Changes/fixes:</h2>
* Changed the default Windows 10 styling when no accent color is applied to black-on-white.
* Changed the theme styling on Windows 10 when the system window frame is used (menu bar enabled) to use the window manager background directly, preventing visual lag updating the window color when it changes.
* Updated user agent overrides for DropBox, YouTube and Yahoo to work around user agent sniffing issues.
* Fixed a crash in the media subsystem.
* Fixed a regression where video playback hardware acceleration was disabled incorrectly on some systems.

<h2>Security fixes:</h2>
* Updated the hyphenation library to the latest upstream code to fix a security issue.
* Updated NSPR to 4.16-RTM with a patch to un-bust building on win64.
* Updated NSS to 3.32.1-RTM.
* Worked around some more issues with Mac fonts (CVE-2017-7825).
* Fixed a potential rooting hazard in NPAPI plugin code. <strong>DiD</strong>
* Fixed a potential reference issue in JavaScript arrays. <strong>DiD</strong>

<strong>DiD</strong> This means that the fix is "Defense-in-Depth": It is a fix that does not apply to a (potentially) actively exploitable vulnerability in Pale Moon, but prevents future vulnerabilities caused by the same code when surrounding code changes, exposing the problem.
