Following the SQL injection vulnerability, a table was revealed containing columns with sensitive information (usernames and their associated passwords).

The issue was finding the database the table was linked to.
This command was used to list existing databases:
1 AND 1=2 UNION SELECT schema_name, NULL FROM information_schema.schemata
This revealed two users (root, admin) with the same password.
Upon closer inspection the password was an MD5 hash for the string 'shadow'.
Logging in with these credentials revealed a flag.

Dangers: access to sensitive data, ability to modify data

Possible fix solution: do not insert user input directly in SQL queries.
