On the 'media' page the request takes an src value as url parameter that is not sanitized properly.

It is possible to change its content to exploit an XSS Off Domain Data Uri vulnerability.
By using the 'data:' protocol, we can load data into the website.
This payload was used to unveil a flag:
data:text/html;base64,PHNjcmlwdD5hbGVydCgxKTwvc2NyaXB0Pg==

Vulnerability:
Cross-Site Scripting vulnerabilities are used to load malicious scripts on web pages. The Off domain version is useful to bypass restrictions, and the Data Uri scheme can bypass some sanitization.

Dangers: 
While this payload only triggers an alert with the value '1', it is possible to inject malicious scripts to unsuspecting users via modified URLs, leading to authentification leaks, malicious actions(fund transfer..).

Solutions:
	- sanitize user input to escape special characters
	- content Security Policy (restrict sources of scripts allowed)
	- subressource Integrity (match the hash of scripts to verify the integrity of the loaded page)
