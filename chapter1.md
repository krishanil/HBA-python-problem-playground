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

--- type:NormalExercise lang:python xp:100 skills:2 key:bf5b161a37
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
test_function_v2("open", do_eval=False, not_called_msg=predef_msg, params=["name", "mode"])
success_msg("Great job!")
```
