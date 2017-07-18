<h1>27.4.0 (2017-07-12)</h1>
This is a major update to straighten out most of the media streaming issues, as well as adding the necessary enhancements, bugfixes and security fixes to the browser.
<h2>Changes/fixes:</h2>
* Completely re-worked the Media Source Extensions code to make it spec compliant, and asynchronous as per specification for MSE with MP4. This should fix playback problems on YouTube, Twitch, Vimeo and other sites that previously had some issues. A massive thank you to Travis for his tireless work on making this happen!<br>Please note that MSE+WebM (disabled by default) is not using this new code yet (planned for the next release), and as such there is a temporary set of things to keep in mind if you don't use default settings:
  - If you have previously enabled MSE+WebM, this setting will be reset when you update to avoid conflicting settings with the updated MSE code.
  - We've added an extra setting in Options to disable the updated MSE code (asynchronous use) in case you need to use WebM or are otherwise having issues with the updated code (please let us know in that case).
  - Once again, the MSE+WebM and Asynchronous MSE use are currently mutually exclusive. You can have one or the other, not both, until we sort out the code for WebM. To enable MSE+WebM you will first have to disable Asynchronouse MSE in settings (otherwise the WebM setting will be greyed out and disabled).
* Added a control in options/preferences for HSTS and HPKP usage.
* Changed HTML bookmark exports to write CRLF line endings to the file on Windows.
* Leveraged multi-core rendering for libVPX (VP8/VP9 WebM decoding).
* Fixed some issues accessing DeviantArt (useragent-sniffing).
* Aligned CSS text-align with the spec.
* Added a recovery module for browser initialization issues (e.g. when using a wrong language pack).
* Fixed spurious console errors for XHR requests with certain http response codes.
* Enabled v-sync aligned refresh for a smoother scrolling experience.
* Removed support for CSS XP-theme media queries.
* Improved console error reporting.
* Fixed resetting toolbars and controls from the safe mode dialog.
* Fixed bookmark recovery option from the safe mode dialog.
* Fixed innerText getters for display:none elements.
* Fixed a GL buffer crash that might occur with certain combinations of drivers and hardware.
* Added some more details to about:support.
* Fixed a potential crash when the last audio device is removed during playback.
* Fixed a crash on about:support when windowless browsers are created.
* Updated <select> elements to blank if the actively set value doesn't match any of the options.
* Updated the interpretation of 2-digit years in date formats to match other browsers:<br>0-49 = 2000-2049, 50-99 = 1950-1999.
* Added "q" units to CSS (quarter of a millimeter).
* Added .origin property to blobs.
* Fixed several minor layout issues.
* Fixed disabled HTML elements not producing the proper JS events.
* Implemented web content handler blacklist according to the spec, allowing more than feeds to be registered.
* Fixed a spec compliance issue with execCommand() on HTML elements.
* Fixed a problem with table borders being drawn uneven or being omitted when zooming the page.
* Added devtools "filter URLs" option in the network panel.
* Added visual sorting options to the Network inspector.
* Added importing of login data from Chrome profiles on Windows (Chrome has to be closed first).
* Added importing of tags from bookmark export files (HTML format).
* Updated usage of SourceMap headers with the updated spec (SourceMap header, keeping X-SourceMap as a fallback).
* Fixed several cases of wrongly-used negations in JS modules.
* Added the auxclick mouse event.
* Added a control to not autoplay video unless it is in view (media.block-play-until-visible).
* Updated the Graphite font library to 1.3.10.
* Updated how image and media elements respond to window size changes (responsive design).
* Added parsing and use of rotation meta data in video.
* Fixed several crashes in a number of modules.
* Fixed performance regression for scaling large vector images (e.g. MSIE Chalkboard test) \o/
* Fixed some issues with notification icons.
* Fixed some internal errors with live bookmarks.
* Updated SQLite to 3.19.3.
* Fixed several reported issues with devtools (cli-cookies, cli help, copying cURL, inspecting SVGs, element size calculations, etc.)
* Fixed an issue where a server response was allowed to override add-ons' specified version ranges even for add-ons that have strict compatibility (e.g. themes, language packs).
<h2>Security fixes:</h2>
* Removed preloading of HPKP hosts and enabled HPKP header enforcement.
* Added support for TLS 1.3, the up-next secure connection protocol.
* Fixed an issue with TLS 1.3 not supporting renegotiation by design.
* Relaxed some restrictions for CSP to temporarily work around web compatibility issues with the CSP-3 deprecated `child-src` directive.
* Updated NSS to 3.28.5.1-PM to address some security issues.
* Updated the installer selfextractor module to address unsafe loading of libraries.
* Changed the way certain resources are included to reduce effectiveness of some common fingerprinting techniques. (e.g. browserleaks.com)
* Fixed a regression in the display of security information in the page info dialog for insecure content.
* Fixed two potential issues with allocating memory for video. DiD
* Fixed a potential issue with the network prediction algorithm. DiD
* Restricted the use of Aspirational scripts in IDNs to prevent domain spoofing, in anticipation of the UAX#31 update making this official.
* Prevented a Mac font specific issue that could be abused for domain spoofing (CVE-2017-7763)
* Fixed several potentially exploitable crashes. (CVE-2017-7751) (CVE-2017-7757) and some that do not have a CVE designation.