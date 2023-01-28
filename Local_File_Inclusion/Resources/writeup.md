While trying random page names we found that non existing pages did not always redirect to a 404 page.

Playing some more with the page name, and after some documentation, we eventually found that there was a chance to access files directly on the website host.
This attempt eventually unveiled a flag:
http://10.1.8.5/index.php?page=../../../../../../../etc/passwd

Vulnerability:
Local File Inclusions vulnerabilities (LFI) happen mostly when url parameters are used to display dynamic content on pages served by servers running PHP, Java, or Js.

Dangers:
Such a vulnerability allows to view sensitive files on the system and also the execution of malicious code by including it as a local file. This type of vulnerability is generally used to gain sensitive information and/or take control of the targeted system.

Solutions:
    - sanitize user input
    - implement file access control
    - running the application within docker
    - use web application firewalls (WAF)
