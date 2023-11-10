# Regex (Regular Expressions)
Regex, which is short for Regular Expressions is a sequence of characters (basic and special) that identifies a match in a pattern in text. Regex is used to describe a pattern and find or validate strings.

## Summary

This is the regex example I will be using which matches a URL.

    /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/

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
 * Anchors are used to make sure that a regex matches a string or a pattern. So it makes sure that the text matches the string or pattern at either the beginning or the end of a string, line, or non-word boundary.
 * The anchors are ^ and $.

In the example, 

    /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/

the caret (^) is used to match the beginning of the above string and the dollar sign ($) matches the end of the string. 
### Quantifiers
* A quantifier is used to specify the number of times a character or expression is able to repeat itself. The quantifiers are *, +, ?, and {}.
    * The asterik (*) means that the character (or expression) is allowed to be used zero or more times. So the character doesn't have a minimum or maximum. 
    * The plus sign (+) is used to specify that the preceding character must be used one or more times. So the character must be used at least once.
    * The question mark (?) is used to specify that the preceding character is not required. It is an optional character.
    * The curly braces ({}) are used to let us know that the preceding character needs to be used n amount of times. 

For example, 

    /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/

the curly braces ({}) are used to let us know that the character needs to be used 2 to 6 times. For {n, m}, which are known as non-negatives, n ≤ m. This quanitfier is letting us know that the character must match at least n times and must be used at most m times. 
In the example above, we can also see the question mark ? at the beginning and end and the plus sign + in the middle. 

### OR Operator
* The OR Operator is used to match a specific character. * The symbol is a pipe (|). An example of this is shown below from a hex value. 
        Hex Value – /^#?([a-f0-9]{6}|[a-f0-9]{3})$/
the OR operator is in the middle. 

In our example, 
    /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/
the OR operator | is not shown, however, by using [a-z\.], it is letting us know that the character can be anything a-z or a period. 
### Character Classes
* Character classes most used are /d, /w, and /s. 
    * /d is used for any single digit 0-9.
    * /w stands for word, and it is used for any character that is letter, number, or underscore. 
    * /s stands for space and it can be used for tabs (/t), newlines (/n) and spaces (/s).

* We see the /w in the example near the end. So it is telling us that the character can be a word, number, or underscore.
    Code Snippet Example: ([\/\w \.-]*)*\/?$/
### Flags
* Flags in regex are an optional parameter. The flags modify the search and they are known as i (ignore casing), g (global), and m (multiline). 

* i = ignore casing. This means that the search is not case sensitive.
* g = global. This means the search will look for all instances.
* m = multiline. This means that instead of searching for a match in the string, the searcch will look for a match in each line.
### Grouping and Capturing
* Grouping and capturing is used to group multiple characters as a single unit.
* It is shown by using parentheses () and placing the characters that will be grouped inside of the parentheses.
* This is helpful when we want to simplify the regex. 

In the example, 

    /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/

it is shown that (https?:\/\/) are grouped together.The other two instances are ([\da-z\.-]+) and ([\/\w \.-]*). 
### Bracket Expressions
* Bracket expressions are shown within a set of brackets [] and they are used to match a specific character or expression. 

In the example, 

    [\da-z\.-]

In the brackets is [\da-z\.-]. So the character can be a digit, a-z, a period, or a dash.
### Greedy and Lazy Match
* Greedy is used to look for as many matches as possible in the string and the longest.
*  Lazy is used to search for as few matches as possible. 
* An example would be /<.+>/g and /<.+?>/g where the fist is the greedy and the second is the lazy match. 
### Boundaries
* A boundary matches a position in the string. One side is a word character (a letter, number, or underscore) and the other is a non-word character.
* The boundary is \b.
### Back-references
* A Back Reference is used to match a previous section of the matched string or expression. It is shown with a backslash (\) and a single digit. 

* The back reference refers to an already captured group.
### Look-ahead and Look-behind
* (?=string) this is an example of a back reference. Here itis telling us that it will look ahead and what follows the equal sign is what it will look for and match.

* (?<=string) this is also an example of a back reference. Here it is telling us that what precedes the position is the string that will be matched.
## Contributions/Credits 
* “Anchors - Launchschool.Com.” Launchschool, launchschool.com/books/regex/read/anchors. Accessed 8 Nov. 2023. 
* “Character Classes.” The Modern JavaScript Tutorial, 12 Dec. 2021, javascript.info/regexp-character-classes#:~:text=A%20character%20class%20is%20a,to%20%E2%80%9Cany%20single%20digit%E2%80%9D.&amp;text=Without%20the%20flag%20g%20%2C%20the,is%20the%20first%20digit%20%5Cd%20. 
* “Flags - Javascript Regexp.” CodeGuage, www.codeguage.com/courses/regexp/flags#:~:text=A%20flag%20is%20an%20optional,a%20single%20lowercase%20alphabetic%20character. Accessed 9 Nov. 2023. 
* NALSengineering, Nguyen Thanh Minh. “Regular Expression for Dummies. Part 1: Quantifiers.” Medium, Medium, 27 Sept. 2023, medium.com/@NALSengineering/regular-expression-for-dummies-25e5c83c72f0. 
## Author
This was created by Madeline Kovanda. 

Contact Information:
* [GitHub](https://github.com/M-deline)

* [LinkedIn](https://www.linkedin.com/in/madeline-kovanda-22399627b/)

* [Email Me](mailto:madkovanda@gmail.com)



