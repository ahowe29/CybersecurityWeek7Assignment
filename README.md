# CyberSecurity_Week7_Assignment

# Project 7 - WordPress Pentesting

Time spent: 4 hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

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
- [x] GIF Walkthrough:<img src='http://i.imgur.com/DfD3ETz.gif' title='GIF Walkthrough' width='' alt='GIF Walkthrough' /> 
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

- [x] GIF Walkthrough:<img src='http://i.imgur.com/xoOxt4Y.gif' title='GIF Walkthrough' width='' alt='GIF Walkthrough' /> 
- [x] Steps to recreate: 
- Choose an image that you will change the name of in your computers files.
- Rename the image to a<img src=a onerror=alert(document.cookie)>.jpg, then upload the image to WordPress
- Click on the image and then click view attachment page.
- You will recieve an error message and be redirected to the images source.
- [x] Affected source code:
- [Link 3](https://github.com/WordPress/WordPress/commit/c9e60dab176635d4bfaaf431c0ea891e4726d6e0)

4\. [x]  (Optional) WordPress 4.0-4.7.2 - Authenticated Stored Cross-Site Scripting (XSS) in YouTube URL Embeded
- [x] Summary: 
- Vulnerability types: XSS and Inject
- Tested in version: 4.2.2
- Fixed in version: 4.2.13

- [x] GIF Walkthrough:<img src='http://i.imgur.com/mPknDdx.gif' title='GIF Walkthrough' width='' alt='GIF Walkthrough' /> 
- [x] Steps to recreate: 
- Choose an youtube video that you would like to embed into the post
- Add "[embed src=âhttps://youtube.come/embed/12345\x3csvg onload=while(1){alert(document.cookie};\x3eâ][/embed]" with the URL
- Post the post
- You will recieve an error message and be redirected to the images source.
- [x] Affected source code:
- [Link 4](https://github.com/WordPress/WordPress/commit/419c8d97ce8df7d5004ee0b566bc5e095f0a6ca8)



GIF created with [LiceCap](http://www.cockos.com/licecap/).

## Notes
This assignment was challenging, but interesting.

## License

Copyright [2017] [Sasha Morgan]

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
