# What is Regex? A Quick Tutorial

Regex stands for Regular Expressions.  They are special strings that represent a pattern that can be matched in a search operation.  They are important tools used in many computer applications, such as in programming languages live Java Script and perl.  They also can be used to text processing tools like sed, grep, and vim.

Usually such patters are used by string-searching algorithms for "find" or "find and replace" operations on strings, or for input validation.

## Summary

There are many types of regular expressions.  For this tutorial I decided to use a regular expression that can be used to verify that user input is a valid email address:

Matching an Email – 

```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```

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
```
====================
```

### Anchors
The Anchor starts and ends the Regular Expression or the beginning of the string and the end of the string.  They are regex tokens that do not match any characters but that say or asset something about the strong of the matching process.  

For this example it is as follows (the entire sequence):

```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/
```

The anchors are the `^` and the `$`.  This Expression is specifically looking for a string that starts with:

```
^([a-z0-9_\.-]+)
```

And then it has to end with this string:

```
.([a-z\.]{2,6})$
```

### Quantifiers
Quantifiers specify how many instances of a character, group, or of a character class that must be present in that input for a match to be found.  For example, if we used the following string `abc+` then this will match any string `ab` followed by at least one `c`.

So if we review our email string above:

```
^([a-z0-9_\.-]+)
```
It would return a match for any string that starts with `z-z`, `0-9`, `_/.`.  The quantifier `+` means that it has to contain at least one of these in order to have a match.  

### OR Operator

You can use Regular Expression Operators to match characters in text strings.  

If you wich to use the OR Operator or `|` lets use the following string to match a hex code:

```
/^#?([a-f0-9]{6}|[a-f0-9]{3})$/
```
This is Regex for marching a hex code that uses the OR Operator.  This will match starting with `#` and then followed by one of the following:

```
[a-f0-9]{6}
```
This would match a 6 character long string that contains a combination of letters and numbers.

`|` OR Operator

```
[a-f0-9]{3}
```
Will match a 3 character long string that contains letters and numbers as well. 


### Character Classes

Character Classes are a set of characters enclosed within square brackets.  They specify the characters that will successfully match a single character from a given input string.  

In our email example above, the string within any of the `[]` brackets are Chracter Classes such as:
```
[a-z0-9_\.-]
``` 
or
```
[a-z\.]
```

### Flags

A regular expression can consist of a pattern and optional flags: g, i, m, u, s, y.  Without flags and special symbols the search by a regexp is the same as a substring search.  

In any reglaur expression you could use the following flags:
- `g` - matches the pattern multiple times
- `i` - makes the regex case insensitive
- `m` - enables mul-line mode
- `u` - enables support for unicode
- `s` - short for single line

There are no flags used in our matching email example for this tutorial.  A regular expression typically comes like follows:

```
/regex/
```
Where above the forward-slashes denote where the regular expression starts and ends.  A flag may be used after the forward-slash to give more guidelines for our matching.  


### Grouping and Capturing

Capturing groups are a way to treat multiple characters as a single unit.  They are created by placing the characters to be grouped inside a set of parentheses.  For example, the regular expression "cat" cretaes a single group that contains the letters "c", "a", "t".  

Our email example has 3 groups all of which are in parentheses.  They are here below:
```
([a-z0-9_\.-]+)
```
```
([\da-z\.-]+)
```
```
([a-z\.]{2,6})
```


### Bracket Expressions

Bracket Expressions is an expression enclosed in square brackets `[]`.  It matches a specific set of single characters and may match a specific set of multi-chracter collating elements, based upon the non-empty set of list expressions contained in the bracket expression.  

From our email example above, this would simply be the characters within the square brackets.  Here is one of them below:
```
[a-z\.]
```


### Greedy and Lazy Match
Greedy quantifiers will match their preceding elements as much as possible to return the highest possible match while non-greedy quantifiers will match as little as possible to return the lowest number of possible macthes.  We talk of greedy for non-greedy (i.e. lazy) quantifiers as providing us with the longest or shortest match.  

### Boundaries

A Word Boundry is a position between `/w` and `/W` or at the begining or end of a string if it begins or ends with a work character.  

### Back-references

Back References are regular expression commands which refer to a previous part of the matched regular expression.  Back References atre specified with a back-slash and a single digit such as, `/1`.  The part of the regular expression they refer to is called a subexpression and is denoted with parentheses.  

### Look-ahead and Look-behind
Lookahead is positive and negtative (i.e. lookbehind).  They define patterns that only match when they are followed or not followed by another pattern.  

## Author

This tutorial was written by Michael Mikelic
</br>
[Github](https://michaelmikelic.github.io/regex-tutorial/)
</br>
[LinkedIn](https://www.linkedin.com/in/mmikelic/)
