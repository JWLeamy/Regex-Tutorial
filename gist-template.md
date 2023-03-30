# What is a Regex?

A regex (short for regular expression) is a sequence of Meta Characters used to describe a search pattern. </br>

Meta characters are simply characters that do not indicate a single literal character, but instead indicates a more generalized pattern.</br>

In other words, a Regex is just a mega-amplified version of a command F search.

## Summary
The following statement is an example of a regex.
```

 /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/ 
 ```
 This particular regex is designed to search for URL links within a given body of text. 
 </br> </br> USES: lets say we are given a list that contains thousands of different words and characters. Somewhere within that list however, there are 5 unique URL's we are trying to find. Rather than scanning through each item on the list, 
 we would use this particular Regex to identify a list item that meets our searchpattern (in this case - find a URL)

 NOTE: It is neccesaryy to wrap any and all regular expressions within slash marks (/). The slash marks denote the start and finish of a Regex, and all characters within the two symbols are cosidered 'Components'.


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
A regex statement has two types of anchors <br>

- ```^``` the starting anchor <br> 
- ``` $ ``` the closing anchor <br>

Don't overthink the anchors - anything within these two anchors will help actually classify the value/pattern your regex is trying to identify, but the anchors themselves simply act as a starting/stopping point.

In our example, we see that aside from our slash marks that capture the regex, it starts with a ^ and end with a $
```
 /^(https?:\/\/)?([\da-z\.-]+)\.([a-z\.]{2,6})([\/\w \.-]*)*\/?$/ 
 ```


### Quantifiers
Quantifiers will set the character limit on a specific string your regex is trying to identify. More specifically, it will force your regex statement to match the quanityity of the leftmost expression. 
- *and *?  Matches Zero or more times.
- +and +?  Matches One or more times.
- ? and ??  Matches Zero or One times.
- {n} and {n}?  Matches exactly n times.
- {n,} and {n,}?   Matches atleast n times.
- {n,m} and {n,m}?  Matches from n to m times.

When we break down our own exmaple regex, we find the following
```
https?          `?` Matches 'https' or 'http' once. 
[\da-z\.-]+     `+` it matches a single digit, group of letters (a-z), dot (.) or hyphen (-) 1 or more times
[a-z\.]{2,6}    `{2,6}` it matches 2 to 6 copies of the sequence [a-z\.]
[\/\w \.-]*     `*` it matches '/', '.', '-', 'www', '//'
```


### OR Operator
The OR Operator ```|``` allows us to specificy specific characters even further than character classes.
### Character Classes
Character classes help define sepecifics sets of characters for our regex statement to follow. Some common character classes include

```.``` —Matches any character except the newline character ```\n```

```\d``` —Matches any Arabic numeral digit. This class is equivalent to the bracket expression ```[0-9]```.

```\w``` —Matches any alphanumeric character from the basic Latin alphabet, including the underscore (_). This class is equivalent to the bracket expression ```[A-Za-z0-9_]```.


```\s``` —Matches a single whitespace character, including tabs and line breaks

<br> 
If we look at our example URL regex, we use multiple character classes to help fufill certain pattern recognition requirements. <br>

/^(https?:\/\/)?([``\d``a-z\.-]+)\.([a-z\.]{2,6})([\/```\w``` \.-]*)*\/?$/ 



### Flags
The only time that you will ever add a character OUTSIDE you starting and closing slash marks (/) is for flag use. A flag can define additional functionality and limitation to the regex when added to the right of your closing slash mark. Some common flags are
<br>

```g```—Global search: the regex should be tested against all possible matches in a string.

```i```—Case-insensitive search: case should be ignored while attempting a match in a string

```m```—Multi-line search: a multi-line input string should be treated as multiple lines
### Grouping and Capturing
Grouping and capturing within a Regex is as stragihtforward as it sounds. Using parenthises ``()``, we are simply organzing our code into shorter blocks or 'subexpressions' that make it easier to form search criteria.
<br>
If we take a look at our example Regex, we will find the following constucted groups.
```
(https?:\/\/)     Indicates that the desired search must start with either "http://"or "https://"
([\da-z\.-]+)     This gorup indicates that the search must match 1 or more numbers, letters, dots or hypens. (this connects to the next subexpression using +)
([a-z\.]{2,6})    Matches 2-6 copies of the sequences "[a-z\.]"
([\/\w \.-]*)     This group is is being matched as many times as they want because of the "*" at the end. Basicallly acting like multiple directories. (refer back to Group project 2).
```

### Bracket Expressions
The content within a Bracket Expression ```[]```, classifies the range of characters the expression is trying to both match & include. 

The bracket expression below exists in our example URL regex, and provides a solid idea on how to use bracket expressions & character classes effectively.
```
[\da-z\.-]    This full bracket expression describes a number (\d), lowercase letters (a-z), a dot (.), or hyphen (-)
```

### Greedy and Lazy Match
The terms 'Greedy' and 'Lazy' are simple ways of classifing the type of quantifier that is used after a regex sequence. A greedy quanitfier, signified by a ```+```, matches as many items as possible to the attached search. 

<br> 

The lazy quantifier, denoted by a ```?```, matches the least amount of items posible. 

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)