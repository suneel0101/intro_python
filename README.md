# Objective
Get you guys a solid foundation in Python, which is useful if you want to build for the web or do any machine learning or data science.

# Instructor
name - Suneel Chakravorty

email - chakravorty@post.harvard.edu

# What do you need?
- Terminal for Mac users, Command Prompt for Windows users
- the python command

# The Basic Data Types
What are the basic data types?
- Integers, e.g. 1, 2, 3
- Floating point numbers, e.g 2.3, 3.7
- String, e.g. "John Krasinski"
- bool, True or False
- None, which just corresponds to empty or null, if you've used other languages

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

What's the difference between 2.0 and 2?
```python
>>> 7/2
3
>>> 7/2.0
3.5
```
Practice question - try these out in the shell:
```
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

Explanations:
```
In 1., we learned that you can chain operations
In 2 and 3, we learned that order matters and you can use parentheses to indicate the order, as part of the usual mathematical order of operations.
In 4 and 5, we learned about the equality operator.
In 6 and 7, we learned about inequality comparions like less than or greater than equal to.
In 8 and 9, we learned about the not-equal-to operator.
```

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

Practice question:
Given x=10, y=2, predict the answers to the following and then try them out in the shell:
```
1. x + y
2. x * y
3. (x + 7) / y
4. (x + 7.0) / y
5. x == y
6. x != y
```

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
Last stop on our journey into basic data types: Strings
A string is a sequence of characters, for example "Hello" or "My id # is 1235!"
Let's try a few in our shell:
```python
>>> "Hello World!"
Hello World!
>>> "Hello" + " World!"
>>> 1 + "world"
```

Practice problem:
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

Practice problem:
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

Let's learn about slicing:
```python
>>> y = [1, 2, 3, 4, 5, 6, 7, 8]
>>> y[2:]
>>> y[:4]
>>> y[1:3]
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
>>> person["deepest_darkest_secret"] = "Loves Vampire Diaries"
print person
>>> del person["deepest_darkest_secret"]
print person
>>> person.keys()
>>> person.values()
>>> person.items()
>>> # check if a key exists in the dictionary
>>> "name" in person
>>> "secret" in person
```
Practice problem:
```
Create a dictionary called `class_data` with the following keys:
- "course_name", which should correspond to "Intro to Python"
- "student_count", which should correspond to number of students, say 20
- "instructor", which should itself be a dictionary with the following keys
    - "name" ("Suneel")
    - "gender" ("M")
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

Practice problem:
```
Given x = "John Jameson",
- Construct an if else statement according to this logic: if "John" is in x, print "John is in x", otherwise print "John is not in x"
- Construct an if/elif/else statement according to this logic: if "roger" is in x, print "Hi Roger!", elif the length of x is greater than 20, print "thats a long string", else print "Oh well!"
```

# Loops
Loops let us pass through a set of values and do some operation on each.
There are different kinds of loops, for loops and while loops. They're quite similar, but let's look at the canonical loop, the for loop.

```python
>>> numbers = [1, 2, 8, 7, 9, 10]
>>> odds = []
>>> for number in numbers:
        if number % 2:
            odds.append(number)

print odds
```
- the `number` in the for loop syntax is a dummy variable that refers to the element in the list that we're passing through. The first time around, number refers to 1, the last time it refers to 10.
- we are going through this list and if the number is odd, we add it to the odds list that we initialized before the for loop.

Before we move on to some practice problems, here is a useful function:
```python
>>> range(10)
```

Practice problems:
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
```

Let's write a function that takes a variable, which is a list of numbers, and then returns just the ones that are divisible by 33.

```python
def div_by_33(numbers):
    by_33 = []
    for number in numbers:
        if number % 33 == 0:
            by_33.append(number)
    return by_33
```

Practice problem: Write a function that takes a list of numbers and retursn True if the sum of the numbers is even and False otherwise.

# 'Real-life' problem: Restaurant Recommendation Engine
- figuring out where to eat lunch everyday is annoying
- let's automate it
- First version is going to be given a list of restaurants, randomly pop out a recommendation until the list is depleted

Let's learn about the random library, a pretty useful builtin python library:
```python
>>> import random # this is how we make accessible the random library code
>>> numbers = [1, 3, 5, 6, 7]
>>> shuffled = random.shuffle(numbers)
>>> for number in shuffled:
        print number.pop()
```

Problem 1:
```
Given a list of restaurants,
["Laut", "Random String", "Chipotle", "Eataly", "Sophie's Cuban", "Chop't", "Potbelly's"]

Write a function that takes the list of restaurants, shuffles the list,
and one by one pops out a restaurant as a recommendation.
```

What happens when we deplete the list and need to recommend again, let's go by the following algorithm:
- Each time, randomly recommend a restaurant from the list that has not been recommended in the last 4 tries

We're going to create a file called recommender.py and type the below in there.

```python
import random

# Keep track of the recommendations
recommendation_history = []
restaurants = ["Laut", "Random String", "Chipotle", "Eataly", "Sophie's Cuban", "Chop't", "Potbelly's"]

def recommend(restaurants):
    random.shuffle(restaurants)
    for choice in restaurants:
        if choice not in recommendation_history[-1: -4]:
            return choice
```

# Useful python libraries to know
- random
- math
- datetime
- collections
- csv

# Crazy cool python libraries to know
- pandas
- nlptoolkit

# So many cool things you can do with python
- AI/ Machine learning/ Natural language processing
- Web development
- Data science

# What's next?
- Web development: [Django](http://djangoproject.com) or [Flask](http://flask.pocoo.org/)
- Data science: [pandas](http://pandas.pydata.org/)
- Tutorial: [Learn Python the Hard Way](http://learnpythonthehardway.org/book/)
- Practice problems: [Project Euler](https://projecteuler.net/)
- More GA: [Advanced Python class on Oct 20](https://generalassemb.ly/education/advanced-python-workshop/new-york-city/8151)
