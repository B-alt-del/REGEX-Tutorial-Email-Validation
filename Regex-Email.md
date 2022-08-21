# Regex Tutorial: Email Checking Algorithm

In search algorithms, Regex (regular expressions) are used to find patterns patterns of characters within a string, and to find and replace a character or sequence of characters within a string. They are also frequently used to validate input. They are very use full and important to understand.

## Summary

`/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`

The code snippet above is used to validate if a given string is in the form of an email. It breaks down into multiple components, checking the 'username', the domain of the service used, and then the domain extension. 


## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Grouping Constructs](#grouping-constructs)
- [Bracket Expressions](#bracket-expressions)
- [Character Classes](#character-classes)
- [The OR Operator](#the-or-operator)
- [Flags](#flags)
- [Character Escapes](#character-escapes)

## Regex Components

### Anchors

/`^`([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})`$`/


Anchors let the algortithm know where to start or end the pattern search.

The `^` component matches anything that begins at the start of the string, for example, ^kit woulld match kits and kitchen but not skits.

The `$` works in a similar way but starting at the end for example cause$ matches cause and because but not causes.

The email regex starts with ^ and ends with $. 

### Quantifiers

/^([a-z0-9_\.-]`+`)@([\da-z\.-]`+`)\.([a-z\.]`{2,6}`)$/

Quantifiers determine the number of characters or expressions to match. 

The `+` matches the proceeding character class and means that there must be 1 or more

The `{2,6}` represents a minimum and maximum number of characters, in this case no less than 2 and no more than 6.

### Grouping Constructs

/^`([a-z0-9_\.-]+)`@`([\da-z\.-]+)`\.`([a-z\.]{2,6})`$/

The `(  )` captures a match and then remembers it. The groups are stored in an array in the order they were captured. For the emails it is usefull to remember these things to match an email to itself. The array would be [(name),(domain),(domain extension)]

### Bracket Expressions

/^(`[a-z0-9_\.-]`+)@(`[\da-z\.-]`+)\.(`[a-z\.]`{2,6})$/

The brackets are used to group together character classes, when making the match in the algorithm it may use any of the characters included inside the brackets.

### Character Classes

/^(`[a-z0-9_\.-]`+)`@`(`[\da-z\.-]`+)\.(`[a-z\.]`{2,6})$/

`@` Match the @ sign, between the username and the service's domain name.

`[a-z0-9_\.-]+ `  

Means match any characters a-z, any digits 0-9, underscores, periods, and dashes 
and the `+` means match one or more.

`[\da-z\.-]+`

`\d` is shorthand for `0-9`, so includes digits, letters, periods and dashes

`[a-z\.]`

Match letters a-z and periods

### The OR Operator

The OR operator `|` is not used in the email regex but it allows an option for matching. 
For exanmple, /green`|`red/ would match either the word green or the word red

### Flags

There are 6 regex flags in javascript, they allow to assign special situations. for example the `i` flag would indicate case insensitivity. There are not any flags in the email regex.

### Character Escapes

/^([a-z0-9_`\.`-]+)@([`\d`a-z`\.`-]+)`\.`([a-z`\.`]{2,6})$/

Character escapes are indicated with a `\` and let the algorithm know that the next character is going to be treated differently.

`\.` indicates that the period should be treated as a period and not as its normal meaning which is to represent any character

`\d` means rather than matching the letter d, it stands for a digit, it is the equivalent of writing `0-9`

## Author

I am a student in the Full Stack coding bootcamp, learning how to code has been very interesting and very exciting, regular expressions seem like jibberish at first but once you start to break them down they are really quite simple. 

Bradley Schill: https://github.com/B-alt-del/REGEX-Tutorial-Email-Validation
