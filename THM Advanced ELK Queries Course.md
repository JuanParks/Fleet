# ELK Queries
## Special Characters
There are special characters that exist within the ELK Query Language that are reserved for specific use. If instance, using a + within a query will cause the query to error. However, if you 'escape' the character
  using a backslash [\], then it will be able to be used within the query
    Example: If you are searching documents/logs that contain the term/phrase "User+1" in the username field, it will result in an error. If you escape the character though, "username:User\+1" will return the desired result
