After finding the SQL injection vulnerability on the 'member' page, it was likely that the 'searchimg' page had the same issues.

Using UNION to show hidden fields from the list_images table reveals a MD5 hash in the comment column (albatroz) and a hint to put it to lower case then perform a sha256 hash on it which yields a flag.

Possible fix solution: do not insert user input directly in SQL queries.
