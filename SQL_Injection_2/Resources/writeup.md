After finding the SQL injection vulnerability on the 'member' page, it was likely that the 'searchimg' page had the same issues.

Using UNION to show hidden fields from the list_images table reveals a MD5 hash in the comment column (albatroz) and a hint to put it to lower case then perform a sha256 hash on it which yields a flag.

Vulnerability:
A type of attack that allows unauthorized access to a website's database by using an input field to insert malicious SQL queries.

Dangers:
Access to sensitive data, ability to modify data...

Solutions:
	- using parameterized queries to ensure user input is properly separated from SQL commands
	- validation and sanitization of user input
