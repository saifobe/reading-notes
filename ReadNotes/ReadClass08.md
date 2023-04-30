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
