---
title       : Welcome to the Playground!
description : Where all good Python problems come to be buried.
attachments :
  slides_link : https://s3.amazonaws.com/assets.datacamp.com/course/teach/slides_example.pdf

--- type:NormalExercise lang:python xp:100 skills:2 key:1592680f34
## Problem with Bokeh histograms

The sample code should work and produce a histogram.


*** =instructions
- 
- 

*** =hint
- 
- 

*** =pre_exercise_code
```{python}

```

*** =sample_code
```{python}
#
import pandas as pd
df = pd.read_csv('https://s3.amazonaws.com/assets.datacamp.com/production/course_1392/datasets/titanic.csv')
from bokeh.charts import Histogram, output_file, show

p = Histogram(df, values = 'Age', title="Age", color="Survived", legend="top_left")

output_file("histogram.html")

show(p)
```

*** =solution
```{python}

```

*** =sct
```{python}
success_msg("Great work!")
```

--- type:NormalExercise lang:python xp:100 skills:2 key:56a485ea45
## Problem with encoding

For some reason, the DataCamp backend doesn't like the solution code and throws an encoding error.

The weird thing is: if I remove solution code, then the same code runs fine when I submit it.

See next exercise.

*** =instructions
- 
- 

*** =hint
- 
- 

*** =pre_exercise_code
```{python}
fn = 'https://s3.amazonaws.com/assets.datacamp.com/production/course_1342/datasets/tweets.csv'
from urllib.request import urlretrieve
urlretrieve(fn, 'tweets.csv')

# Import pandas
import pandas as pd

# Import Twitter data as dataframe: dataframe
tweets_df = pd.read_csv('tweets.csv')

# Don't forget to print out an appropriate error message in the `except` block for cases when the function is called incorrectly.

```

*** =sample_code
```{python}
#
result = filter(lambda x: x[0:2] == 'RT', tweets_df['text'])

#
res_list = list(result)

#
for tweet in res_list:
    print(tweet)

```

*** =solution
```{python}
#
result = filter(lambda x: x[0:2] == 'RT', tweets_df['text'])

#
res_list = list(result)

#
for tweet in res_list:
    print(tweet)

```

*** =sct
```{python}
success_msg("Great work!")
```

--- type:NormalExercise lang:python xp:100 skills:2 key:038f1b3790
## No problem with encoding

This is exactly the same as the previous exercise, except there is NO solution code here.

The sample code runs perfectly well.

*** =instructions
- 
- 

*** =hint
- 
- 

*** =pre_exercise_code
```{python}
fn = 'https://s3.amazonaws.com/assets.datacamp.com/production/course_1342/datasets/tweets.csv'
from urllib.request import urlretrieve
urlretrieve(fn, 'tweets.csv')

# Import pandas
import pandas as pd

# Import Twitter data as dataframe: dataframe
tweets_df = pd.read_csv('tweets.csv')

# Don't forget to print out an appropriate error message in the `except` block for cases when the function is called incorrectly.

```

*** =sample_code
```{python}
#
result = filter(lambda x: x[0:2] == 'RT', tweets_df['text'])

#
res_list = list(result)

#
for tweet in res_list:
    print(tweet)

```

*** =solution
```{python}
#
```

*** =sct
```{python}
success_msg("Great work!")
```


--- type:NormalExercise lang:python xp:100 skills:2 key:bf5b161a37
## Testing test_function_v2 1

Testing `test_function_v2`
*** =instructions
- 
- 

*** =hint
- 
- 

*** =pre_exercise_code
```{python}
#PEC

```

*** =sample_code
```{python}
# This is pi
pi = 3.14159

# Round pi to 3 digits
r_pi = round(pi, 3)

```

*** =solution
```{python}
# This is pi
pi = 3.14159

# Round pi to 3 digits
r_pi = round(pi, 3)
```

*** =sct
```{python}
test_function_v2("round", params=["number", "ndigits"])
success_msg("Great job!")
```

--- type:NormalExercise lang:python xp:100 skills:2 key:c58a963dcd
## Testing test_function_v2 2

Testing `test_function_v2`
*** =instructions
- 
- 

*** =hint
- 
- 

*** =pre_exercise_code
```{python}
#PEC
fn = 'https://s3.amazonaws.com/assets.datacamp.com/production/course_998/datasets/moby_opens.txt'
from urllib.request import urlretrieve
urlretrieve(fn, 'moby_dick.txt')
```

