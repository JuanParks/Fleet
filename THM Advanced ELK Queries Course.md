# ELK Query Notes
## Special Characters
There are special characters that exist within the ELK Query Language that are reserved for specific use. If instance, using a + within a query will cause the query to error. However, if you 'escape' the character
  using a backslash [\\], then it will be able to be used within the query
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Example: If you are searching documents/logs that contain the term/phrase "User+1" in the username field, it will result in an error. If you escape the character though, "username:User\\+1" will return the desired result

## Wildcards
Wildcards allow for general searches to be done. The wildcard character [\*] is used to find any character & any amount of characters within a query.
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Example: If you are searching all documents that contain the words "hacking" and "hack" within the "activity" field, then the query would look like "activity:hack\*" 
