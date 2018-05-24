<h1>27.9.2 (2018-05-18)</h1>
This is a security and stability update.
<h2>Changes/fixes:</h2>
* We changed the language strings for softblocked items so people will cry less when we do our job.
* (CVE-2018-5174) Prevent potential SmartScreen bypass on Windows 10.
* (CVE-2018-5173) Fixed an issue in the Downloads panel improperly rendering some Unicode characters, allowing for the file name to be spoofed. This could be used to obscure the file extension of potentially executable files from user view in the panel.
* (CVE-2018-5177) Fixed a vulnerability in the XSLT component leading to a buffer overflow and crash if it occurs.
* (CVE-2018-5159) Fixed an integer overflow vulnerability in the Skia library resulting in possible out-of-bounds writes.
* (CVE-2018-5154) Fixed a use-after-free vulnerability while enumerating attributes during SVG animations with clip paths.
* (CVE-2018-5178) Fixed a buffer overflow during UTF8 to Unicode string conversion within JavaScript with extremely large amounts of data. This vulnerability requires the use of a malicious or vulnerable extension in order to occur.
* Fixed several stability issues (crashes) and memory safety hazards.

<h1>27.9.1 (2018-05-07)</h1>
This is a maintenance release.
<h2>Changes/fixes:</h2>
* Removed the unused/incomplete places protocol handler.
* Worked around an issue with MSE media without a Track ID. This should help with the playability of some live streams.
* Ported across jemalloc improvements from UXP.
* Ported across cairo mutex improvements from UXP.
* Added support for FFmpeg 4.0/libavcodec 58.
* Added a fix for Windows 10's "isAlpha()" not being what one would expect in v1803.