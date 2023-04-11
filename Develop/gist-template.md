# Explanation of regex: hex number selector

This gist explains a regex that selects certain number in hexadecimal format. This regex will select either 6 digits or 3 digits number in hexadecimal format, such as: #000000, #000, #ffffff, #fff.In most applications this can be used to select the css color code since they are coded in hexadecimal format and started with ‘#’.

## Summary

The regex used in this explanation is `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`, this regex will be break into several parts based on its type, and explained separately.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Flags](#flags)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)
- [Boundaries](#boundaries)
- [Back-references](#back-references)
- [Look-ahead and Look-behind](#look-ahead-and-look-behind)

## Regex Components

### Anchors

`^` and `$`\
`^` marks the start of a string, and `$` marks the end of a string. So, the string will not be selected from the middle, it will only be selected when it matches all the content of a 'word' not just part of it.

### Quantifiers

`?` and `{}`\
`?` shows there will be none or just one character before it. In this case the string it selected will contain one `#` or none in the beginning
`{}` shows how many characters the requirement before it. In this case `[a-f0-9]{6}` shows there will be 6 characters that matches the requirement in the `[]`, and 6 characters that matches `[a-f0-9]`.

### OR Operator

`|`\
`|` shows either condition is fine. In this case `[a-f0-9]{6}|[a-f0-9]{3}` either 6 or 3 characters that matches `[a-f0-9]` are fine for this search

### Character Classes

`a-f0-9`\
`a-f0-9` shows only 'a','b','c','d','e','f' and number '0' to '9' will be selected. Upper case is not allowed as well.

### Flags

N/A

### Grouping and Capturing

`()`\
`()` is the grouping, it separates and creates subexpression of a string. In this case since only hexadecimal number is selected, so there is no subexpression, the only grouping is for the 6- or 3-digit hexadecimal number.

### Bracket Expressions

`[]`\
`[]` shows the requirement for the search, the character classes inside this `[]` will be selected.

### Greedy and Lazy Match

N/A

### Boundaries

N/A

### Back-references

N/A

### Look-ahead and Look-behind

N/A

## Author

This gist is written by Haozhe Huang, a beginner of coding, if you want to learn more about me or connect with me, you can visit my GitHub profile at https://github.com/Haozhe-H. Feel free to explore my repositories and leave feedback if you have any suggestions or comments.
