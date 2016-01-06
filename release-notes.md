---
title: App Distribution Release Notes
---

<br/>
<br/>


###Previous Releases

###1.2.3.0

Updated stemcell to 3130. This is a regular security upgrade that resolves the following issues:

[USN-2806-1](http://www.ubuntu.com/usn/usn-2806-1/) Linux kernel (Vivid HWE) vulnerability
<br/>

[USN-2798-1](http://www.ubuntu.com/usn/usn-2798-1/) Linux kernel (Vivid HWE) vulnerabilities


###1.2.2.0

Fix to disable verbose loggin during installation process

###1.2.1.0

* Support for PCF 1.6
* API to upload files to builds
* Minor bug fixes and UI updates

###1.1.0.0

* Provided APIs that can be used by CI scripts to create a build and upload a file
* Minor UI updates - new login page, view login profile (from user id dropdown)

###1.0.1.28

* Support for external MySQL and Redis services
* Support for PCF 1.4 on AWS

Known issues:

* On AWS, this version supports deployments in the US-East region. Multi-region support is coming in a future release.
* The experimental HTTPS-only feature in Elastic Runtime 1.5 may cause issues with this version of the product. Full support for HTTPS-only traffic is coming in a future release.

<p class="note"><strong>Note</strong>: BOSH Stemcell 2865.1 is required for installation on Ops Manager 1.5.x and above.</p>

###1.0.1.15

* Offline installation support
* Compatibility with PCF 1.4 (vSphere)

###1.0.0

* Create a project from which app releases will be sent
* Pivotal Tracker integration (features delivered, bugs fixed, etc.)
* Create and share multiple app releases to testers
* Role based access:

     * Administrator - create/view all projects, add project users, and create app releases
     * Member - create app releases and add project users
     * Viewers - view app releases (must be a project member)
