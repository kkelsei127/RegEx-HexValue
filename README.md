# RegEx-HexValue
This is intended to be a walkthrough on how to use a regular expression (RegEx) to match hex values. The outline below details each component of how each component of the regular expression works and how it is used.

## Summary

The following regular expression will be used to match Hex Values:

`/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`

The decriptions below will provide details on the anchors, quantifiers, grouping contructs, bracket expressions, character classes, OR Operator, flags and character escapes and how they will be used in this particular regular expression.

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

The beginning and ending of a regular expression will always include an anchor. 

For this particular example the beginning of the anchor is  `/^#` .

What follows after the anchor is what the string you are using the regular expression to search for contains. For example, `^The` means the string MUST start with `The`, `the` will not be considered as applicable.

The next character in the beginning of our anchor is the `#`. `#` is used to identify a hexadecimal number from a regular decimal number.

The ending of our anchor tag is `$/`

The `$/` represents the end of the string. It checks to see if the string will fully complete the pattern and is only used at the end. For example, `goodbye$` means the string MUST end with `goodbye`.



### Quantifiers

When matching hex values, the quantifier is `?`. `?` will imply that it is generally a boolean value, a 0 or a 1. It will make the preceding character or symbol an optional. For example, one could use an expression to find the difference between American and British spelling of awful or aweful, by putting `awe?ful`

For this specific code snippet, `/^#?` , it is stating that the preceding character of `#` is an optional character to have.

Additionally, in this code snippet the `{3}` and `{6}` are quantifiers. This means that the previous statement will be either 3 or 6 characters long. This will be covered more in detail below.


### Grouping Constructs

Next, is the grouping contruct. This groups the regular expression between an opened a closed parantheses `()`.

In this particular code snippet, `([a-f0-9]{6}|[a-f0-9]{3})` is the regex group with all the requirements nested inside, this will be covered in more detail below. 

### Bracket Expressions

After the open paranthesis is a bracket of grouped information. Often identified by square brackets `[]`.

Inside the square brackets is a piece of the expression that is used to match a specific pattern of characters identified in them. This can include alphabetic, numeric, special characters, symbols and more. A hyphen `-` will be used to describe a set or range of characters that can be used, more commonly seen as `0-9`, representing any number between 0 and 9. 

In this particular string of code the first bracket set identified by `[a-f0-9]`.


### Character Classes

Character classes are used inside the bracket expression as identified above, `[a-f0-9]` .

This character class respresents that the matching code snippet must have any lower case letter a-f and/or any number from 0-9.


### The OR Operator

The OR operator is identified by `|` . 

In the example code snippet,`([a-f0-9]{6}|[a-f0-9]{3})`, the `|` is nested betqeen two bracket expressions. This is a indicator that the boolean will match either the expression before or after the `|`.

In this particular code snippet the matching set can conain any lower case letter a-f or any number 0-9 that is 6 characters long OR it can conain any lower case letter a-f or any number 0-9 that is 3 characters long. Anything other than that will not match.


### Flags

Flags are used as advanced searching mechanisms within a regex function.

In the code snippet example, `/^#?([a-f0-9]{6}|[a-f0-9]{3})$/`, the flag is also the anchor, the `^` and the `$`. This allows the expression to cross multiple lines of code without breaking.


### Character Escapes

Character escapes are not used in this particular regex expression, they are often identified by a `\` and a letter or string of letters or a `0`. This is also case sensitive, again not used in this expression, but `\m` notated that it will only match the BEGINNING of a word, where `\M` matches only the END of a word. 


## Author

My name is Kelsei Kyser, a once pastry chef who transformed to a less messy profession, a developer (or so she thought!)! My passion is for web development and learning the newest and greatest technologies out there. My github displays many projects that help display my learned knowledge and marks milestones in my development technique and style.

For future posts or more info about Kelsei, visit her Github profile listed below. 

https://github.com/kkelsei127
