# Week 7 & 8 - Wordpress Penetration testing

## Vulnerability 1:
Authenticated Stored Cross-Site Scripting via Image Filename

Wordpress(WP) versions before version 4.6.1 are vulnerable to the Cross site scripting (XSS) attack.
The XSS code can be inserted as a filename of any post attachment. This post when viewed can cause malicious actions to occur on the viewers computer.

![](Week_7.gif)
