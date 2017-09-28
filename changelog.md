<h1>27.5.0 (2017-09-26)</h1>
This is a major update furthering general development of the browser.
<h2>Changes/fixes:</h2>
* User interface:
  - Added a menu option to restart the browser.
  - Added Windows-specific CSS parameters and queries for the use of the system accent color. Added are parameters -moz-win-accentcolor and -moz-win-accentcolortext, and the media query -moz-win-accentcolor-applies to know if Windows is actively using an accent color.
  - Changed Windows' browser CSS sheet ot use variables instead of hard-coding colors, simplifying its style and making it more flexible. Further cleaned up the Windows 10 specific browser style.
  - Changed the theme on Windows 10 to use the new accent colors and improve O.S. consistency.
  - Fixed some general inconsistencies in the Windows theme on all Windows operating systems.
  - Updated Windows widgets to be able to pick up Windows 10 accent colors dynamically and have the browser 's look and feel respond accordingly, even with automatic color changes based on desktop wallpaper.
  - Removed the experimental FF4 prerelease status-in-addressbar feature because the already-crowded address bar needs a break. This should solve some extension interop issues, theme issues and domain highlighting issues people have reported.
  - Cleaned up some dead code for the plugin updater that no longer exists.
  - Fixed a text direction issue in preferences.
  - Fixed an issue with disabled context menu entries after using Customize...
  - Reorganized and cleaned up the status preferences.

* Media:
  - MSE Media updates (ongoing). We are focusing on improving MP4 handling.
  - Improved MP3 metadata parsing (e.g. incorrect duration with embedded album cover)
  - Fixed a number of searching issues in MP3 files
  - Fixed a few crashes.

* Fixed an issue with automatically exporting bookmarks to HTML on shutdown.
* Fixed a regression re: domains allowed to/blocked from installing add-ons.
* Fixed several internal errors thrown in the front-end.
* Fixed several minor issues in the devtools.
* Added a fix to prevent the home page from being loaded (and subsequently overridden) when restoring a session.
* Added an option to control add-on blocklist behavior (Options -> Security)
* Added DOM function isSameNode().
* Added DOM onvisibilitychange event.
* Added document.scrollingelement (CSSOM).
* Added a basic implementation of Object.values and Object.entries enumerator functions (ECMA2017 draft).
* Added "Open in new private window" to bookmarks, feeds and history entries.
* Added HTTP request method OPTIONS.
* Added an option to exit to a no-content page after encountering a network or security error.
* This is controlled with the preference browser.escape_to_blank -- when set to true, "Get me out of here" buttons will load a blank page instead of the browser's home page.
* Added experimental Brotli accept-encoding (alternative to gzip/deflate compressed http data transfer). Disabled by default for now because it causes issues.
* Improved the handling of several CSS selectors.
* Changed session storage to remember form data for https sites by default.
* Added (yet another) trap prevention method to onbeforeunload events.
* Fixed privacy preferences not correctly resetting all options when choosing "Remember History"
* Fixed not being able to deselect loading bookmarks in the sidebar.
* Limited the display of user names and hosts in the http auth dialog to sane lengths, preventing over-sizing issues.
* Fixed a number of potential crash points.
* Improved the security of the Windows dll loader module.
* Reinstated "Open all in tabs" option on folders of live bookmarks (feeds).
* Made URL matching more liberal in selected text to make it easier to open stated addresses.
* Fixed an issue with Graphite font rendering where automatic font collision fixing didn't always work.
* Color Management for images is now disabled by default on Linux, due to many distributions not having a streamlined setup with sane default ICC profiles, which makes images look worse when color management is enabled.
* Tightened the update security check to prevent acceptance of update manifests that have been intercepted/replaced through https MitM attacks.
* Please be aware that https-filtering antivirus may interfere with future application updates as a result.
* Updated the ANGLE library to broaden WebGL support and reduce the potential of crashes (due to junk being sent to the video driver).
* Added content-sniffing for WebP images (working around CloudFront's incorrect content-type headers).
* Fixed a problem with some H.264 media not playing (SPS NAL).
* Improved timer efficiency (switch back to lower precision when high precision is no longer needed, reducing CPU/power consumption).
* Improved context search on selected text/links.
* Updated address bar handling with Alt or Shift modifiers, so that "switch to tab" with a modifier can open copies of already-opened sites.
* Added a fix on Linux for starting the browser from Enlightenment.
* Privacy fix: Pale Moon will now clear QuotaManager storage (asm.js cache/IndexedDB data) as part of clearing Offline Website Data.