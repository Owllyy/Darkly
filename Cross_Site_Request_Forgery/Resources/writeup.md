On the 'copyright' page the HTML code contains comments hinting at changing the referer and the user-agent in the request header for this page.

Changing the referer to:
Referer: https://www.nsa.gov/
and changing the user-agent to:
User-Agent: ft_bornToSec
reveals a flag on the page.

Dangers:

Possible fix solution: validate referer on sensitive pages by cross checking real origin and theorical origin.