*** =sample_code
```{python}
# Open a file: file
file = open('moby_dick.txt', mode='r')

# Print it
print(file.read())
```

*** =solution
```{python}
# Open a file: file
file = open('moby_dick.txt', mode='r')

# Print it
print(file.read())
```

*** =sct
```{python}
predef_msg = "You don't have to change any of the predefined code."
test_function_v2("open", do_eval=False, not_called_msg=predef_msg, params=["file", "mode"])
success_msg("Great job!")
```



--- type:NormalExercise lang:python xp:100 skills:2 key:b62fd865c9
## Testing test_function_v2 3

Testing `test_function_v2`
*** =instructions
- 
- 

*** =hint
- 
- 

*** =pre_exercise_code
```{python}
#PEC
fn = 'https://s3.amazonaws.com/assets.datacamp.com/production/course_998/datasets/moby_opens.txt'
from urllib.request import urlretrieve
urlretrieve(fn, 'moby_dick.txt')
```

*** =sample_code
```{python}
x = 'waddup'

# Print it
print(x)
```

*** =solution
```{python}
x = 'waddup'

# Print it
print(x)
```

*** =sct
```{python}
predef_msg = "You don't have to change any of the predefined code."
test_function_v2("print", do_eval=False, not_called_msg=predef_msg, params=["value"])
success_msg("Great job!")
```

--- type:NormalExercise lang:python xp:100 skills:2 key:dcbbb057c4
## Testing test_correct

Testing `test_correct`
*** =instructions
- 
- 

*** =hint
- 
- 

*** =pre_exercise_code
```{python}
#PEC
from urllib.request import urlretrieve
fn1 = 'https://s3.amazonaws.com/assets.datacamp.com/production/course_998/datasets/Chinook.sqlite'
urlretrieve(fn1, 'Chinook.sqlite')
```

*** =sample_code
```{python}
# Import packages
from sqlalchemy import create_engine
import pandas as pd

# Create engine: engine
engine = create_engine('sqlite:///Chinook.sqlite')

# Open engine connection
con = engine.connect()

# Perform query: rs
rs = con.execute("SELECT * FROM Album")

# Save results of the query to DataFrame: df
df = pd.DataFrame(rs.fetchall())

# Close connection
con.close()

# Print head of DataFrame df
print(df.head())

```

*** =solution
```{python}
# Import packages
from sqlalchemy import create_engine
import pandas as pd

# Create engine: engine
engine = create_engine('sqlite:///Chinook.sqlite')

# Open engine connection
con = engine.connect()

# Perform query: rs
rs = con.execute("SELECT * FROM Album")

# Save results of the query to DataFrame: df
df = pd.DataFrame(rs.fetchall())

# Close connection
con.close()

# Print head of DataFrame df
print(df.head())

```

*** =sct
```{python}

# Test: Predefined code
predef_msg = "You don't have to change any of the predefined code."

def df_diag():
    test_function("rs.fetchall")
    test_function("pandas.DataFrame")
    test_function("con.execute")
    
    

test_correct(lambda: test_object('df'), df_diag)

success_msg("Good job!")
```



--- type:NormalExercise lang:python xp:100 skills:2 key:b0410adc71
## Testing test_or

Testing `test_or`
*** =instructions
- 
- 

*** =hint
- 
- 

*** =pre_exercise_code
```{python}
#PEC
from urllib.request import urlretrieve
fn1 = 'https://s3.amazonaws.com/assets.datacamp.com/production/course_998/datasets/Chinook.sqlite'
urlretrieve(fn1, 'Chinook.sqlite')
```

*** =sample_code
```{python}
# Import packages
from sqlalchemy import create_engine
import pandas as pd

# Create engine: engine
engine = create_engine('sqlite:///Chinook.sqlite')

# Open engine connection
con = engine.connect()

# Perform query: rs
rs = con.execute("SELECT * FROM Album")

# Save results of the query to DataFrame: df
df = pd.DataFrame(rs.fetchall())

# Close connection
con.close()

# Print head of DataFrame df
print(df.head())

```

*** =solution
```{python}
# Import packages
from sqlalchemy import create_engine
import pandas as pd

# Create engine: engine
engine = create_engine('sqlite:///Chinook.sqlite')

# Open engine connection
con = engine.connect()

# Perform query: rs
rs = con.execute("SELECT * FROM Album")

# Save results of the query to DataFrame: df
df = pd.DataFrame(rs.fetchall())

# Close connection
con.close()

# Print head of DataFrame df
print(df.head())

```

