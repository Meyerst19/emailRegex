# Breaking Down the Email Matching Regex

How to read and understad the email matching regex expression `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/`.

## Summary

The regex expression `/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/` may look like nonsense but it actually can be used to verify a string matches the qualifications of an Email address.

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

Anchors are what begin and end a regex expression. These anchors are `^` and `$`.

`^` signifies that the following characters will begin the string. Looking at the email matching expression `^([a-z0-9_\.-]+)` we can see that the begining of our string that follows the `^` is within the first set of parenthesis refered to as a subexpressions.

`$` will then signify that the preceding characters. `([a-z\.]{2,6})$` the subexpression (everything within the parenthesis) indicates the characters that will end the string as indicated by the anchor `$`.

### Quantifiers

Now lets look inside that ending subexpression specifically the barcketed portion `{2,6}`. This portion is a quantifier.

### Grouping Constructs

### Bracket Expressions

### Character Classes

### The OR Operator

### Flags

### Character Escapes

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
