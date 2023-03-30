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

It is neccesaryy to wrap any and all regular expressions within slash marks (/). The slash marks denote the start and finish of a Regex, and all characters within the two symbols are cosidered 'Components'.

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


### OR Operator

### Character Classes
Character classes help define sepecifics sets of characters for our regex statement to follow. Some common character classes include

```.``` —Matches any character except the newline character ```\n```

```\d``` —Matches any Arabic numeral digit. This class is equivalent to the bracket expression ```[0-9]```.

```\w``` —Matches any alphanumeric character from the basic Latin alphabet, including the underscore (_). This class is equivalent to the bracket expression ```[A-Za-z0-9_]```.


```\s``` —Matches a single whitespace character, including tabs and line breaks

<br> 
If we look at our example URL regex, we use multiple character classes to help fufill certain match requirements. <br>

/^(https?:\/\/)?([``\d``a-z\.-]+)\.([a-z\.]{2,6})([\/```\w``` \.-]*)*\/?$/ 



### Flags
The only time that you will ever add a character OUTSIDE you starting and closing slash marks (/) is for flag use. A flag can define additional functionality and limitation to the regex when added to the right of your closing slash mark. Some common flags are
<br>

```g```—Global search: the regex should be tested against all possible matches in a string.

```i```—Case-insensitive search: case should be ignored while attempting a match in a string

```m```—Multi-line search: a multi-line input string should be treated as multiple lines
### Grouping and Capturing

### Bracket Expressions
The content within a Bracket Expression ```[]```, classifies the range of characters the expression is trying to both match & include. 

### Greedy and Lazy Match

### Boundaries

### Back-references

### Look-ahead and Look-behind

## Author

A short section about the author with a link to the author's GitHub profile (replace with your information and a link to your profile)
