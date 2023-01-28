On the 'copyright' page the HTML code contains comments hinting at changing the referer and the user-agent in the request header for this page.

Changing the referer to:
Referer: https://www.nsa.gov/
and changing the user-agent to:
User-Agent: ft_bornToSec
reveals a flag on the page.

Vulnerability:
Broken Access Control happen when a website does not enforce proper restrictions on what users are allowed to do.

Dangers:
Mostly dependent on the website implementation, but it will typically be used to bypass access restrictions on specific content, requests, etc. and can lead to sensitive data exposure or host hijacking.

Solution: 
	- validate referer on sensitive pages by cross checking real origin and theorical origin
	- use an unpredictable randomly generated Authentification Token
