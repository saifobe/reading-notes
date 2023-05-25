# Regular Expressions
- A regular expression is a sequence of characters that forms a search pattern.
- When you search for data in a text, you can use this search pattern to describe what you are searching for.
- A regular expression can be a single character, or a more complicated pattern.
- Regular expressions can be used to perform all types of text search and text replace operations.
- A regular expression is a sequence of characters that forms a search pattern.
- When you search for data in a text, you can use this search pattern to describe what you are searching for.


# Regex Tutorial
- https://regexone.com/
- https://regexr.com/
- https://www.regular-expressions.info/tutorial.html
- https://www.rexegg.com/regex-quickstart.html


### In Python, regular expressions are supported by the re module. That means that if you want to start using them in your Python scripts, you have to import this module with the help of import:
```python
import re
```
### Basic Patterns: Ordinary Characters
- You can easily tackle many basic patterns in Python using ordinary characters, for example to search for a single character 'a' in a string, or for a string of characters like 'bat'.
- The regular expression pattern for a single character 'a' would just be 'a'.
- To search for a string of characters like 'bat', you simply need to write that string as it is, for example 'bat'.
- Any additional characters in the regular expression are considered ordinary characters and just 'added on' to the pattern to be matched.
- In other words, the regular expression pattern 'bat' matches all strings that contain the string 'bat', such as 'bat', 'batman', 'batter' or 'abate'.
- We can use ordinary characters to match themselves exactly or to match different characters by using metacharacters.
- Metacharacters are what make regular expressions more powerful than normal string methods.
- They allow you to create regular expressions to represent concepts like "one or more repetitions of a vowel".
- The list of metacharacters are: . ^ $ * + ? { } [ ] \ | ( )
- The metacharacter . is used to match any character (except newline).
- For example, the regular expression .at matches any three-character string ending with 'at', including 'hat', 'cat', and 'bat'.
- The regular expression ..t also matches any three-character string ending with 'at', but since there are only two characters before 't', it doesn't match 'bat'.

### Wildcard: . (Dot)
- The . metacharacter is the simplest example of a wildcard in regular expressions. It matches any single character in the place of the dot.
- For example, the regular expression .ar matches any three-character string that begins with 'a' and ends with 'r', including 'bar', 'car', and even 'aar'.
- Note that the . metacharacter does not match newline characters.

### Caret: ^ (Caret)
- The caret symbol ^ is used to check if a string starts with a certain character.
- To match any string that starts with 'Hello', you can use the regex ^Hello.
- The regular expression ^Hello matches strings that start with 'Hello', such as 'Hello, world!' and 'Hello, everybody!'.
- The regular expression ^Dear is used by the re.sub() function to replace the occurrences of 'Dear' at the beginning of the sentences with 'Hello,'.

### Dollar: $ (Dollar)
- The dollar symbol $ is used to check if a string ends with a certain character.
- To match a string that ends with 'world!' you can use the regex world!$.
- The regular expression world!$ matches the strings that end with 'world!', such as 'No one says hello world!' and 'Hello world!'.

### Star: * (Star)
- The star symbol * matches zero or more occurrences of the pattern left to it.
- For example, the regular expression a*b*c* matches zero or more occurrences of a or b or c, such as 'abc', 'ac', 'b', 'abbbc', etc.
- The star symbol can be used in three different ways with the regular expression:
- Left to a string, it matches zero or more occurrences of the given pattern.
- Right to a string, it matches zero or more occurrences of the given pattern.
- Between two characters, it matches zero or more occurrences of characters between them.

### Plus: + (Plus)
- The plus symbol + matches one or more occurrences of the pattern left to it.
- For example, the regular expression a+b+c+ matches one or more occurrences of a or b or c, such as 'abc', 'aabbbbc', etc.
- The plus symbol can be used in two different ways with the regular expression:
- Left to a string, it matches one or more occurrences of the given pattern.
- Between two characters, it matches one or more occurrences of characters between them.

### Question Mark: ? (Question Mark)
- The question mark symbol ? matches zero or one occurrence of the pattern left to it.
- For example, the regular expression ab?c matches either 'abc' or 'ac' because the b is considered optional.
- The question mark symbol can be used in two different ways with the regular expression:
- Left to a string, it matches zero or one occurrence of the given pattern.
- Between two characters, it matches zero or one occurrence of characters between them.

### Curly Braces: { } (Curly Braces)
- The curly braces { } are used to specify the number of occurrences of a character we wish to match.
- For example, the regular expression {2} matches the expression to its left two times.
- So, the regular expression {2} is equivalent to {1}{1}.
- Similarly, the regular expression {5} is equivalent to {1}{1}{1}{1}{1}.
- We can also specify a range of occurrences.
- For example, the regular expression {2,5} matches minimum two occurrences and maximum five occurrences of the pattern to its left.
- So, the regular expression {2,5} is equivalent to {2}{3}{4}{5}.
- We can also omit the first or the second number of the range to leave it unspecified.
- For example, the regular expression {,5} matches the string that has maximum five occurrences of the pattern to its left.
- So, the regular expression {,5} is equivalent to {0}{1}{2}{3}{4}{5}.
- Similarly, the regular expression {3,} matches the string that has at least three occurrences of the pattern to its left.
- So, the regular expression {3,} is equivalent to {3}{4}{5}{6}…

## Reading Questions
1- How can you use regular expressions in Python to search for specific patterns in a string, and what is the primary library to work with them?
- You can use the re module to search for specific patterns in a string.

2- What is the purpose of the shutil library in Python, and provide an example of a common use case for file or directory management with this library?
- The shutil module offers a number of high-level operations on files and collections of files. In particular, functions are provided which support file copying and removal.

3- Explain one automation idea from the assigned material and describe how it can be implemented using Python’s regular expressions and shutil libraries.
- You can use shutil to copy files from one directory to another. You can use regular expressions to search for specific patterns in a string.




