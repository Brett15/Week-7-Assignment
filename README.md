# Project 7 - WordPress Pentesting

Time spent: 2.5 hours spent in total

> Objective: Find, analyze, recreate, and document **five vulnerabilities** affecting an old version of WordPress

## Pentesting Report

1. (Required)  WordPress <= 4.2.2 - Authenticated Stored Cross-Site Scripting (XSS)
  - [ ] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version:  4.2.3
  - [ ] GIF Walkthrough: <img src='https://imgur.com/a/Ut3Zv' title='GIF Walkthrough' width='' alt='GIF Walkthrough' /> 
  - [ ] Steps to recreate: Click Edit to change the page's HTML. Add the following code <a href="[caption code=">]</a><a title=" onmouseover=alert('test')  ">link</a> . Save the chagnes and then view the page, there will be text "link" which will have the stored xss.
  - [ ] Affected source code:
    - [Link 1](https://wordpress.org/news/2015/07/wordpress-4-2-3/)
1. (Required) Authenticated Cross-Site Scripting (XSS) via Media File Metadata
  - [ ] Summary: 
    - Vulnerability types: XSS
    - Tested in version: 4.2
    - Fixed in version: 4.2.13
  - [ ] GIF Walkthrough: <img src='https://imgur.com/a/P9RIB' title='GIF Walkthrough' width='' alt='GIF Walkthrough' /> 
  - [ ] Steps to recreate: Upload an MP3 file. Edit the description of the file to include the code <script>prompt(1)</script> . Then view the attachment page
  - [ ] Affected source code:
    - [Link 1](https://github.com/WordPress/WordPress/commit/28f838ca3ee205b6f39cd2bf23eb4e5f52796bd7)
1. (Required) WordPress <= 4.2 - Unauthenticated Stored Cross-Site Scripting (XSS)
  - [ ] Summary: 
    - Vulnerability types: xss
    - Tested in version:4.2
    - Fixed in version: 4.2.1
  - [ ] GIF Walkthrough: <img src='https://imgur.com/a/qbPwO' title='GIF Walkthrough' width='' alt='GIF Walkthrough' />
  - [ ] Steps to recreate: Log out to be a regular user, post a comment with xss in the attributes of the <a> tags the message must be more than 64kB of data. <a title='x onmouseover=alert(unescape(/hello%20world/.source)) style=position:absolute;left:0;top:0;width:5000px;height:5000px  AAAAAAAAAAAA...[64 kb]..AAA'></a>
  - [ ] Affected source code:
    - [Link 1](https://wpvulndb.com/vulnerabilities/7945)
1. (Optional) Vulnerability Name or ID
  - [ ] Summary: 
    - Vulnerability types:
    - Tested in version:
    - Fixed in version: 
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php)
1. (Optional) Vulnerability Name or ID
  - [ ] Summary: 
    - Vulnerability types:
    - Tested in version:
    - Fixed in version: 
  - [ ] GIF Walkthrough: 
  - [ ] Steps to recreate: 
  - [ ] Affected source code:
    - [Link 1](https://core.trac.wordpress.org/browser/tags/version/src/source_file.php) 

## Assets

List any additional assets, such as scripts or files

## Resources

- [WordPress Source Browser](https://core.trac.wordpress.org/browser/)
- [WordPress Developer Reference](https://developer.wordpress.org/reference/)

GIFs created with [LiceCap](http://www.cockos.com/licecap/).

## Notes

Finding well described vulnerabilities, some of the exploits I wanted to try were hard to figure out what I needed to do to set up an
enviroment for it to work. For example the SQLI exploits seemed like they needed some specific set up with plugins but further guide was not provided.

## License

    Copyright [2017] [Bret Tomko]

    Licensed under the Apache License, Version 2.0 (the "License");
    you may not use this file except in compliance with the License.
    You may obtain a copy of the License at

        http://www.apache.org/licenses/LICENSE-2.0

    Unless required by applicable law or agreed to in writing, software
    distributed under the License is distributed on an "AS IS" BASIS,
    WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
    See the License for the specific language governing permissions and
    limitations under the License.
