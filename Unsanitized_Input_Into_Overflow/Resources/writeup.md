On the 'survey' page, there are several input forms that are not properly sanitized.

It is possible to intercept the request (using Burp Suite for instance) and modify the input value to cause an overflow which uncovers the related flag.

Vulnerability:
Overflows can lead to the execution of malicious code.

Dangers:


Solution:
	- properly sanitize all incoming input on the server
