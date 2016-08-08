---
title       : Welcome to the Playground!
description : Where all good Python problems come to be buried.
attachments :
  slides_link : https://s3.amazonaws.com/assets.datacamp.com/course/teach/slides_example.pdf



--- type:NormalExercise lang:python xp:100 skills:2 key:1592680f34
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
