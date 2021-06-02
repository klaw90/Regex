# Regex Tutorial

This tutorial is to help explain the regex so that the student can understand the search pattern that regex defines.

## Summary

I will explain the Regex for matching an Email - /^([a-z0-9_.-]+)@([\da-z.-]+).([a-z.]{2,6})$/

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

The anchors that are found in this Regex are ^ (hat) and $ (dollar sign) are used to to start the expression ^ and end it $, indicating that the Regex inbetween those two symbols are what is to be matched in the input

### Quantifiers

In this Regex there are two quantifiers, + and {}. The + located in this part of the Regex "([a-z0-9_.-]+)" is saying that any of those specific characters can occur more than one time in that sequence and still be valid. The same is for this part "([\da-z.-]+)" where it's saying that following the @ symbol in the email there can be numerous occurrances of any digit and any lowercase letter as well as - and .

The bound {} quantifier sets the exact number of occurances for those characters. If there is a {,} this sets a minimum and maximum character limit. For this Regex it's saying that after the . for the email address, the characters a-z and . can be no less than two characters and no more than six characters.

### OR Operator

The OR Operator | is used to separate characters and look for either of the characters given. There is no OR Operator in this Regex.

### Character Classes

Character classes is when you want to make only one or two characters out of several characters. This is helpful when looking for words (even mispelled ones). This can be done by placing [] around the characters. There are no specific character classes in this Regex.

### Flags

Flag help narrow down specific searchs in Regex. There are 6 flags "i", "g", "m", "s", "u" and "y"

i - will search for letters regardless of their case sensitivity

g - will search for all characters in a global search and bring them back, regardless of location

m - affects the behavior of the ^ and $ anchors and can find characters at the beginning and end of multiple lines

s - this makes the wildcard (.) match all multiple lines as well

u - this is used for strings that aren't typical characters found in the UTF-16 character set

y - this is a sticky and searches for the exact position of that character within the text

### Grouping and Capturing

Grouping in Regex happens with (). The characters between the () are matched with the text input

### Bracket Expressions

Brackets are used to put multiple character grouping or sets to be matched together or apply a range of characters to be matched

### Greedy and Lazy Match

The Greedy match is when you create a Regex to match as many input characters as possible when given certain quantifers.

The Lazy match is when you try to match as few input characters as possible. For lazy matches they are often followed by a ?.

In the Regex above, we are using the greedy match.

### Boundaries

Boundary or \b is an anchor that can match a specific character to either the beginning or end of a word.

### Back-references

Back references are used to match the same character sets again without rewriting the Regex. To do this you would include \1 in the regex pattern

### Look-ahead and Look-behind

Lookaround can be used to match characters but instead of returning the specific characters asked, it will return "match" or "no match"

## Author

Kay Law (github.com/klaw90)
