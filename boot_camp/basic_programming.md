**Additional Resources:**

-   [R4DS Chapters 17-21:
    Programming](https://r4ds.had.co.nz/program-intro.html)
-   [R for Data Science Chapter 16: Dates and
    times](https://r4ds.had.co.nz/dates-and-times.html)

**Run the code below to load the `congress` dataframe we will use in
this quiz**

``` r
load(url('https://dssoc.github.io/datasets/congress.RData'))
```

<br/>

## Questions

<br>

**1. In your own words, describe what a function is and provide one
example of how you might use it in a data science.** 

<br/>

**2. Packages in R can contain many useful functions/commands. If you
didn’t know what a certain function did, or how it worked, where within
RStudio would you look to learn more / see example code? Where would you
look outside RStudio?**

<br/>

**3. Write a function that takes a character vector as an argument and
returns a character vector containing the first letters of each element
in the original vector. To show that it works, test it on the character
vector `sentence` defined below.**

``` r
sentence <- c('you', 'only', 'understand', 'data', 'if', 'data', 'is', 'tidy')
# your answer here
```

<br/>

**4. Create your own function which accepts a birthyear vector and
returns an approximate current age, then use it on the `birthyear`
column of the `congress` dataframe to create a new `age` column with
`mutate`.**

Note: functions used inside mutate accept single columns from the
original dataframe and return a column or vector of the same size. This
is a valuable tool for developing your workflow.

<br/>

**5. Write a function that accepts a date string and returns the day of
the week it corresponds to, then use it to create a new column of
`congress` representing the weekday of the birth of each politician
using `mutate`.**

<br/>

**6. Write a function that accepts a dataframe with the columns
`birthday` and `full_name`, and prints the names and ages of the `k`
oldest *representatives* in congress (i.e. not including senators) using
a “for loop”. In this sense, `k` is an arbitrary number that should be
given as an argument to the function - set the default value to be 5. If
you use the dataframe as the first argument, you can use the pipe
operator (“%\>%”) to pass the dataframe directly to the function. Define
your function such that you can use it like this:
`congress %>% print_oldest(3)`.**

<br/>

**7. Starting with the function from the previous question, change it
such that if k \> 5, it only prints the first 5. Test isusing this code:
`congress %>% print_oldest(100)`.**

<br/>

Thanks to Devin Cornell and Taylor Brown for helping to create these
quizzes!
