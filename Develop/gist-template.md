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
Quantifiers specify how many instances of a character, group, or of a character class that must be present in that input for a match to be found.  

### OR Operator

### Character Classes

### Flags

### Grouping and Capturing

### Bracket Expressions

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

This tutorial was written by Michael Mikelic
</br>
[Github](https://michaelmikelic.github.io/regex-tutorial/)
</br>
[LinkedIn](https://www.linkedin.com/in/mmikelic/)
