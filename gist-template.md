# Email Verifier Regular Expression

A regular expression is a string of characters written in a specific order to execute a searches for various characters and key words in a given text. Regular expressions are used for searching through and manipulating different kinds of data sets.

Think of a regular expression like a special code that acts as a search query for text. It's like having a secret code that tells you exactly what to look for in a block of text. Just as detectives use clues to find specific information in a case, regular expressions help programmers find and manipulate specific patterns in text data.

## Summary

/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/

This regular expression is used to find email addresses that match the given criteria. What are the criteria and how do we know how they function? Let's take a look:

## Table of Contents

- [Anchors](#anchors)
- [Quantifiers](#quantifiers)
- [Character Classes](#character-classes)
- [Grouping and Capturing](#grouping-and-capturing)
- [Bracket Expressions](#bracket-expressions)


## Anchors
Anchors are used to match a specific part of the string. In our example, the ^ symbol signals the beginning of our string. the $ symbol signals the end of a string.

## Grouping and capturing
Creating subexpressions by enclosing certain parts of the expression in parentheses. Like in our expression here: ([a-z0-9_\.-]+), here: ([\da-z\.-]+), and here: ([a-z\.]{2,6})

## Bracket Expressions
Brackets are used to create character sets that match any character specified within the set.

## Character Classes
Character classes specify which sets of characters we want to find. a-z matches lower-case letters. 0-9 matches digits 0 through nine. _ matches any underscores. \. matches any periods. - matches any hyphens.

@ meatches the 'at' character in an email address.

The next character set is matching characters in the second part of the email adress before the .com/.org/etc.

\d is a metacharacter that will match any digits 0-9.

a-z will match any letters a through z.

\. will match any period characters.

- will match any hypen characters.

\.([a-z\.]{2,6})  This is the last subexpression character set of our regular expression. It will match the last part of the email address (.com/.org/etc)

Within the character set (the square brackets), we are trying to match any letter a through z and any instances of a period.

{2,6} is a quantifier used to match the top-level domain part of the email address (.com/.org/etc). Here, we specify that it should be between 2 and 6 of the characters specified within the character set.


## Quantifiers
Quantifiers tell us how many times we should see these characters. In our expression, the + in ([a-z0-9_\.-]+) means we should expect multiple instances of each of these characters' usage.

## Author

Connor Allen is a junior full stack developer with one year of startup experience as a tech blogger. You can view his projects here: https://github.com/connor27allen?tab=repositories 