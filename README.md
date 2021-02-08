# Understanding a Hex Value Regular Expression

This gist will contain information and explanations surrounding the regular expression for matching a Hex value.

## Summary

The hex value regular expression checks for the 6 character values that follow a <#> in a hexadecimal code. An example of a hexadecimal string would be #aa112233. I will be explaining how the different components of the regular expression factor into accurately registering the hex values that are being searched.

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
  *OR operator-  **|**  
  * Flags- **g**(global)  
  * Grouping and Capturing- **()**  
  * Bracket Expressions- **`[a-f0-9]`**
### Anchors
* By themselves the ^ and $ are used to match with any string that begins with the following character or group and matches with any string that ends with the preceding character respectively.
* When a regex begins with ^ and ends with $ then they work to search for an exact match for the string that is between them. 
* /`^#`([a-f0-9]{6}|[a-f0-9]{3})`$`/
  This means that everything the regex is meant to capture everything between the highlighted characters.

### Quantifiers

### OR Operator

### Flags

### Grouping and Capturing

### Bracket Expressions

## Author
Chandler Green 
Full Stack Web Developer with experience in React, Express, Javascript and other Frontend/Backend frameworks and tools.
https://github.com/axeliono

