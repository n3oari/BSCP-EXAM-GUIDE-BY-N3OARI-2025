# Offline password cracking

First, we discovered that the cookie follows a specific structure: Base64 encoding of the username, followed by a colon (:) and the MD5 hash of the password.

![Screenshoot1](../../04-Screenshots/offline1.png)

We look for a XSS vulnerability on the website to exfiltrate the victim's session cookie:

![Screenshoot2](../../04-Screenshots/offline2.png)

Finally, we decode the Base64 cookie and use tools such as CrackStation to crack the hash and retrieve the plaintext value:

![Screenshoot3](../../04-Screenshots/offline3.png)