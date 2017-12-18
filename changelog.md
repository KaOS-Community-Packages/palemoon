<h1>27.6.2 (2017-11-28)</h1>
This is a security and minor bugfix update to the browser.
This will most likely be the last update for 2017, with the holidays not far away.
<h2>Changes/fixes:</h2>
* Implemented the concept of so-called "cookie-averse document objects" which is a security & privacy measure that blocks certain web content from setting cookies. This mitigates cookie-injection, which might help against "hidden" cookie tracking.
* Mitigated some domain name spoofing through IDN by using dotless-i and dotless-j with accents. (CVE-2017-7832)
* Pale Moon will display these kinds of spoofed domains in punycode now in the actual address bar.
* Please note that the identity panel will always be able to help you on secure sites when IDNs are in use to notice potential spoofing, as opposed to relying on detection algorithms in the URL itself. As such, some other issues like CVE-2017-7833 are already mitigated by us.
* Fixed an issue with mixed-content blocking. (CVE-2017-7835)
* Added an extra check for the correct signature data type on certificates.
* Added missing sanitization in exporting bookmarks to HTML. (CVE-2017-7840)
* Fixed several crashes and memory safety hazards.
* Fixed the Linux load throbber image to be properly encoded, to prevent flickering.
* Removed the shortcut key combination for restarting the browser to avoid issues with people using certain keyboard layouts hitting the combination and unintentionally triggering a browser restart.

<h2>27.6.1 (2017-11-15)</h2>
This is a minor bugfix release to address some pressing issues people have reported.
<h3>Changes/fixes:</h3>
* Fixed a regression with new windows (opening two windows from the command-line or file association, focus issues on new windows, not loading the home page in a new window, etc.)
* Aligned XHR with the currect spec to allow withCredentials.
* Fixed an input element focus issue within handlers.
* Fixed the processing of all-padding HTTP/2 frames to prevent rare HTTP/2 hangups.
* Updated CitiBank override to work around their login issues.
* Updated Netflix override to a community-supplied one that seems to satisfy their arbitrary restrictions better.

<h2>27.6.0 (2017-11-07)</h2>
This is a major development update.
<h3>Changes/fixes:</h3>
* Dropped support for Direct2D 1.0 to avoid font rendering issues. Windows installations not capable of using Direct2D 1.1 will now fall back to software rendering. As a result, fonts may look different from this version onwards if you are on Windows Vista or Windows 7. Users on Windows 7 affected by this should install the Platform Update to re-enable Direct2D.
* Updated the Brotli decoder library, and enabled support for Brotli HTTP content-encoding by default.
* Added notifications to inform users about WebExtensions not being supported if they try to install them (as opposed to "extension is corrupt")
* Added a number of DOM childNode convenience functions. This should fix some lazy-loading frameworks. (enjoy your LOLcats again!)
* Changed automatic updates over to the new infrastructure.
* Added extra proxy settings in Options, covering DNS lookups through SOCKS v5 and automatic proxy authentication with known credentials.
* Added a selectable fallback character encoding of UTF-8 and fallback to UTF-8 as a last effort. (Issue #1423)
* Improved timing of canplay and canplaythrough firing to work around a potential race condition locking up queued video playback.
* Improved upmixing of mono sound for multi-channel setups.
* Fixed a parallelization issue with the KISS-FFT library causing CPU-deadlocked threads (Issue #1425)
* Fixed "Remove from history" function from the downloads panel.
* Forced focus on the address bar in new windows if the content is a blank/empty document.
* Fixed the dropmarker in the address bar to allow the suggestions to be closed with a click.
* Further cleaned up the status bar code.
* Disabled window.showModalDialog; it's been removed from the spec 2 years ago and has potential abuse issues (modal dialogs block the UI)
* Fixed image decoder calls to make sure the image load event doesn't fire prematurely.
* Updated LibPNG to 1.6.28, and enabled faster SSE2 decoding.
* Updated WOFF2 code from upstream.
* Updated the zlib compression library.
* Made general improvements to internal code structure and spec adherence.
* Fixed an issue with certain command-line parameters being used.
* Updated the default theme to improve consistency and contrast of toolbar and download buttons.
* Increased the default duration of notification pop-ups and made them configurable.
* Improved handling of audio-visual media (ongoing).
* Fixed an issue in CSS where elements would sometimes reflow to the next line even with sufficient visual space.
* Aligned the implementation of for(let x=y;;) loops with the final ES6 specification.
* Fixed the selection system inside of a nested contenteditable element being broken.
* Fixed Windows 10 detection for blocklisting graphics drivers.
* Enabled pasting of clipboard data in documents without an editor element to improve web compatibility.
* Fixed the uninstallation routine of restartless add-ons.
* Fixed the handling of unimplemented functions in the console API.
* Updated the Facebook user-agent to enable otherwise vendor-restricted functionality.
* Updated the SVG scaling cache limit to be more lenient for larger SVG images at a small performance trade-off, working around some sites' design issues.
<h3>Security/privacy fixes:</h3>
* Added an option to clear Site Connectivity Data (delete history).
* Removed stale entries from the HSTS preload list, and improved generation/processing of it.
* Removed undesired certificate issuer organization to common name fallback (if issuer org is empty).
* Added pretty-printing for ECDSA-SHA224, 256, 384 and 512 hashed certificate signatures.
* Worked around some more issues with broken Apple fonts.
