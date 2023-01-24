On the page of the password recovery i found a <form></form> that leaks a sensitive data.

The input "mail" was hidden, but visible on the html page.
It was leaking a recovery mail "webmaster@borntosec.com".
My first test was to try an other value for this hidden input : "admin@borntosec.com" and it give me the flag.

A solution to fix this : Do not send the form with the mail input inside for regular user and complete the information on the server.