*** =sct
```{python}



def df_test():
    test_function("rs.fetchall")
    test_function("con.execute")
    test_object("df")
    

test_or(df_test, lambda: test_object("df"))

success_msg("Good job!")
```

--- type:NormalExercise lang:python xp:100 skills:2 key:05c5b9aeb7
## Testing test_object w/ df

Testing `test_object`
*** =instructions
- 
- 

*** =hint
- 
- 

*** =pre_exercise_code
```{python}
#PEC
from urllib.request import urlretrieve
fn1 = 'https://s3.amazonaws.com/assets.datacamp.com/production/course_998/datasets/Chinook.sqlite'
urlretrieve(fn1, 'Chinook.sqlite')
```

*** =sample_code
```{python}
# Import packages
from sqlalchemy import create_engine
import pandas as pd

# Create engine: engine
engine = create_engine('sqlite:///Chinook.sqlite')

# Open engine connection
con = engine.connect()

# Perform query: rs
rs = con.execute("SELECT * FROM Album")

# Save results of the query to DataFrame: df
df = pd.DataFrame(rs.fetchall())

# Close connection
con.close()

# Print head of DataFrame df
print(df.head())

```

*** =solution
```{python}
# Import packages
from sqlalchemy import create_engine
import pandas as pd

# Create engine: engine
engine = create_engine('sqlite:///Chinook.sqlite')

# Open engine connection
con = engine.connect()

# Perform query: rs
rs = con.execute("SELECT * FROM Album")

# Save results of the query to DataFrame: df
df = pd.DataFrame(rs.fetchall())

# Close connection
con.close()

# Print head of DataFrame df
print(df.head())

```

*** =sct
```{python}

# Test: Predefined code
predef_msg = "You don't have to change any of the predefined code."

test_object("df")

success_msg("Good job!")
```

--- type:NormalExercise lang:python xp:100 skills:2 key:beda3ff71a
## Testing test_object w/ df

Testing `test_object`
*** =instructions
- 
- 

*** =hint
- 
- 

*** =pre_exercise_code
```{python}
#PEC
from urllib.request import urlretrieve
fn1 = 'https://s3.amazonaws.com/assets.datacamp.com/production/course_998/datasets/Chinook.sqlite'
urlretrieve(fn1, 'Chinook.sqlite')
```

*** =sample_code
```{python}
# Import packages
from sqlalchemy import create_engine
import pandas as pd

# Create engine: engine
engine = create_engine('sqlite:///Chinook.sqlite')

# Open engine connection
con = engine.connect()

# Perform query: rs
rs = con.execute("SELECT * FROM Album")

# Save results of the query to DataFrame: df
df = pd.DataFrame(rs.fetchall())

# Close connection
con.close()

# Print head of DataFrame df
print(df.head())

```

*** =solution
```{python}
# Import packages
from sqlalchemy import create_engine
import pandas as pd

# Create engine: engine
engine = create_engine('sqlite:///Chinook.sqlite')

# Open engine connection
con = engine.connect()

# Perform query: rs
rs = con.execute("SELECT * FROM Album")

# Save results of the query to DataFrame: df
df = pd.DataFrame(rs.fetchall())

# Close connection
con.close()

# Print head of DataFrame df
print(df.head())

```

*** =sct
```{python}

# Test: Predefined code
predef_msg = "You don't have to change any of the predefined code."

test_object("df")

success_msg("Good job!")
```

--- type:NormalExercise lang:python xp:100 skills:2 ,8 key:ad4428428a
## Testing test_correct within a context manager

Testing `test_correct` within a context manager

*** =instructions
- help! :-D

*** =hint
- blah

*** =pre_exercise_code
```{python}
from urllib.request import urlretrieve
fn1 = 'https://s3.amazonaws.com/assets.datacamp.com/production/course_998/datasets/Chinook.sqlite'
urlretrieve(fn1, 'Chinook.sqlite')
#
from sqlalchemy import create_engine
import pandas as pd
#
engine = create_engine('sqlite:///Chinook.sqlite')
```

*** =sample_code
```{python}
# Open engine in context manager
# Perform query and save results to DataFrame: df
with engine.connect() as con:
    rs = con.execute("SELECT LastName, Title FROM Employee")
    df = pd.DataFrame(rs.fetchmany(size=3))
    df.columns = rs.keys()

# Print the length of the DataFrame df
print(len(df))

# Print the head of the DataFrame df
print(df.head())

```

