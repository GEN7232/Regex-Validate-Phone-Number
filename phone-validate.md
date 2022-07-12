# Using a Regex to Validate or Match a Phone Number

When asking a user for their phone number, the code needs to be able to validate that not only is it a phone number but also match it to an existing phone number. Here I will demonstrate how to validate or match a phone number using a regular expression (regex).

## Summary

When asking a user for their phone number, the code needs to be able to validate that it is a correct phone number, and then can further be set as unique.

Validating a phone number code: `^[\+]?[(]?[0-9]{3}[)]?[-\s\.]?[0-9]{3}[-\s\.]?[0-9]{4,6}$`

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

All regular expression both start and end with a slash "/". Then to start the anchor component is shown with a caret "^". The end anchor component in this case is a dollar sign "$".

### Quantifiers

Quantifiers specify if there are any numbers of a character, character class, or group present to find a match.

(*) - Matches zero or more times
(+) - Matches one or more times
(?) - Matches zero or one times
({ n }) - Matches exactly n times
({ n, }) - Matches at least n times
({n , m}) - Matches from n to m times

Our phone validation code uses some of the following quantifiers:
A plus "+" matches the preceding item, which is "\", one or more times.
We also have a question mark "?" which means the code will look for the pattern "[-\s\.]" pattern zero to one times. It will stop as soon as it finds a match. 
The {3} will match the numbers 0-9 exactly three times.
The {4, 6} will match the numbers 0-9 four to six times.

### Grouping Constructs

Grouping constructs is done by using parentheses "()", and are also referred to as a "capturing group" at times. We do not have any grouping constructs in our code.

### Bracket Expressions

A bracket expression is an expression enclosed in square brackets "[]".
In our code the bracket expressions are:
`[0-9]` describes a single character that can be any number zero through nine.
`[-\s\.]` - matches the character "-", \s matches a single white space character, \ indicates that the next character is special.


### Character Classes

Character classes can make the regex match only one out of many characters. One can do this by placing them between square brackets as shown above.

### The OR Operator

Like in most javascript based code the word "or" is represented with a "|". There are no or operators in our code, but for example (a|b) would match either "a" or "b"

### Flags

Flags in regular expressions are used to affect the search. Our code does not include any flags.

i - the search is case-insensitive,
g - the search looks for all matches, without it only the first match is returned,
m - multiline mode,
s - enables "dotall" mode, that allows a dot "." to match newline character "\n"
u - enables full Unicode support,
y - "Stick" mode: seaches at the exact position in the text

### Character Escapes

Starting with a backslash "\" character escapes match a character having a special meaning in regex.

## Author

Written by Genevieve Nelson, a current student at the Rutgers coding bootcamp.

Github profile: https://github.com/GEN7232
