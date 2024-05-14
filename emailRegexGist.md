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

Now lets look inside that ending subexpression specifically the barcketed portion `{2,6}`. This portion is a quantifier. It specifies what the precededing sections length needs to be. Between 2 and 6 characters.

### Grouping Constructs

Each of these section is primary grouped using `()` as subgroups. To break up these subgroups we will need to use grouping constructs. This is done with a `:`. Since within the regex for an email use specific characters between subexpresssions we do not need to use a colon. Instead the subgroups are divided between from the start to `@` and then from there to `.` and then the closing subgroup.

### Bracket Expressions

We can see within these subgroups the use of `[]` called breacket expressions. In here we can state what values that subgroup needs to consist of.

`[a-z0-9_\.-]` - Any lowercase letters from a to z, any digit between 0 and 9 or `_`,`\`,`.`, or `-` (see OR Operator)

`[\da-z\.-]` - here `\d` (See Character Classes) represents any digit from 0 to 9. Then as before it can be a lower case letter from a to z or `\`,`.`, or `-`

### Character Classes

THese define a set of characters, any one of which can occur in an input string to fulfill a match. As show above with `\d`.

### Character Escapes

If a set of chacters represents a character class if needed we cna escape this by preceding it with a `\`

### The OR Operator

As within javascript the OR operator is defined with the `|` and acts just as such within javascript context. Our regex doen't rely on any or operators.

### Flags

These are the only exception to the rule of wrapping a regex in slashes. Flags specify addition fuctionality.

## Author

I am Tyler Meyers. More naturally writing code over text and hopefull soon employeed to do so. Check out my github profile to see what I'm doing: `https://github.com/Meyerst19`