*** =solution
```{python}
# Open engine in context manager
# Perform query and save results to DataFrame: df
with engine.connect() as con:
    rs = con.execute("SELECT LastName, Title FROM Employee")
    df = pd.DataFrame(rs.fetchmany(size=3))
    df.columns = rs.keys()

# Print the length of the DataFrame df
print(len(df))

# Print the head of the DataFrame df
print(df.head())

```

*** =sct
```{python}
# Tests for the context manager body
def test_with_body():

    # Test: call to con.execute() and 'rs' variable
    test_object("rs", do_eval=False)
    #test_function("con.execute")
    #test_function("rs.fetchmany")
    def inner_test():
        test_function("rs.fetchmany")
        test_function("rs.keys")
        test_function("con.execute")
        

    # Test: call to pd.DataFrame() and 'df' variable
    test_correct(lambda: test_object('df'),
             lambda: inner_test())

# Test: Context manager
test_with(
    1,
    context_vals=True,
    context_tests=lambda: test_function("engine.connect"),
    body=test_with_body
)



success_msg("Awesome!")
```

--- type:NormalExercise lang:python xp:100 skills:2 key:ed693c5d52
## Bringing it all together (1)

You've got your first taste of writing your own functions in the previous exercises. You've learned how to add parameters to your own function definitions, return a value or multiple values with tuples, and how to call the functions you've defined.

In this and the following exercise, you will bring together all these concepts and apply them to a simple data science problem. You will load a dataset and develop functionalities to extract simple insights from the data. 

For this exercise, your goal is to recall how to load a dataset into a dataframe. The dataset contains Twitter data and you will iterate over entries in a column to build a dictionary with keys the names of languages and values the number of tweets in the given language. The file `tweets.csv` is available in your current directory.

*** =instructions
- Import the pandas package with the alias `pd`.
- Import the file `'tweets.csv'` using the pandas function `read_csv()`. Assign the resulting dataframe to `df`.
- Complete the `for` loop by iterating over the `'lang'` column in the dataframe `df`.
- Complete the bodies of the `if-else` statements in the `for` loop: **if** the key is in `langs_count`, add `1` to its current value, **else** add the key to `langs_count` and set its value to `1`. Use the loop variable `entry` in your code.


*** =hint
- To import a package `x` with the alias `y`, do: `import x as y`.
- To import the file, pass the filename `'tweets.csv'` to `read_csv()`. Remember that `read_csv()` is a pandas function.
- To access a column `'a'` in a dataframe `b`, do: `b['a']`.
- To _update_ the value of a key `entry` in a dictionary `d`, do: `d[entry] = ` _operation_. Use a similar syntax when adding a new key to the dictionary and setting its value.

*** =pre_exercise_code
```{python}
fn = 'https://s3.amazonaws.com/assets.datacamp.com/production/course_1342/datasets/tweets.csv'
from urllib.request import urlretrieve
urlretrieve(fn, 'tweets.csv')

```

*** =sample_code
```{python}
# Import pandas


# Import Twitter data as dataframe: df
df = ____

# Initialize an empty dictionary: langs_count
langs_count = {}

# ...
col = df['lang']

# Iterate over lang column in df
for entry in ____:

    # If the language is in langs_count, add 1
    if entry in langs_count.keys():
        ____
    # Else add the language to langs_count, set the value to 1
    else:
        ____

# Print the populated dictionary
print(langs_count)

```

*** =solution
```{python}
# Import pandas
import pandas as pd

# Import Twitter data as dataframe: df
df = pd.read_csv('tweets.csv')

# Initialize an empty dictionary: langs_count
langs_count = {}

# ...
col = df['lang']

# Iterate over lang column in dataframe
for entry in col:

    # If the language is in langs_count, add 1
    if entry in langs_count.keys():
        langs_count[entry] += 1
    # Else add the language to langs_count, set the value to 1
    else:
        langs_count[entry] = 1

# Print the populated dictionary
print(langs_count)

```

