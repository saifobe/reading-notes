# Lists Comprehensions in Python
## What is List Comprehensions?
List comprehensions provide a concise way to create lists. It consists of brackets containing an expression followed by a for clause, then zero or more for or if clauses. The expressions can be anything, meaning you can put in all kinds of objects in lists.
## How to use List Comprehensions?
The list comprehension starts with a ‘[‘ and ‘]’, square brackets, to help you remember that the result is going to be a list.
The basic syntax uses square brackets.

```python
new_list = [expression for_loop_one_or_more conditions]
```
The expression is what you want to have in your new list, the for loop is what you are iterating over. You can add multiple conditions.
The easiest way to remember list comprehensions is to read the first part of the expression backwards.
```python
new_range = [i * i for i in range(5) if i % 2 == 0]
```
* Result: [0, 4, 16]
* Example: Create a simple list
```python
x = [i for i in range(10)]
print x
```
* Result: [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]
* Example: Create a list using loops and list comprehension
```python
>>> x = [i**2 for i in range(10) if i > 5]
>>> x
[36, 49, 64, 81]
```
* Example: Multiplying parts of a list
```python
>>> vec = [[1,2,3], [4,5,6], [7,8,9]]
>>> [num for elem in vec for num in elem]
[1, 2, 3, 4, 5, 6, 7, 8, 9]
```
* Example: Show the first letter of each word
```python
>>> words = ['The', 'quick', 'brown', 'fox', 'jumps', 'over', 'the', 'lazy', 'dog']
>>> [w[0] for w in words]
['T', 'q', 'b', 'f', 'j', 'o', 't', 'l', 'd']
```
* Example: Lower/Upper case converter
```python
>>> [x.lower() for x in ["A","B","C"]]
['a', 'b', 'c']
>>> [x.upper() for x in ["a","b","c"]]
['A', 'B', 'C']
```
* Example: Print numbers only from a given string
```python
>>> string = "Hello 12345 World"
>>> numbers = [x for x in string if x.isdigit()]
>>> print numbers
['1', '2', '3', '4', '5']
```
* Example: Parsing a file using list comprehension
```python
>>> with open('file.txt') as f:
...     lines = [line.strip() for line in f]
```
* Example: Using list comprehension in functions
```python
>>> def double(x):
...     return x*2
...
>>> [double(x) for x in range(10)]
[0, 2, 4, 6, 8, 10, 12, 14, 16, 18]
```
* Example: Show the first letter of each word using list comprehension
```python
>>> words = ['The', 'quick', 'brown', 'fox', 'jumps', 'over', 'the', 'lazy', 'dog']
>>> [word[0] for word in words]
['T', 'q', 'b', 'f', 'j', 'o', 't', 'l', 'd']
```

## References
* [Python List Comprehension](https://www.pythonforbeginners.com/basics/list-comprehensions-in-python)
* [Python List Comprehension](https://www.programiz.com/python-programming/list-comprehension)
* [Python List Comprehension](https://www.w3schools.com/python/python_lists_comprehension.asp)
* [Python List Comprehension](https://www.geeksforgeeks.org/python-list-comprehension/)
* [Python List Comprehension](https://www.datacamp.com/community/tutorials/python-list-comprehension)
* [Python List Comprehension](https://www.python-course.eu/python3_list_comprehension.php)

## Things I want to know more about
* I want to know more about Python List Comprehension

### Auther : Saif Obeidat

