A file typically found on websites is the robots.txt file.
This file is used to let web crawlers or similar automated tools to not be accessed or indexed.

On this website it revealed the existence of a folder called .hidden.
This reveals a location with 26 folders that each lead to more folders up to a depth of 3.
Each folder also has a readme file that contains various information.
Using wget to retrieve all the content of the .hidden folder:
wget --no-clobber --convert-links --random-wait -r -p -E -e robots=off -U mozilla http://10.1.8.5/.hidden/
then using grep locally to find a file containing a string in a flag format:
grep -rl -E "[a-f0-9]{64}" /path/to/.hidden
revealed a readme file with a flag.

Dangers:

Possible fix solution:
