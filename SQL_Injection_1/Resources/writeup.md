On the 'member' page, there is a search field that performs and SQL query which is not properly sanitized.

Normal input reveals that the user with the id 5 has Get TheFlag as first name and surname.
It is possible to use UNION to enhance the query into displaying a lot more information than intended:

all users:
'1 AND 1=1'
db host and version:
'1 UNION ALL SELECT @@HOSTNAME, @@version'
all existing tables and columns:
'1 AND 1=2 UNION SELECT table_name, column_name FROM information_schema.columns'

Upon closer inspection it appears that the users table contains several other fields than the ones displayed on the member pages, namely :
town, country, planet, Commentaire, countersign
Showing the content of the Commentaire and countersign for user 5 reveals an MD5 hash as countersign (FortyTwo) while the Commentaire hints to lower case the result (fortytwo) and perform a sha256 hash on it which yields a flag.

Vulnerability:
A type of attack that allows unauthorized access to a website's database by using an input field to insert malicious SQL queries.

Dangers: access to sensitive data, ability to modify data...

Possible fix solutions:

- using parameterized queries to ensure user input is properly separated from SQL commands
- validation and sanitization of user input
