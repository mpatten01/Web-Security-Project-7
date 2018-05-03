# Web-Security-Project-7

# Exploit 1 - Unauthenticated Stored Cross-Site Scripting
# - The above exploit is possible on Wordpress version 4.2 and was fixed in 4.2.1. An unauthenticated user can inject java-script into a comment under a post. The code then activates when an admin views the comment. This can cause the attacker to compromise the system and/or do whatever the admin can do such as change the password or create more admins. For this to work the comment has to be very long. In my proof of conecpt, I used responded to a comment made by an admin. The comment starts with script that is meant to show an alert box with "test" written inside. That script is followed with a series of 'A's that makes the comment long enough for the exploit to work. 
<img src="https://imageshack.com/a/img923/5236/eo5Fmf.gif" width="800"> 
