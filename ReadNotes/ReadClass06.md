# Random Module 
## What is Random Module in Python
The random module provides access to functions that support many operations. Not all of the functions are accessible to the simple import statement, however. Some functions are accessible through the random.Random class. This class is based on a version of the Mersenne Twister algorithm. It generates pseudo-random numbers that can be used for simulations, testing, security, and gaming. The random module is also useful for shuffling a deck of cards in a card game or picking a random name from a list of names for a contest winner.
## How to use Random Module in Python
### 1. Random Number
The random module contains a function called random() that generates a random number between 0.0 and 1.0. The function returns a floating-point number. To generate a random integer, you can multiply the random number by the highest number you want, then round it down to the nearest integer using the built-in int function.
```python
import random
for i in range(10):
    x = random.random()
    print(x)
```
### 2. Random Choice
The random module contains a function called choice() that takes a sequence as an argument and returns a random element from the sequence. The choice function can be used to choose a random element from a list.
```python   
import random
t = [1, 2, 3]
print(random.choice(t))

input = [1,2,3]
output = 1 || 2 || 3
```
### 3. Random Shuffle
The random module contains a function called shuffle() that takes a list as an argument and returns a random permutation of the list. The shuffle function modifies the original list. If you want to keep the original list, you can make a copy before shuffling.
```python
import random
t = [1, 2, 3]
random.shuffle(t)
print(t)

input = [1,2,3]
output = [2,3,1] || [3,1,2] || [1,3,2]
```
### 4. Random Sample
The random module contains a function called sample() that takes a list and a number as arguments and returns a new list with the given number of random elements from the original list. The sample function does not modify the original list.
```python
import random
t = [1, 2, 3]
print(random.sample(t, 2))

input = [1,2,3]
output = [1,2] || [2,3] 
```
### 5. Random Seed
The random module contains a function called seed() that takes an integer as an argument and initializes the random number generator with that integer. If you call the seed function with the same integer, it generates the same sequence of random numbers. If you don’t provide an argument, it uses the current system time as a seed.
```python
import random
random.seed(17)
for i in range(10):
    print(random.random())

```
### 6. Random Randint
The random module contains a function called randint() that takes the parameters low and high, and returns an integer between low and high (including both).
```python
import random
for i in range(10):
    print(random.randint(5, 10))
```
### 7. Random Randrange
The random module contains a function called randrange() that takes parameters similar to those of randint(), and returns a random integer chosen from the given range.
```python
import random
for i in range(10):
    print(random.randrange(0, 101, 2))
```
### 8. Random Uniform
The random module contains a function called uniform() that takes parameters low and high and returns a floating-point number between low and high (including both).
```python   
import random
for i in range(10):
    print(random.uniform(0, 1))
```

# Risk Analysis in Software Testing
## What is Risk Analysis in Software Testing?
 
 risk analysis is a process of identifying the risks associated with the project and then analyzing the probability of the risk occurring and the impact of the risk on the project.

## Why do we need Risk Analysis in Software Testing?
     
     The risk analysis process is used to identify the risks and then to analyze the risks and then to plan for the risk mitigation. 

## What are the types of Risk Analysis in Software Testing?
### 1. Qualitative Risk Analysis
Qualitative risk analysis is a process of identifying the risks and then analyzing the risks based on the experience of the tester. The tester uses his experience to analyze the risks and then to plan for the risk mitigation. The qualitative risk analysis is a simple process and it i
### 2. Quantitative Risk Analysis
Quantitative risk analysis is a process of identifying the risks and then analyzing the risks based on the probability of the risk occurring and the impact of the risk on the project. The tester uses the probability and impact of the risk to analyze the risks and then to plan for the risk mitigation. The quantitative risk analysis is a complex process and it is used when the project is large and complex.

## What are the steps involved in Risk Analysis in Software Testing?
### 1. Identify the risks
The first step in the risk analysis process is to identify the risks associated with the project. The risks can be identified by the tester or by the project manager. The risks can be identified by the brainstorming session or by the risk identification tools. The risks can be identified by the risk identification checklist.
### 2. Analyze the risks
The second step in the risk analysis process is to analyze the risks. The risks can be analyzed by the qualitative risk analysis or by the quantitative risk analysis. The risks can be analyzed by the experience of the tester or by the probability and impact of the risk on the project.
### 3. Plan for the risk mitigation
The third step in the risk analysis process is to plan for the risk mitigation. The risks can be mitigated by the risk mitigation strategies. The risks can be mitigated by the risk mitigation checklist. The risks can be mitigated by the risk mitigation plan.








