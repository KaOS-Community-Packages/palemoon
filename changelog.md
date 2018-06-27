<h1>27.9.3 (2018-06-12)</h1>
This is a security update.
<h2>Changes/fixes:</h2>
* (CVE-2017-0381) Ported a patch from libopus upstream. Note, contrary to that report, the libopus maintainers state they don't believe remote code execution was possible, so this was not a critical patch.
* Fixed an issue with task counting in JS GC.
* Fixed a use-after-free in DOMProxyHandler::EnsureExpandoObject (thanks to Berk Cem Göksel for reporting).