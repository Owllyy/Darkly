Following the SQL injection vulnerability, a table was revealed containing columns with sensitive information (usernames and their associated passwords).

The issue was finding the database the table was linked to.
This command was used to list existing databases:
1 AND 1=2 UNION SELECT schema_name, NULL FROM information_schema.schemata
This revealed two users (root, admin) with the same password.
Upon closer inspection the password was an MD5 hash for the string 'shadow'.
Logging in with these credentials revealed a flag.

Vulnerability:
A type of attack that allows unauthorized access to a website's database by using an input field to insert malicious SQL queries.

Dangers: access to sensitive data, ability to modify data...

Possible fix solutions:

- using parameterized queries to ensure user input is properly separated from SQL commands
- validation and sanitization of user input
