# Regex Tutorial

Regular expressions (Regex) are a sequence of characters that define a specific search pattern. They are used to search for certain patterns of characters within a string or to find and replace a character or sequence of characters within a string. In this tutorial, we will be breaking down the components of a regular expression used to match hexadecimal color codes. Hexadecimal color codes are commonly used to represent colors on a web page using the hexadecimal color code format. There are two formats for a hex color code, a standard hex triplet and a shorthand hex format, where both formats start with a #.

## Summary

Regex: /^#?([a-f0-9]{6}|[a-f0-9]{3})$/

Components:

^ and $ are anchors that signify the beginning and end of the expression.
? is a lazy quantifier that matches the preceding element zero or one times.
[a-f0-9] is a character class that matches a single character that is a letter between a and f or a digit between 0 and 9.
{6} and {3} are quantifiers that specify the length of the preceding element.
| is an or operator that separates two options.

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [OR Operator](#or-operator)
- [Character Classes](#character-classes)
- [Bracket Expressions](#bracket-expressions)
- [Greedy and Lazy Match](#greedy-and-lazy-match)

## Regex Components

### Anchors

`/^`#?([a-f0-9]{6}|[a-f0-9]{3})`$/`

Anchors are used at the start and end of a string or expression. In this case, the regular expression starts with ^ and ends with $. The ^ anchor signifies the start of the expression, and the $ anchor signifies the end of the expression. Together, they ensure that the expression matches the entire string.


### Quantifiers

/^#`?`([a-f0-9]`{6}`|[a-f0-9]`{3}`)$/

Quantifiers are used to communicate how many characters are expected. Quantifiers specify how many instances of a character, group, or character class must be present in the input for a match to be found. By default, quantifiers are greedy, and will match as many characters as possible. If the characters *, +, ?, {}, are found within regular expressions, they are considered quantifiers.

In our regex, we have two quantifiers: {6} and {3}. These indicate that the length of the preceding element should be 6 for the hex triplet format and 3 for the shorthand hex format.

### OR Operator

/^#?([a-f0-9]{6}`|`[a-f0-9]{3})$/

The | character is an or operator that separates two options. In our regular expression, the two options are [a-f0-9]{6} and [a-f0-9]{3}. This means that our hexadecimal color code could either be 6 characters long for the hex triplet format or 3 characters long for the shorthand hex format.

### Character Classes

/^#?(`[a-f0-9]`{6}|`[a-f0-9]`{3})$/

Character classes are used to match a specific set of characters. In our regular expression, we use the character class [a-f0-9] to match any lowercase letters a to f and any digit from 0 to 9. We use this character class twice, once for the 6-digit hexadecimal value and again for the 3-digit hexadecimal value.

### Bracket Expressions

/^#?`([a-f0-9]{6}|[a-f0-9]{3})`$/

In our regular expression, we use bracket expressions to group together the character classes and quantifiers. We use parentheses () to group the expression [a-f0-9]{6}|[a-f0-9]{3} together, so that the OR operator applies to the entire group.

### Greedy and Lazy Match

/^#`?`([a-f0-9]{6}|[a-f0-9]{3})$/

In regular expressions, we have two types of matches: greedy and lazy. A greedy match will match as many characters as possible, while a lazy match will match as few characters as possible. In our regular expression, we use a lazy match for the optional # symbol, denoted by the ? quantifier. The ? quantifier causes the regular expression engine to match as few occurrences as possible, i.e., either 0 or 1 occurrences.

## Author

Jonathan Pohahau

I graduated from Charleston Southern University with a bachelors in Social and Human Sciences and a minor in Business Administration. I decided to switch to coding because I wanted the new challenges I was missing from collegiate sports, football in particular. A lot of people underestimate what a college student athlete goers through daily and i compare it to coding. Continuous just to maintain your skills, a new opponent(problem) to take on once the other one is finished, and long prep times to see how to attack the issues you are going to face. 