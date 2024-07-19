# Regex Tutorial:Explaining a Specific Regular Expression

Regular expressions are powerful tools for finding patterns in strings. They are commonly used in programming for tasks like validation, searching, and text manipulation. Knowing regex is essential for web developers because it helps with efficient data handling and validation.


## Summary
In this tutorial, we'll use password formatting as an example, although regex can be applied to many other tasks. When creating a password, certain criteria may need to be met. In this case, we'll require:

A minimum of 6 characters
A maximum of 16 characters
Lowercase letters (a-z)
Uppercase letters (A-Z)
Numbers
Some special characters
Our regex for this will be:

/^[a-zA-Z0-9!@#$%^&*()_-]{6,16}$/


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
Anchors, also called assertions, are used to signify the beginning and end of the expression. They are used to add structure and precision to the expression by limiting the acceptable threshold of matching.
The anchors in the matching an email regex are ^ and $.

The ^ signifies the beginning of the string, where all the characters that follow it must fit within the upcoming parameters (which we will get to).

The $ signifies the end of the string, where all the characters that precede it must fit within the parameters declared.

Effectively, the anchors comprise the bookends of the string, ensuring the parameters within the email match the criteria exactly.

### Quantifiers

Quantifiers allow us to define the length of a string. For example, we might want to limit a phone number to 10 digits or, in our case, set the length of a password. Quantifiers match the specified number of preceding tokens. They often include a minimum and maximum range, separated by a comma. In our example, we want at least 6 characters and no more than 16, indicated by wrapping the quantifier in {}. There are other ways to set limits on the string you want to match with your regex:

* matches the pattern 0 or more times
+ matches the pattern one or more times
? matches the pattern zero or one time

Curly brackets can also specify different limits. Using one number inside brackets matches the pattern exactly that many times. Adding a comma after the number sets that value as the minimum.

### Grouping Constructs
Grouping constructs are also not used in this specific match an email regex, but they are commonly found in regexes as a whole. Parentheses ( ) are the main syntax for grouping and are used to group strings in what is called a subexpression.

The purpose of subexpressions is to search for the specific string that is contained within the parentheses.



### Bracket Expressions
Bracket expressions are essential for matching an email regex and are indicated by square brackets [ ]. The characters within these brackets define the range of characters the regex aims to match. For example:

[a-zA-Z0-9+_.-] and [a-zA-Z0-9.-].

Bracket expressions are relatively straightforward compared to other regex components, as they explicitly define the character ranges within the brackets.

The first part of the regex looks for any lowercase or uppercase letter (a-z, A-Z), any digit (0-9), and also allows the characters +, _, ., and -.

The second part of the regex is similar but allows fewer characters. It matches any lowercase or uppercase letter (a-z, A-Z), any digit (0-9), and the characters . and -. This section, following the @ symbol, represents the "organization.com" part of the email address, which is why it permits fewer characters than the first section.

### Character Classes
Characters are characterized by various classes. These indicators we use for classes are case sensitive.

\d represents any numerical digit between 0 and 9

.* represents a wild card, or any character

\w represents any alphanumerical character, so anything uppercase or lowercase from a-z and any number from 0-9.

\s represents any white space

. matches any character

\W represents anything that is not a word character, so the inverse of \w.

\S is also inverse, representing anything that is not a space


### The OR Operator
There are no OR operators in this regex. The OR operator, |, is used to add flexibility into grouping constructs and bracket expressions.


### Flags
Flags are added at the end of the regex, after the second slash, to define additional properties for the regex.

'i' ignores the case of letters during matching.

'g' searches globally to find all possible matches.

'm' enables multi-line searching.

Less commonly used flags include:

's' enables single line (dotall) mode.

'u' allows for Unicode matching.

'y' enables sticky searching.

### Character Escapes
A character escape, marked by a \ within the expression, instructs the regex to treat a special character as a literal character. However, this regex does not contain any character escapes.

## Author
Rachel Gyarko is a Full Stack Developer and a BSN Nursing student. She is enthusiastic about ongoing personal and professional growth and development.









