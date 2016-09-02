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
x = sum(range(10))

```

*** =solution
```{python}
x = sum(range(10))

```

*** =sct
```{python}
# All functions used here are defined in the pythonwhat Python package.
# Documentation can also be found at github.com/datacamp/pythonwhat/wiki


test_student_typed("sum", pattern=False, not_typed_msg="Did you use `sum`?")

success_msg("Great work!")

```
