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
print(df)
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

# Let's practice!

Notes: Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam tristique
libero at est congue, sed vestibulum tortor laoreet. Aenean egestas massa non
commodo consequat. Curabitur faucibus, sapien vitae euismod imperdiet, arcu erat
semper urna, in accumsan sapien dui ac mi. Pellentesque felis lorem, semper nec
velit nec, consectetur placerat enim.
