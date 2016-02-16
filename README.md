# Objective
Give students a solid foundation in Python, which they can use to build for the web or do data science, data analytics and beyond.

# Why Python?
Let's discuss.

# Where We'll Code
Open this link in the browser: [Repl.it](https://repl.it/languages/python3)

# The Basic Data Types
What are the basic data types?
- Integers, e.g. 1, 2, 3
- Floating point numbers, e.g 2.3, 3.7
- String, e.g. "John Krasinski"
- bool, True or False
- None, which just corresponds to empty or null, if you've used other languages

# Numerical Data
Let's start with integers and floats.

Let's go into the python shell.
To do this, open up your terminal and type 'python' and then press Enter.

We can do math in the shell.
```python
>>> 2 + 2
4
>>> 2 * 3.5
7.0
>>>
```

## Practice question - try these out in the shell:
```python
1. 2 * 7 * 3.5
2. 3 + 5 - (2 * 6)
3. (3 + 5 - 2) * 6
4. 4 == 5
5. 5 == 5
6. 4 < 5
7. 5 >= 4
8. 9 != 9
9. 8 != 9
```

# Variables
Now let's talk variables. What's a variable? It's a placeholder for a value.
```python
>>> x = 5
>>> y = 2
>>> x + y
7
>>> x = 3
>>> x + y
5
```

# Assignment vs Equality Check

```python
>>> x = 2
>>> x == 5
>>> x = 5
```

# Boolean: True or False
Now let's talk about Booleans.
Simply put, a boolean variable is either True or False, and every python object or data has a boolean value.
We can find out what the true-false value is by using bool()

Let's try it out:
```python
>>> bool(False)
False
>>> bool(True)
True
>>> bool(0)
False
>>> bool(7)
True
>>> bool(None)
False
>>> bool(7 == 0)
False
>>> 7 == 0
False
```

# Strings
Last stop on our journey into basic data types: Strings
A string is a sequence of characters, for example "Hello" or "My id # is 1235!"
Let's try a few in our shell:
```python
>>> "Hello World!"
Hello World!
>>> "Hello" + " World!"
>>> 1 + "world"
```

# Practice problem
```
- Set a variable called `name` equal to your full name.
- Set a variable called `first_name` equal to your first name.
- Set a variable called `last_name` equal to your last name.
- Then combine `first_name` and `last_name` so that it equals your full name, and save this in a variable called `full_name`.
- Prove using the == operator that they are equal.
```

# Lists
Lists is a super useful data type.
It's an ordered collection of items, which you can modify by adding or removing elements.

Let's learn the syntax of a list:
```python
>>> x = [1, 2, 3, 4, 5]
>>> len(x)
5
>>> # what's between the brackets is called the index
>>> x[0]
1
>>> x[1]
2
>>> x[4]
5
>>> x[6]
IndexError
>>> x.append("hello")
>>> len(x)
6
>>> x[5]
"Hello"
>>> # can remove elements, defaults to popping off the last one
>>> x.pop()
>>> print x
>>> # can specify the index
>> x.pop(2)
>>> print x
>>> # can do a boolean check if something is in the list
>>> 5 in x
False
>>> 1 in x
```

# Practice problem
```
- Create a list called `restaurants` consisting of the following elements in this order:
"Laut", "Random String", "Chipotle", "Eataly", "Sophie's Cuban", "Chop't", "Potbelly's"
- Get the third element of the list
- Add "Ootoya" to the end of the list
- Use .pop() to remove "Random String" from the list
- Print the list
- Check if 'Chipotle' is in the list
- Check if 'Random String' is in the list
- Get the length of the list
```

# Dictionaries
Dictionaries are also massively useful. You can think of them as maps, between as set of keys and their corresponding values.
Let's look at one in the shell to better understand how they work and how they can be useful:

```python
>>> # Here's the syntax, {} with key:value, with key being a string.
>>> person = {"name": "John Jameson", "age": 31, "hobbies": ["tennis", "python", "piano"]}
>>> person["name"]
>>> # like a string, we use the brackets but instead of the index, we provide the key name
>>> person["age"]
>>> hobbies = person["hobbies"]
>>> len(hobbies)
>>> hobbies[1]
>>> person["random"]
KeyError
>>> person["location"] = "New York"
>>> person["hometown"] = "Jupiter, Florida"
print person
>>> del person["hometown"]
print person
>>> person.keys()
>>> person.values()
>>> person.items()
>>> # check if a key exists in the dictionary
>>> "name" in person
>>> "secret" in person
```

# Practice problem
```
Create a dictionary called `class_data` with the following keys:
- "course_name", which should correspond to "Betaworks Intro to Python"
- "student_count", which should correspond to number of students, say 20
- "instructor", which should itself be a dictionary with the following keys
    - "name" ("Suneel")
    - "can_program" (True)
- get the student count from the dictionary
- get the instructor name from the dictionary
```

# If/Else
If/else statements are blocks of our code that allow us to do different things based on some logical condition
Let's learn the syntax, note INDENTATION is important:
```python
>>> x = 5
>>> if x > 4:
        print "Hello"
    else:
        print "World"
Hello
>>> if x < 5:
        print "Less than five"
    else:
        print "Greater than or equal to five"
>>> if x == 1 or x == 2:
        print "Ha"
    elif x == 3:
        print "Hey"
    else:
        print "Hi"
```

# Practice problem:
```
Given x = "John Adams",
- Construct an if else statement according to this logic: if "John" is in x, print "John is in x", otherwise print "John is not in x"
- Construct an if/elif/else statement according to this logic: if "roger" is in x, print "Hi Roger!", elif the length of x is greater than 20, print "thats a long string", else print "Oh well!"
```

# Loops
Loops let us pass through a set of values and do some operation on each.
There are different kinds of loops, for loops and while loops. They're quite similar, but let's look at the canonical loop, the for loop.

```python
>>> numbers = [1, 2, 8, 7, 9, 10]
>>> odds = []
>>> for zebra in numbers:
        if zebra % 2 == 1:
            odds.append(zebra)

print odds
```
- the `number` in the for loop syntax is a dummy variable that refers to the element in the list that we're passing through. The first time around, number refers to 1, the last time it refers to 10.
- we are going through this list and if the number is odd, we add it to the odds list that we initialized before the for loop.

Before we move on to some practice problems, here is a useful function:
```python
>>> range(10)
```

# Practice problems
```
- Construct a list of numbers between 0 and 1000 that are divisible by 33
- Given the following list
["Donald Duck", "Mickey Mouse", "Daffy Duck", "Goofy", "Minnie Mouse", "Pluto"]
Get the sum of all of the lengths of these strings.
- Given the above list, create a list of all of the elements that have the letter "d" or the letter "m" in them
```

# Functions
Functions are the heart and soul of python. Functions are blocks of code that take an input and based on some rules produce an output.

Let's learn the syntax of functions:

```python
>>> def add(a, b):
        return a + b
>>> z = add(3, 4)
>>> print z
```
a and b are variables that the function `add` takes

Practice problems:
```
- create function `multiply` that takes two variables and returns their product
- create function `subtract` that takes two variables and returns their difference
- write a function that takes a variable, which is a list of numbers, and then returns just the ones that are divisible by 33.
- write a function that takes a list of numbers and returns True if the sum of the numbers is even and False otherwise.
```

# Using Other Libraries
What is a library? A reusable, collection of code that someone else (or you) has already written. Some great built-in libraries:
- `random`
- `csv`
- `collections`
- `datetime`

To use other libraries, we need to be able to:
- understand the documentation of that library
- understand what the inputs and outputs of their functions are
- how to call those functions correctly

Let's start with the random library.

## The `random` library.
Our first step is to locate the documentation. Google "python random". It should take you [here](https://docs.python.org/2/library/random.html)

Let's import the library
```python
>>> import random
>>> dir(random)
```

How does python know what `random` is and how to find the code? Because it comes built-in to the Python language. Other libraries such as `pandas` will have to be installed prior to use.

### Exercises
1. Find the `randint` function in the documentation and explain to your neighbor what it does and how to use it.
2. Again, with your partner, use the `randint` function to generate a random number between 1 and 125.


# What's next?
- Web development: [Django](http://djangoproject.com) or [Flask](http://flask.pocoo.org/)
- Data science: [pandas](http://pandas.pydata.org/)
- Tutorial: [Learn Python the Hard Way](http://learnpythonthehardway.org/book/)
- [Practice problems with full solutions](https://github.com/suneel0101/python-powerup)
- Practice problems: [Project Euler](https://projecteuler.net/)