*** =sct
```{python}
# All functions used here are defined in the pythonwhat Python package.
# Documentation can also be found at github.com/datacamp/pythonwhat/wiki

predef_msg = "You don't have to change any of the predefined code."

# Test: import of pandas package
test_import("pandas")

# Test: pd.read_csv() call
test_function("pandas.read_csv")

# Test: df object
test_object("df")


# Test: for loop iterable
def test_for_iter():
    test_object("col")



def test_for_body():
    test_student_typed("langs_count[entry] += 1", not_typed_msg="Did you add 1 to the current value of the key in the `if` statement?",
    pattern=False)
    test_student_typed("langs_count[entry] = 1", not_typed_msg="Did you initialize the value of the key in the `else` statement?",
    pattern = False)

# Test: for loop
test_for_loop(
    index=1,
    for_iter=test_for_iter,
    body=test_for_body
)


# Test: langs_count object
test_object("langs_count")

# Test: print() call
test_function(
    "print",
    not_called_msg=predef_msg,
    incorrect_msg=predef_msg
)

success_msg("Great work!")

```
--- type:NormalExercise lang:python xp:100 skills:2 key:f8d6f897de
## Test_student_typed

Is `test_student_typed()` working?
*** =instructions
- ?

*** =hint
- ?

*** =pre_exercise_code
```{python}
# pec
```

*** =sample_code
```{python}
print('globalteam')

```

*** =solution
```{python}
print('global team')

```

*** =sct
```{python}
# All functions used here are defined in the pythonwhat Python package.
# Documentation can also be found at github.com/datacamp/pythonwhat/wiki


test_student_typed("global\s+team", pattern=True, 
    not_typed_msg="Did you use the keyword `global` to change the value of the global variable `team`?")

success_msg("Great work!")

```

--- type:NormalExercise lang:python xp:100 skills:2 key:d442dfd8ee
## Nested Functions I

You've learned in the last video about nesting functions within functions. A couple reasons why you'd like to do this is to _encapsulate_ certain mechanisms within functions and to avoid writing out the same computations within functions repeatedly (_DRY_!). There's nothing new about defining nested functions: you simply define it as you would a regular function with `def` and embed it inside another function!

In this exercise, inside a function `three_shouts()`, you will define a nested function `inner()` that concatenates a string object with `!!!`. `three_shouts()` then returns a tuple of three elements, each a string concatenated with `!!!` using `inner()`. Go for it!

*** =instructions
- Complete the function header of `inner()` with a single parameter `word`.
- Complete the return value: each element of the tuple should be a call to `inner()`, passing in the parameters from `three_shouts()` as arguments to each call.

*** =hint
- A nested function is defined the same way you would define a regular function: `def` _function name_`(`_parameters_`):`.
- Each element of the tuple return value is a call to `inner()`. Do three `inner()` calls, passing in `word1`, `word2`, and `word3`.

*** =pre_exercise_code
```{python}
# pec
```

*** =sample_code
```{python}
# Define three_shouts
def three_shouts(word1, word2, word3):
    """Returns a tuple of strings
    concatenated with '!!!'."""

    # Define inner
    def ____(____):
        """Returns a string concatenated with '!!!'."""
         # Return word concatenated with '!!!'
        ____

    # Return a tuple of strings
    return (____, ____, ____)

# Call three_shouts() and print
print(three_shouts('a', 'b', 'c'))

```

*** =solution
```{python}
# Define three_shouts
def three_shouts(word1, word2, word3):
    """Returns a tuple of strings
    concatenated with '!!!'."""

    # Define inner
    def inner(word):
        """Returns a string concatenated with '!!!'."""
        # Return word concatenated with '!!!'
        return word + '!!!'

    # Return a tuple of strings
    return (inner(word1), inner(word2), inner(word3))

# Call three_shouts() and print
print(three_shouts('a', 'b', 'c'))

```

*** =sct
```{python}
# All functions used here are defined in the pythonwhat Python package.
# Documentation can also be found at github.com/datacamp/pythonwhat/wiki

test_student_typed("return\s+word\s+\+\s+\'!!!\'", pattern=True, 
    not_typed_msg="Did you return `word + '!!!'` in the inner function?")

def inner_test():
    test_function_definition("inner", results=[("Hi")])
    #test_function_definition("inner", lambda: test_student_typed("rreturn\s+word\s+\+\s+\'!!!\'", pattern=True, 
    #not_typed_msg="Did you return `word + '!!!'` in the inner function?"))
    #test_function_definition("inner", results=[("Hi")])


# Test: three_shouts() definition
test_function_definition("three_shouts", body=inner_test)

# TO-DO
# Test: inner() definition IN three_shouts()

# TO-DO
# Test: 3 inner() calls

# Test: three_shouts() call
test_function_v2(
    "three_shouts",
    do_eval=None,
    not_called_msg="You don't have to change any of the predefined code1.",
    incorrect_msg="You don't have to change any of the predefined code1."
)

# Test: print() call
test_function(
    "print",
    do_eval=False,
    not_called_msg="You don't have to change any of the predefined code2.",
    incorrect_msg="You don't have to change any of the predefined code2."
)

success_msg("Great work!")

```
--- type:NormalExercise lang:python xp:100 skills:2 key:2a23c21a24
## Nested Functions II

