# Lockaa Regex Tutorial

Regex is a powerful tool used to match and manipulate text. It allows you to search for patterns within text, extract specific information, or replace text with something else. Regex is widely used in computer programming, data analysis, web development, and many other fields where text manipulation is required. Its importance lies in its ability to automate repetitive tasks and simplify complex text processing operations. With regex, you can quickly search through large volumes of data and extract the information you need in a precise and efficient manner. Overall, regex is an essential tool for anyone working with text data and is a skill that can greatly enhance your productivity and efficiency.

## Summary

In this tutorial, we will go over the various components of a regular expression. Here is a an expression defining an email handle: /^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/ . We will be looking over the various parts of this expression and how they work along with other regex components common in use but not applicable in this example.

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
Regex (which is short for Regular Expression) is a powerful tool used to match and manipulate text. It is comprised of various components, each of which performs a specific function in defining a pattern.


### Anchors
Anchors are special characters that match a specific position within a string, rather than matching any actual characters. There are two types of anchors: the caret symbol ^ and the dollar sign $. The caret symbol ^ is used to match the beginning of a string. When it is used at the beginning of a regular expression, it matches the start of a string, so the regular expression will only match if the string starts with the pattern after the caret. The dollar sign $ is used to match the end of a string. Together, the caret and dollar sign are often used to match an entire string. For example, the regular expression /^hello world$/ will only match the string "hello world", and not any other string that includes "hello world".

### Quantifiers
 In regular expressions, quantifiers are special characters that allow you to specify how many times a character or group of characters should be matched in a pattern. Quantifiers can be applied to individual characters, character sets, or groups of characters, and they control the number of times a pattern is matched. Here are a few used in our example:

The + matches the preceding character or group one or more times. For example, the regular expression /ab+c/ would match "abc", "abbc", "abbbc", and so on, but not "ac".

Curly braces with two numbers separated by a comma (ie {n,m}) matches the preceding character or group at least n times, but no more than m times. For example, the regular expression /ab{2,4}c/ would match "abbc", "abbbc", or "abbbbc", but not "abc" or "abbbbbbc".


### Grouping Constructs
In regular expressions, grouping constructs are used to group together one or more characters or expressions so that they can be treated as a single unit. Grouping constructs are enclosed in parentheses () and are used to specify the scope of an operation or a quantifier.

 Parentheses are the most common grouping construct in regular expressions. It allows you to group together characters or expressions so that they can be treated as a single unit. For example, the regular expression /(ab)+/ would match "ab", "abab", "ababab", and so on.

### Bracket Expressions
In regular expressions, bracket expressions are used to specify a set of characters that should be matched in a pattern. Bracket expressions are enclosed in square brackets [] and can include a range of characters or individual characters that should be matched. Here are a few bracket expressions used in our example.

Square brackets ( [] ) are the most common bracket expression in regular expressions. It allows you to specify a set of characters that should be matched. For example, the regular expression /[aeiou]/ would match any vowel in a string.

Hyphen inside square brackets ( [ - ] ) are used to specify a range of characters that should be matched. For example, the regular expression /[a-z]/ would match any lowercase letter in a string, while the regular expression /[0-9]/ would match any digit.

### Character Classes
In regular expressions, a character class (also known as a character set or bracket expression) is a group of characters that can be matched by a single character in a pattern. Character classes are enclosed in square brackets [] and allow you to match any one of a set of characters. Here are a few character classes from our example.

The \d (digit) character class matches any digit from 0 to 9. For example, the regular expression /\d+/ would match any sequence of one or more digits in a string.

The '.' (dot) matches any character except a newline character. For example, the regular expression /./ would match any character in a string.

### The OR Operator
In regular expressions, the OR operator (also known as the alternation operator) is a symbol that allows you to match one of several possible patterns. The OR operator is represented by the | symbol and is used to specify alternative patterns that should be matched.

In our example we don't use any OR operators but here's an example of how the OR operator works in a regular expression:

The regular expression /cat|dog/ matches either the word "cat" or the word "dog". If either "cat" or "dog" appears in the input string, the regular expression will match.

The OR operator can also be used in combination with other regular expression elements. For example, the regular expression /\d{3}-\d{2}|\d{5}/ matches either a five-digit number or a number formatted as a three-digit number followed by a hyphen and then a two-digit number.

### Flags
In regular expressions, flags are additional parameters that can be added to a regular expression to change how it behaves when matching against input strings. We don't use any in our example but here are some flags used in regular expressions:

The i (case-insensitive) flag makes the regular expression case-insensitive, so that it matches both uppercase and lowercase characters. For example, the regular expression /cat/i would match "cat", "Cat", and "CAT".

The g (global) flag enables global matching, which means that the regular expression will match all occurrences of the pattern in the input string, rather than just the first occurrence. For example, the regular expression /cat/g would match all occurrences of "cat" in the input string.

The m (multiline) flag enables multiline matching, which means that the regular expression will match patterns that span multiple lines in the input string. For example, the regular expression /^cat/m would match any line in the input string that begins with "cat".

The u (unicode) flag enables full Unicode support, including support for Unicode characters that are outside the ASCII range.

The s (dotall) flag allows the dot (.) metacharacter to match any character, including newlines.

### Character Escapes
In regular expressions, a character escape is a way to match a specific character that has a special meaning or function. It's represented by a backslash (\) followed by a specific character or sequence of characters.

For example, if you want to match a literal period character in a regular expression, you can use the character escape \.. Otherwise, the period character is interpreted as a metacharacter that matches any character.

Some common character escapes in regular expressions include \d (matches any digit character), \w (matches any "word" character), and \s (matches any whitespace character).

## Author

This tutorial was written by Allen Lockard
