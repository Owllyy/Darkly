On the 'password recovery' page, there is a <form></form> that contains sensitive data.

There is a 'mail' variable that is hidden but still visible on the html page.
It discloses this recovery mail: "webmaster@borntosec.com".
The first test was to change this hidden input with "my@email.com" which uncovered a flag.

Vulnerability:
Sensitive Data Exposure is the accidental release of sensitive information (like personal information, login credentials, confidential business inforation..).

Dangers:
Depends on the nature of the leaked data.

Possible fix solution: do not send a form containing the mail input for regular users and fill the required information on the server directly.
