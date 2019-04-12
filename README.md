# Week 7 & 8 - Wordpress Penetration testing

## Vulnerability 1:
Authenticated Stored Cross-Site Scripting via Image Filename

Steps:
1. Intro -The XSS code can be inserted as a crafted filename of any post attachment. This post when viewed can cause malicious actions to occur on the viewers computer.

2. The file name given to the image to be used here is:
<img src=a onerror=alert(document.cookie)>.jpg

3. The image is uploaded in a post as an attachment file.

4. When the post is viewed an alert pops up on the viewers screen.

Vulnerability Type:
Cross Site Scripting (XSS)

Affected Versions: 4.2-4.6

Fixed in version: 4.6.1

References: 
https://sumofpwn.nl/advisory/2016/persistent_cross_site_scripting_vulnerability_in_wordpress_due_to_unsafe_processing_of_file_names.html

![](Week_7.gif)
