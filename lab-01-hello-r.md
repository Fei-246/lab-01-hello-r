Lab 01 - Hello R
================
Fei Xie
02/03/2021

## Load packages and data

``` r
library(tidyverse) 
library(datasauRus)
```

## Exercises

### Exercise 1

How many columns does the datasaurus\_dozen file have? What are the
variables included in the data frame?

dataset n \* <chr> <int> 1 away 142 2 bullseye 142 3 circle 142 4 dino
142 5 dots 142 6 h\_lines 142 7 high\_lines 142 8 slant\_down 142 9
slant\_up 142 10 star 142 11 v\_lines 142 12 wide\_lines 142 13 x\_shape
142

### Exercise 2

``` r
dino_data <- datasaurus_dozen %>%
  filter(dataset == "dino")

ggplot(data = dino_data, mapping = aes(x = x, y = y)) +
  geom_point()
```

![](lab-01-hello-r_files/figure-gfm/plot-dino-1.png)<!-- -->

``` r
dino_data %>%
  summarize(r = cor(x, y))
```

    ## # A tibble: 1 x 1
    ##         r
    ##     <dbl>
    ## 1 -0.0645

### Exercise 3

Add code and narrative as needed. Note that the R chunks are labelled
with `plot-star` and `cor-star` to provide spaces to place the code for
plotting and calculating the correlation coefficient. To finish, clean
up the narrative by removing these instructions.

Blah blah blah…

I’m some text, you should replace me with more meaningful text…

### Exercise 4

Add code and narrative as needed. Note that two R chunks are given but
they are not labeled. Use the convention from above to name them
appropriately.

### Exercise 5

Add code and narrative as needed. To add R chunks either type out the
backticks, curly braces, and the letter `r` or use the Insert chunk
button above, green C+.
