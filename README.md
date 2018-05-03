# Web-Security-Project-7

# Exploit 1 - Unauthenticated Stored Cross-Site Scripting (XSS)
# - The above exploit is possible on Wordpress version 4.2 and was fixed in 4.2.1. An unauthenticated user can inject java-script into a comment under a post. The code then activates when an admin views the comment. This can cause the attacker to compromise the system and/or do whatever the admin can do such as change the password or create more admins. For this to work the comment has to be very long. In my proof of conecpt, I used responded to a comment made by an admin. The comment starts with script that is meant to show an alert box. That script is followed with a series of 'A's that makes the comment long enough for the exploit to work. 
<img src="https://imageshack.com/a/img923/5236/eo5Fmf.gif" width="800"> 
# Here is the source I used: https://klikki.fi/adv/wordpress2.html

# Exploit 2 - Stores XSS
# - This exploit allows a user with posting permissions (contributor or author) to compromise the site. This exploit is possible in versions 3.0 to 4.2.2. Here, the user would post specially formatted javascript into a page or post on Wordpress. Depending on the configuration of this script, it can give an unauthenticated user the capability to post or edit a post. In my example, I made a page with the follow script in it:
# <a href="[caption code=">]</a><a title=" onmouseover=alert('test')  ">link</a>
# Then an alert box pops up on the page whenever it is viewed. This exploit was patched immediately which means it was fixed by version 4.2.3.
<img src="https://imageshack.com/a/img924/7236/doGC81.gif" width="800">
# Here is the source I used: https://klikki.fi/adv/wordpress3.html

# Exploit 3 - Large File Upload Error XSS
# - This next exploit is possible in Wordpress 4.7.2 and was fixed in version 4.7.5. This exploit involves injecting malicious script into the title of an image. The victim(the admin) uploading this file will lead to XSS entering the control panel. For this to work, to file has to be too large to upload to the WordPress control panel. When the file is loaded, an error message pops up, but the script in the image name is still activated. This can be seen below.
<img src="https://imageshack.com/a/img923/8413/5xZ3dn.gif" width="800">
# Here is the source I used for this exploit: https://hackerone.com/reports/203515 
