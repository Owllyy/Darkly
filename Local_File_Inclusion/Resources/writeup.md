While trying random page names we found that non existing pages did not always redirect to a 404 page.

Playing some more with the page name, and after some documentation we eventually found that there was a chance to access files directly on the website host.
This attempt eventually unveiled a flag:
http://10.1.8.5/index.php?page=../../../../../../../etc/passwd

Dangers:

Possible fix solution:
