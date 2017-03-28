---
title: A probabilistic introduction
description: 'This chapter will *probably* be awesome.

--- type:VideoExercise lang:python xp:50 skills:2 key:931db27cf9
## Flippin' coins and rollin' dice

numpy random number generator and plotting: BOOM!

*** =video_link
//player.vimeo.com/video/154783078

*** =video_hls
//videos.datacamp.com/transcoded/000_placeholders/v1/hls-temp.master.m3u8

--- type:NormalExercise lang:python xp:100 skills:2 key:373697b89c
## Random number generation with Python

In the video, Jake showed you how to use Python to generate (pseudo) random number using `numpy`, a skill that will come in handy whenever thinking probabilistically! In the demo, Jake used `np.random.rand()`, which generates random numbers between 0 and 1 with equal probability. Another function we will find useful is `np.random.randn()`, which generates normally-distributed numbers.

*** =instructions
- Import `numpy` and `matplotlib.pylot`, using their common aliases.
- Seed the random number generator with the value 0.
- Generate 10,000 normally-distributed random numbers using `np.random.randn()`.
- Plot the histogram with 20 bins and display the plot, using `plt.hist()` and `plt.show()`, respectively.
*** =hint

*** =pre_exercise_code
```{python}

```

*** =sample_code
```{python}
# Import necessary modules
import numpy as np
import matplotlib.pyplot as plt

# Set your PRNG seed
np.random.seed(0)

# Generate 10,000 normally-distributed random numbers
x = np.random.randn(10000)

# Plot the histogram and display the plot
plt.hist(x, bins=20);
plt.show()

```

*** =solution
```{python}
# Import necessary modules
import numpy as np
import matplotlib.pyplot as plt

# Set your PRNG seed
np.random.seed(0)

# Generate 10,000 normally-distributed random numbers: x
x = np.random.randn(10000)

# Plot the histogram and display the plot
plt.hist(x, bins=20);
plt.show()

```

*** =sct
```{python}
Ex().test_function('numpy.random.seed')
Ex().test_function('numpy.random.randn')
Ex().test_object('x')
Ex().test_function('matplotlib.pyplot.hist')
Ex().test_function('matplotlib.pyplot.show')

success_msg("Well done on generating loads of normally distributed numbers!")

```

--- type:NormalExercise lang:python xp:100 skills:2 key:8bc7653064
## Rollin' dice with Python

Jake simulated coin tosses by generating uniformly-distributed numbers, and comparing them to the probability 0.5. Here you will simulate rolling of dice using the same technique. The question we'd like to answer is this: how likely are you to roll more than four sixes in five rolls of a standard six-sided die?

*** =instructions
- Seed the random number generator with a value of 0.
- The probability of rolling a 6 on a single roll is 1/6. Using `np.random.rand()`, simulate 10,000 trials of 5 rolls.
- Compute the number of sixes observed in each trial.
- Plot and show a histogram of the results, with 11 bins.

*** =hint

*** =pre_exercise_code
```{python}
import numpy as np
import matplotlib.pyplot as plt
```

*** =sample_code
```{python}
# Seed your RNG
np.random.seed(0)

# Simulate 10,000 trials of 5 rolls each: sixes
sixes = (np.random.rand(10000, 5) < 1/6)

# Compute the number of sixes observed in each trial: total
total = sixes.sum(1)

# Plot and show the histrogram
plt.hist(total, 11);
plt.show()

```

*** =solution
```{python}
# Seed your RNG
np.random.seed(0)

# Simulate 10,000 trials of 5 rolls each: sixes
sixes = (np.random.rand(10000, 5) < 1/6)

# Compute the number of sixes observed in each trial: total
total = sixes.sum(1)

# Plot and show the histrogram
plt.hist(total, 11);
plt.show()

```

*** =sct
```{python}
Ex().test_function('numpy.random.seed')
#Ex().test_function('numpy.random.rand')
Ex().test_object('sixes')
Ex().test_function('sixes.sum')
Ex().test_object('total')

Ex().test_function('matplotlib.pyplot.hist')
Ex().test_function('matplotlib.pyplot.show')

success_msg("Well done: you have just used random number generation to answer a question about the probability of events occurring.")


```




--- type:MultipleChoiceExercise lang:python xp:50 skills:2 key:7d938156c1
## How many times did you roll 3 or more sixes?

You have now simulated the number of sixes observed in 10,000 trials of 5 rolls.
The number of sixes observed in each trial, `total`, is in the namespace. Your job now is to answer the question:

**What is the approximate probability of rolling 3 or more sixes in five rolls?**

To answer this, count the number of times an entry in `total` is `>= 3` and divide by the length of `total`.

*** =instructions
- 0.003
- 0.03
-  0.07
-  0.28

*** =hint

*** =pre_exercise_code
```{python}
import numpy as np
import matplotlib.pyplot as plt

# Seed your RNG
np.random.seed(0)

# Simulate 10,000 trials of 5 rolls each: sixes
sixes = (np.random.rand(10000, 5) < 1/6)

# Compute the number of sixes observed in each trial: total
total = sixes.sum(1)

```

*** =sct
```{python}
test_mc(2, msgs = ['Incorrect. Did you count the number of times an entry in `total` is `>= 3` or `>3`?', 'You got it!', 'Incorrect. Message here TBD.', 'Incorrect. Message here TBD.']) 

```
--- type:VideoExercise lang:python xp:50 skills:2 key:e8741eb52b
## Joint probabilities and conditional probabilities

flipping two coins; flipping a biased coin twice

*** =video_link
//player.vimeo.com/video/154783078

*** =video_hls
//videos.datacamp.com/transcoded/000_placeholders/v1/hls-temp.master.m3u8

--- type:NormalExercise lang:python xp:100 skills:2 key:47b36f08c0
## What is the probability that two randomly-chosen men are both over six feet tall?

Content

*** =instructions

*** =hint

*** =pre_exercise_code
```{python}

```

*** =sample_code
```{python}

```

*** =solution
```{python}

```

*** =sct
```{python}

```

--- type:NormalExercise lang:python xp:100 skills:2 key:ebd1641b1b
## What the probability that a man and his biological son are both over six feet tall?

Content

*** =instructions

*** =hint

*** =pre_exercise_code
```{python}

```

*** =sample_code
```{python}

```

*** =solution
```{python}

```

*** =sct
```{python}

```

--- type:VideoExercise lang:python xp:50 skills:2 key:d07a67440f
## The ways of Bayes

Bayes' Theorem. Derive symbolically based on $P(A, B) = P(B, A)$

*** =video_link
//player.vimeo.com/video/154783078

*** =video_hls
//videos.datacamp.com/transcoded/000_placeholders/v1/hls-temp.master.m3u8

--- type:NormalExercise lang:python xp:100 skills:2 key:1a7be6fc6c
## Computing conditional probabilites

We discussed the following idea: P(has disease|+ve test)

*** =instructions

*** =hint

*** =pre_exercise_code
```{python}

```

*** =sample_code
```{python}

```

*** =solution
```{python}

```

*** =sct
```{python}

```
