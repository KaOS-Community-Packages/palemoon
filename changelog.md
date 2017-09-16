<h1>27.4.2 (2017-08-22)</h1>
This is a small update to address some security and stability issues.
<h2>Changes/fixes:</h2>
* Fixed a number of crashes.
* Enabled the opt-in debugging feature to log SSL keys to a file in all builds.
* Added a fix for TLS 1.3 handshakes causing a browser hangup.
* Handshakes should be considerably faster now and no longer stall in the wrong circumstances.

<h2>Security fixes:</h2>
* Updated NSPR to 4.15.
* Updated NSS to 3.31.1.
* Fixed a DoS issue using overly long Username in URL scheme (CVE-2017-7783)
* Fixed an issue where (cross domain) iframes could break scope (CVE-2017-7787)
* Fixed an issue in WindowsDllDetourPatcher (CVE-2017-7804)
* Fixed an issue with elliptic curve addition in mixed Jacobian-affine coordinates (CVE-2017-7781)
* Fixed a UAF in nsImageLoadingContent (CVE-2017-7784)
* Fixed a UAF in WebSockets (CVE-2017-7800)
* Fixed a heap-UAF in RelocateARIAOwnedIfNeeded (CVE-2017-7809) DiD (accessibility is disabled)
