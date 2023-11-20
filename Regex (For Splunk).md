# Notes for Splunk
## Regex Token(s)
1. ^ Sets position at start of line
2. $ Sets position at end of line
3. \s One white space, \s+ One or more white spaces
4. [a-z] Any lowercase character between a-z, [a-z]+  // adding the plus means one or more lowercase characters
5. [A-Z] Any uppercase character between A-z, [A-Z]+  // adding the plus means one or more uppercase characters
6. [0-9] Any numeric between 0-9, [0-9]+  // adding the plus means one or more numeric characters
7. \w Equals to [a-zA-Z0-9_], \w+  // adding the plus means one or more of any of these characters (generalized)
8. \d Matches a digit (equall to [0-9]), \d+ // adding the plus means one or more of a digit between 0-9 (any number)
9. .(dot) Any character (except for line terminators)
10. .+ or .* Any number of characters
11. () Unnamed capture group
12. (?<filed1>) Named capture group
13. \d{1,3} Matches optional digits from 1 to 3,, useful while extracting IP

## Examples of how to search/query on Splunk using Regex
- When searching in Splunk using regex..
> | rex "\<insert regex here\>"
- If you are looking for a specific log set with specifc dates, how would you use regex to query for this?
> \d{4}-\d{2}-\d{2}
>> If the log has two dates \& you wanted to identify only the first date, then the query would look like ^\d{4}-\d{2}-\d{2}
- To set a (un)named group... ^(\d{4}-\d{2}-\d{2})  /// ^(?\<date\>\d{4}-\d{2}-\d{2})
> The group will now be named 'date'
- 
