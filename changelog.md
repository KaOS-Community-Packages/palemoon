<h1>27.4.1 (2017-08-03)</h1>
This is a major update to straighten out most of the media streaming issues, as well as adding the necessary enhancements, bugfixes and security fixes to the browser.
<h2>Changes/fixes:</h2>
* Fixed an issue where media playback would not use hardware acceleration properly when using MSE.<br> This would cause high CPU usage and/or choppy playback for HD video on e.g. YouTube.
* Fixed ES6 iterator chains to be spec-compliant.
* Fixed ES6 vector append calls and some related memory leaks.
* Added a workaround to reduce the likelihood of a potential rare (timing-critical) crash.