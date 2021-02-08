# Understanding a Hex Value Regular Expression

This gist will contain information and explanations surrounding the regular expression for matching a Hex value.

## Summary

The hex value regular expression checks for the 6 or 3 character values that follow a <#> in a hexadecimal code. An example of a hexadecimal string would be #aa112233. I will be explaining how the different components of the regular expression factor into accurately registering the hex values that are being searched.

`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`

## Table of Contents

- [Understanding a Hex Value Regular Expression](#understanding-a-hex-value-regular-expression)
  - [Summary](#summary)
  - [Table of Contents](#table-of-contents)
  - [Regex Components](#regex-components)
    - [Anchors](#anchors)
    - [Quantifiers](#quantifiers)
    - [OR Operator](#or-operator)
    - [Flags](#flags)
    - [Grouping and Capturing](#grouping-and-capturing)
    - [Bracket Expressions](#bracket-expressions)
  - [Author](#author)

## Regex Components
`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`  
*Breaking the preceding regex down into its basic components we have  
  * Anchors-  **^** and **$**  
  * Quantifiers-  **?** and **{}**  
  * OR operator-  **|**  
  * Flags- **\g**  
  * Grouping and Capturing- **()**  
  * Bracket Expressions- **`[a-f0-9]`**
### Anchors
* By themselves the ^ and $ are used to match with any string that begins with the following character or group and matches with any string that ends with the preceding character respectively.
* When a regex begins with ^ and ends with $ then they work to search for an exact match for the string that is between them. 
* `/`**^#**`([a-f0-9]{6}|[a-f0-9]{3})`**$**`/`
  * This signifies that the regex is meant to capture everything between the highlighted characters.

### Quantifiers
* Quantifiers are used to signify how many characters in the expression need to be found based on the preceding criteria.
* `/^#?([a-f0-9]`**{6}**`|[a-f0-9]`**{3}**`)$/`  
* {3} and {6} are used, in conjunction with the OR operator to make sure that a hexadecimal string with either 3 or 6 characters is found.

### OR Operator
* The OR operator is used to be able to search for multiple different strings within the same regular expression. 
* `/^#?([a-f0-9]{6}`**|**`[a-f0-9]{3})$/`  
* The | is what allows one to search for either a hexadecimal of 3 characters or 6 characters in conjunction with the quantifiers in the expression.

### Flags
* While there is no flag shown in the original regex `/g` can be used to search through entire document for the associated string and not just for the first case that fits the criteria.
* `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`**g**

### Grouping and Capturing
* The () is used to place all criteria within into an array
* `/^#?`**(**[a-f0-9]{6}|[a-f0-9]{3}**)**`$/`
* In the example the parenthesis will allow the expression to capture all strings that fulfill the criteria and place them into an array.

### Bracket Expressions
* A bracket expression is meant to capture a single character within the specified criteria.
* `/^#?(`**[a-f0-9]**`{6}|`**[a-f0-9]**`{3})$/`
* The a-f and 0-9 signifies any letter or number in that range respectively and case insensitively. 

## Author
Chandler Green 
Full Stack Web Developer with experience in React, Express, Javascript and other Frontend/Backend frameworks and tools.
https://github.com/axeliono

