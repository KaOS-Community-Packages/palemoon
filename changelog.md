<h1>28.7.0 (2019-08-29)</h1>
This is a major development update involving a partial JavaScript engine overhaul and improvement, implementing several website-impacting changes. It should be noted that these changes follow some revisions of specifications (also adopted by mainstream browsers) that are not necessarily backwards compatible for web content as some scripting behavior has changed. If you are targeting Pale Moon specifically (e.g. through ua sniffing) please check and verify the behavior is still as expected.
<h2>Changes/fixes:</h2>
* Landed a large JavaScript parser tune-up, which as a targeted goal brings our ES6 stringification fully in line with the ES2018 revision for classes, and implements rest/spread parameters for object literals. (Cheers to Luke!)
* Fixed a crash with the tuned-up parser code when certain error messages were triggered.
* Aligned browser behavior with mainstream regarding inner window behavior when domain is manipulated.
* Improved performance dealing with frame properties.
* Improved performance for handling html5 strings.
* Improved performance of image content loading.
* Fixed potential type confusion in array joins.
* Fixed an issue on some pages causing high CPU usage when wrongly specifying plugin content.
* Fixed an issue with the add-ons manager "discover" pane if no network connection is present.
* Fixed an issue with bookmark/history search results offering context menu options that would be invalid without a selection.
* Fixed the devtools JSON viewer and enabled it by default.
* Fixed searching from about:home not working for search plugins using the POST method.
* Fixed an issue with the checkboxes for location bar preferences.
F* ixed SVG alignment issues if SVG-containing elements fall on odd pixel sizes, causing blurry display of especially small SVGs like icons/glyphs.
* SVGs will now always be pixel-snapped to provide expected crisp display.
* Fixed precompilation of Sync client modules when packaging. This also removes the redundant services.sync.enabled pref.
* Added support for matroska containers and h264-based webm video formats.
* Added support for AAC audio in matroska and webm video formats.
* Added support for spaces in the Mac package and application name.
* Added an exception to the unique file origin policy for font types.
* Added native file picker support for xdg on Linux.
* Updated the default bookmark icons.
* Updated the SQLite lib to 3.29.0.
* Removed e10s information from about:troubleshooting.
* Removed hotfix leftovers.
* Removed the WebIDE developer tool.
* Removed conditional build-time disabling of the Pale Moon status bar code.
* Removed "Delete this page" and "Forget about this site" links from live bookmarks (since they make no sense on feeds).
* Removed the Financial Times' polyfill user-agent override since they updated their detection to work with Pale Moon.
