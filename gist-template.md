# Computer Science for JavaScript: Regex Tutorial

This gist tutorial will explain how a specific regular expression, or regex, functions by breaking down each part of the expression and describing what it does. Regular Expressions, known as Regex, serve to identify specific character patterns within strings. They are valuable for extracting data from code and for validation purposes. This tutorial will explore an example code excerpt that shows how to match an email address. Additionally, this will cover the various elements that make up regular expressions. 

## Summary

The following code will be the base example in this tutorial, which will showcase practical applications of regex components. It is meant for email matching purposes and can validate whether an email complies to the correct format.

/^([a-z0-10_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,5})$/

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

The anchor marks the beginning and end of a regular expression. In the email matching code,

/^([a-z0-10_.-]+)@([\da-z.-]+).([a-z.]{2,5})$/,

the anchors, ^ and $, define the boundaries. 

More specifically, the code below indicates the starting criteria, which details what is inside the parentheses later in this tutorial.

^([a-z0-10_.-]+)

The anchor also implies that any match must comply to these initial guidelines. Additionally, it must conclude with the following.

.([a-z.]{2,5})$. 

Therefore, it needs to begin and conclude following the parameters set within the code. If it does not, it will not qualify as a match.

### Quantifiers

A quantifier sets the requirement for the number of times a particular character or character group must appear to constitute a match. For example, employing the code xyz+ in our regex would match any sequence starting with xy followed by a minimum of one z. Similarly, examining our email matching code:

([a-z0-10_.-]+)

This pattern will match any string encompassing a-z, 0-10, _, ., or -. The presence of the quantifier + mandates that there must be at least one occurrence of these characters for a match to occur.

### Grouping Constructs

Group constructs are used to separate sections that fulfill different requirements. The general format is displayed below and two essentials of the groups are '()' and ':'. Grouping constructs come in capturing and non-capturing. Capturing groups store matched character sequences that can be used more than once, while non-capturing groups do not store these sequences.

(abc):(def)

### Bracket Expressions

A bracket expression (which is enclosed in square brackets) is a regular expression that matches a single character, or collating element. Please see the examples below.

[abc] - Matches any single character within the set 'a', 'b', or 'c'.
[a-z] - Matches any lowercase letter from 'a' to 'z'.
[A-Z] - Matches any uppercase letter from 'A' to 'Z'.
[0-9] - Matches any digit from 0 to 9.
[a-zA-Z] - Matches any letter, both lowercase and uppercase.
[a-zA-Z0-9] - Matches any alphanumeric character.

### Character Classes

A character class in regex defines a set of characters in an input string (within square brackets) that are meant to complete a match, which allow you to define patterns for letters, digits, special characters, or custom sets of characters within a larger string. Please see the examples below.

\d Matches a single character that is a digit.

\w Matches a word character, i.e. [a-zA-Z0-10_].

### The OR Operator

The | is related to 'OR' within regular expressions. It matches the expression that is either before or after the |. This operator can function within a group or across an entire expression. Patterns are tested sequentially and it looks for either this OR that in the matching process.

### Flags

Flags change how the expression is interpreted. Flags follow the closing forward slash of the expression. Please see the examples below.

(i) Ignore Case - This makes the pattern case-insensitive, which allows it to match both uppercase and lowercase characters interchangeably.
(g) Global Flag - This flag enables the regex to find all matches within a string, not just the first one.
(m) Multiline Flag - When the multiline flag is enabled, beginning and end anchors (^ and $) will match the start and end of a line, instead of the start and end of the whole string.
(u) Unicode - Enables full Unicode support for the pattern.
(y) The expression will only match from its lastIndex position and ignores the global (g) flag if set. Because each search in RegExr is discrete, this flag has no further impact on the displayed results.
(s) Dot (.) will match any character, including newline.

### Character Escapes

Character escapes in regular expressions are special sequences that represent a single character with a special meaning. 

The backslash (/) is an example of a character escape. For example, adding a backslash before the open paranthesis (\() means that the regex should look for the open paranthesis.

## Author

Please select the link below to view my profile.

[GitHub-Online-Profile](https://github.com/aubreymlj96)