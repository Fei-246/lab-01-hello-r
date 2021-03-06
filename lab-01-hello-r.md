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

Plot y vs. x for the dino dataset. Then, calculate the correlation
coefficient between x and y for this dataset.

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

Plot y vs. x for the star dataset. Then, calculate the correlation
coefficient between x and y for this dataset.

``` r
star_data <- datasaurus_dozen %>%
  filter(dataset == "star")

ggplot(data = star_data, mapping = aes(x = x, y = y)) +
  geom_point()
```

![](lab-01-hello-r_files/figure-gfm/plot-star-1.png)<!-- -->

``` r
star_data %>%
  summarize(r = cor(x, y))
```

    ## # A tibble: 1 x 1
    ##         r
    ##     <dbl>
    ## 1 -0.0630

### Exercise 4

Plot y vs. x for the circle dataset. You can (and should) reuse code we
introduced above, just replace the dataset name with the desired
dataset. Then, calculate the correlation coefficient between x and y for
this dataset. How does this value compare to the r of dino?

``` r
circle_data <- datasaurus_dozen %>%
  filter(dataset == "circle")

ggplot(data = circle_data, mapping = aes(x = x, y = y))+ geom_point()
```

![](lab-01-hello-r_files/figure-gfm/plot-circle-1.png)<!-- -->

``` r
circle_data %>%
  summarize(r = cor (x,y))
```

    ## # A tibble: 1 x 1
    ##         r
    ##     <dbl>
    ## 1 -0.0683

### Exercise 5

Add code and narrative as needed. To add R chunks either type out the
backticks, curly braces, and the letter `r` or use the Insert chunk
button above, green C+.
