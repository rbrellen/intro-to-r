---
type: slides
---

# Introduction

Notes: Text at the end of a slide prefixed like this will be displayed as
speaker notes on the side. Slides can be separated with a divider: ---.

---

# Get to know the iris data frame

- We prefer to use a data format called a `tibble`, which allows us to print our data frames cleaner.

```r
# Store iris as a tibble object named df
df <- as_tibble(iris)

# Print the iris data frame
df
```

```out
# A tibble: 150 x 5
   Sepal.Length Sepal.Width Petal.Length Petal.Width Species
          <dbl>       <dbl>        <dbl>       <dbl> <fct>
 1          5.1         3.5          1.4         0.2 setosa
 2          4.9         3            1.4         0.2 setosa
 3          4.7         3.2          1.3         0.2 setosa
 4          4.6         3.1          1.5         0.2 setosa
 5          5           3.6          1.4         0.2 setosa
 6          5.4         3.9          1.7         0.4 setosa
 7          4.6         3.4          1.4         0.3 setosa
 8          5           3.4          1.5         0.2 setosa
 9          4.4         2.9          1.4         0.2 setosa
10          4.9         3.1          1.5         0.1 setosa
# ... with 140 more rows
```

Notes: Notice the information included when we print `df`:
  - Number of rows and columns
  - Data types of each column
  - First ten rows of data
  - How many more rows of have not been printed

---

# Filtering

- To filter, we will use the `filter` function from the `dplyr` package.
- Inside the function, include a logical statement that evaluates to `TRUE` or `FALSE`

```r
# Return all rows from df where Sepal.Width is less than 3.0
filter(df, Sepal.Width < 3.0)
```

```out
# A tibble: 57 x 5
   Sepal.Length Sepal.Width Petal.Length Petal.Width Species
          <dbl>       <dbl>        <dbl>       <dbl> <fct>
 1          4.4         2.9          1.4         0.2 setosa
 2          4.5         2.3          1.3         0.3 setosa
 3          5.5         2.3          4           1.3 versicolor
 4          6.5         2.8          4.6         1.5 versicolor
 5          5.7         2.8          4.5         1.3 versicolor
 6          4.9         2.4          3.3         1   versicolor
 7          6.6         2.9          4.6         1.3 versicolor
 8          5.2         2.7          3.9         1.4 versicolor
 9          5           2            3.5         1   versicolor
10          6           2.2          4           1   versicolor
# ... with 47 more rows
```

---

# Using the pipe operator

- Rather than putting the data frame first, we can "pipe" it into the filter function using `%>%` (the pipe operator)
- It helps to think of the pipe operator at the spoken word "then"

```r
# Start with the df data frame, THEN filter to return all rows where Sepal.Width is less than 3.0
df %>% filter(Sepal.Width < 3.0)
```

```out
# A tibble: 57 x 5
   Sepal.Length Sepal.Width Petal.Length Petal.Width Species
          <dbl>       <dbl>        <dbl>       <dbl> <fct>
 1          4.4         2.9          1.4         0.2 setosa
 2          4.5         2.3          1.3         0.3 setosa
 3          5.5         2.3          4           1.3 versicolor
 4          6.5         2.8          4.6         1.5 versicolor
 5          5.7         2.8          4.5         1.3 versicolor
 6          4.9         2.4          3.3         1   versicolor
 7          6.6         2.9          4.6         1.3 versicolor
 8          5.2         2.7          3.9         1.4 versicolor
 9          5           2            3.5         1   versicolor
10          6           2.2          4           1   versicolor
# ... with 47 more rows
```

---

# Let's practice!

Notes: The `tidyverse` set of packages (including `dplyr`) is built around functions that expect a data frame as the first argument.
