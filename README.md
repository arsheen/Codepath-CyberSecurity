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

Affected Versions: 4.2

Fixed in version: 4.2.10

References: 
https://sumofpwn.nl/advisory/2016/persistent_cross_site_scripting_vulnerability_in_wordpress_due_to_unsafe_processing_of_file_names.html

![](Week_7.gif)

## Vulnerability 2:
Unauthenticated Stored Cross Site Scripting:

Steps:
1. Intro - A text string that is longer than the SQL specified text field can lead to truncation and malformed HTML, opening up opportunities for XSS.
2. Create a string longer than the specified 64k character limit. Upoun truncation this renders as malformed HTML. Browsers try to fix this which leads to interpretation of the onmouseover exploit.
3. Create the string using the following python code to generate a file:

out = "<a title='xonmouseover=alert(unescape(/hello%20world/.source))style=position:absolute;left:0;top:0;width:5000px;height:5000px  "
with open('xss.txt','a') as f:
    f.write(out)
    for i in range(64*1024):
        f.write('X')
    f.write("</a>")

4. Use the string generated in a comment on WP.
5. View the comment to get the alerts(pop-ups) due to XSS.

Vulnerability Type:
Cross Site Scripting (XSS)

Affected Versions: 4.2

Fixed in version: 4.2.1

References:
https://wpvulndb.com/vulnerabilities/7945
http://klikki.fi/adv/wordpress2.html


    