Great job, you've just nested a function within another function. One other pretty cool reason for nesting functions is the idea of a **closure**. This means that the nested or inner function remembers the state of its enclosing scope when called. Thus, anything defined locally in the enclosing scope is available to the inner function even when the outer function has finished execution.

Let's move forward then! In this exercise, you will complete the definition of the inner function `inner_echo()` and then call `echo()` a couple of times, each with a different argument. Complete the exercise and see what the output will be!

*** =instructions
- Complete the function header of `inner_echo()` with a single parameter `word1`.
- Return `inner_echo` from inside `echo()`.
- Call `echo()`, passing 2 as an argument. Assign the resulting function to `twice`.
- Call `echo()`, passing 3 as an argument. Assign the resulting function to `thrice`.

*** =hint
- A nested function is defined the same way you would define a regular function: `def` _function name_`(`_parameters_`):`.
- Make sure to return the function `inner_echo` without the parentheses `()` from _inside_ the `echo()` function.
- Make sure to assign the call to `echo()` to the object `twice`. Pass 2 as an argument to `echo()`.
- The second call to `echo()` follows the same format as the previous `echo()` call, but with 3 as an argument. Don't forget to assign the result to the object `thrice`.

*** =pre_exercise_code
```{python}
# pec

```

*** =sample_code
```{python}
# Define echo
def echo(n):
    """Return the inner_echo function."""

    # Define inner_echo
    def ____(____):
        """Concatenate n copies of word1."""
        echo_word = word1 * n
        return echo_word

    # Return inner_echo
    

# Call echo: twice


# Call echo: thrice


# Call twice() and thrice() then print
print(twice('hello'), thrice('hello'))

```

*** =solution
```{python}
# Define echo
def echo(n):
    """Return the inner_echo function."""

    # Define inner_echo
    def inner_echo(word1):
        """Concatenate n copies of word1."""
        echo_word = word1 * n
        return echo_word

    # Return inner_echo
    return inner_echo

# Call echo: twice
twice = echo(2)

# Call echo: thrice
thrice = echo(3)

# Call twice() and thrice() then print
print(twice('hello'), thrice('hello'))

```

*** =sct
```{python}
# All functions used here are defined in the pythonwhat Python package.
# Documentation can also be found at github.com/datacamp/pythonwhat/wiki

def inner_test():
    test_function_definition("inner_echo", body=lambda: test_object_after_expression("echo_word", context_vals = ['anything']))

# Test: echo() definition
test_function_definition("echo", body=inner_test)

success_msg("Great work!")

```

--- type:NormalExercise lang:python xp:100 skills:2 key:a14c11f75a
## Nested Functions and the keyword nonlocal

`nonlocal`

*** =instructions
- ok
- ok1

*** =hint
- Hint, here.
- And here.

*** =pre_exercise_code
```{python}
# pec

```

*** =sample_code
```{python}
def echo_shout(word):
    """Change the value of the nonlocal variable echo_word"""
    
    echo_word = word*2
    print(echo_word)
    
    def shout():
        nonlocal echo_word
        echo_word = echo_word + '!!!'
    
    shout()
    print(echo_word)
    
echo_shout('hello')
```

*** =solution
```{python}
def echo_shout(word):
    """Change the value of the nonlocal variable echo_word"""
    
    echo_word = word*2

    print(echo_word)

    def shout():
        nonlocal echo_word
        echo_word = echo_word + '!!!'
    
    shout()

    print(echo_word)
    
echo_shout('hello')

```

*** =sct
```{python}
# All functions used here are defined in the pythonwhat Python package.
# Documentation can also be found at github.com/datacamp/pythonwhat/wiki

test_student_typed("nonlocal\s+echo_word", not_typed_msg="Did you use the `nonlocal` keyword to change `echo_word` in the inner function `shuout`?")

def inner_test():
    test_object_after_expression("echo_word", context_vals=["hello"])
    test_function_definition("shout")
    test_function("shout")
    test_function("print", args=[], index=1)
    test_function("print", args=[], index=2)

test_function_definition("echo_shout", body=inner_test)

test_function("echo_shout")

```
