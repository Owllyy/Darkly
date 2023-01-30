On the 'survey' page, there are several input forms that are not properly sanitized.

It is possible to intercept the request (using Burp Suite for instance) and modify the input value to cause an overflow which uncovers the related flag.

Vulnerability:
An Overflow happens when data is put into a buffer that is too small to store it.

Dangers:
This vulnerability can lead to the execution of malicious code on the host machine, information disclosure, denial of service, or even compromise the system.

Solution:
	- properly sanitize all incoming input on the server
