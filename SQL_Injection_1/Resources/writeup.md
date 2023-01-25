On the 'member' page, there is a search field that performs and SQL query which is not properly sanitized.

Normal input reveals that the user with the id 5 has Get TheFlag as first name and surname.
It is possible to use UNION to enhance the query into displaying a lot more information than intended:

all users:
'1 AND 1=1'
db host and version:
'1 UNION ALL SELECT @@HOSTNAME, @@version'
all existing tables and columns:
'1 AND 1=2 UNION SELECT table_name, column_name FROM information_schema.columns'

Upon closer inspection we can see that the users table contains several other fields than the ones displayed on the member pages, namely
town, country, planet, Commentaire, countersign.
Showing the content of the Commentaire and countersign for user 5 reveals an MD5 hash as countersign (FortyTwo) while the Commentaire hints to lower case the result (fortytwo) and perform a sha256 hash on it which yields a flag.

Possible fix solution: do not insert user input directly in SQL queries.
