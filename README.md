# CyberSecurity_Week7_Assignment

# Project 7 - WordPress Pentesting

Time spent: 4 hours spent in total

> Objective: Find, analyze, recreate, and document **three vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1\. [x]  (Required) WordPress <= 4.2 - Unauthenticated Stored Cross-Site Scripting (XSS)
- [x] Summary: 
- Vulnerability types: XSS
- Tested in version: 4.2
- Fixed in version: 4.2
- [x] GIF Walkthrough: ![week7 1](https://user-images.githubusercontent.com/10890766/31866138-bf94e780-b748-11e7-8784-a18b17b08d04.gif) 
- [x] Steps to recreate: Go to the comments section of the page.  Enter in <script>while(1){alert(document.cookie);}</script> in the comments box.  Warning once you click submit, the page will refresh and you will have an infinite amount of alert messages.  After you are done with this vulnerability, to end the message, go to the info page and delete the comment.
- [x] Affected source code:
- [Link 1](https://compsecurityconcepts.wordpress.com/tag/cross-site-scripting/)

2\. [x]  (Required) WordPress 3.6.0-4.7.2 - Authenticated Cross-Site Scripting (XSS) via Media File Metadata
- [x] Summary: 
- Vulnerability types: XSS Injection
- Tested in version: 4.1.1
- Fixed in version: 4.2.13
- [x] GIF Walkthrough: ![week7 2](https://user-images.githubusercontent.com/10890766/31866517-96cd67fe-b74e-11e7-947b-40303e8d2091.gif) 
- [x] Steps to recreate: 
    - Add three or more media files to your wordpress library, insert "Let it go <noscript/><script>alert(document.cookie);</script>" into the description of the media file.
    - Create a new post and add the media file to the post as an audio playlist.
    - You should recieve an error message when you try to create the playlist.
- [x] Affected source code:
- [Link 2](https://github.com/WordPress/WordPress/commit/28f838ca3ee205b6f39cd2bf23eb4e5f52796bd7)

3\. [x]  (Required) WordPress 2.5-4.6 - Authenticated Stored Cross-Site Scripting (XSS) via Image Filename
- [x] Summary: 
- Vulnerability types: XSS
- Tested in version: 4.2.2
- Fixed in version: 4.2.10

- [x] GIF Walkthrough:![week7 3](https://user-images.githubusercontent.com/10890766/31866449-91f3bf72-b74d-11e7-808a-7a243926bd4d.gif) 
- [x] Steps to recreate: 
- Choose an image that you will change the name of in your computers files.
- Rename the image to a<img src=a onerror=alert(document.cookie)>.jpg, then upload the image to WordPress
- Click on the image and then click view attachment page.
- You will recieve an error message and be redirected to the images source.
- [x] Affected source code:
- [Link 3](https://github.com/WordPress/WordPress/commit/c9e60dab176635d4bfaaf431c0ea891e4726d6e0)





GIF created with [LiceCap](http://www.cockos.com/licecap/).

## Notes
This assignment was interesting.

## License

Copyright [2017] [Allie Howe]

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
