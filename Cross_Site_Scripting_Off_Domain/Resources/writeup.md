On the 'media' page the request takes an src value that is not sanitized properly.

It is possible to change its content to exploit an XSS Off Domain vulnerability.
By using the 'data:' protocol, we can load data into the website.
This payload was used to unveil a flag:
data:text/html;base64,PHNjcmlwdD5hbGVydCgxKTwvc2NyaXB0Pg==

Dangers: while this payload only triggers an alert with the value '1', it is possible to inject malicious scripts to unsuspecting users via modified URLs.

Possible solutions: sanitize user input to escape special characters.
