Ryan Tillis - Data Science - R Programming - Quiz 2 - Coursera
================
<a href="http://www.ryantillis.com"> Ryan Tillis </a>
August 4, 2016

Quiz 2
------

This is Quiz 2 from Coursera's R Programming class within the <a href="https://www.coursera.org/specializations/jhu-data-science">Data Science Specialization</a>. This publication is intended as a learning resource, all answers are documented and explained. Datasets are available in R packages.

<hr>
<font size="+2">**1.** </font>Suppose I define the following function in R

``` r
cube <- function(x, n) {
        x^3
}

cube(3)
```

    ## [1] 27

<hr>
<font size="+1"><b>

-   27

</b> </font>

<hr>
##### Explanation:

Function cubes the input.

<hr>
<font size="+2">**2.** </font> The following code will produce a warning in R.

``` r
x <- 1:10
if(x > 5) {
        x <- 0
}
```

    ## Warning in if (x > 5) {: the condition has length > 1 and only the first
    ## element will be used

Why?

<hr>
<font size="+1"><b>

-   'x' is a vector of length 10 and 'if' can only test a single logical statement.

</b> </font>

<hr>
##### Explanation:

R will automatically use the first element of the vector.

<hr>
<font size="+2">3. </font> Consider the following function

``` r
f <- function(x) {
        g <- function(y) {
                y + z
        }
        z <- 4
        x + g(x)
}
```

and then run

``` r
z <- 10
f(3)
```

    ## [1] 10

<hr>
<font size="+1"> <b>

-   10

</b> </font>

<hr>
##### Explanation:

Run it.

<hr>
<font size="+2">**4.**</font> Consider the following expression:

``` r
x <- 5
y <- if(x < 3) {
        NA
} else {
        10
}
y
```

    ## [1] 10

<hr>
<font size="+1"><b>

-   10

</b> </font>

<hr>
##### Explanation:

Run it.

<hr>
<font size="+2">5. </font>Consider the following R function

``` r
h <- function(x, y = NULL, d = 3L) {
        z <- cbind(x, d)
        if(!is.null(y))
                z <- z + y
        else
                z <- z + f
        g <- x + y / z
        if(d == 3L)
                return(g)
        g <- g + 10
        g
}
```

<hr>
-   <font size="+1">**f**</font>

<hr>
<hr>
<font size="+2">**6.** </font> What is an environment in R?

<hr>
-   <font size="+1">**a collection of symbol/value pairs**</font>

<hr>
<hr>
<font size="+2">**7.** </font> The R language uses what type of scoping rule for resolving free variables?

<hr>
-   <font size="+1">**lexical scoping**</font>

<hr>
<font size="+2">**8.** </font> How are free variables in R functions resolved?

<hr>
<font size="+1"><b>

-   The values of free variables are searched for in the environment in which the function was defined

</b> </font>

<hr>
<font size="+2">**9.** </font> What is one of the consequences of the scoping rules used in R?
<hr>
-   <font size="+1">**All objects must be stored in memory**</font>

<hr>
<font size="+2">**10.** </font> In R, what is the parent frame?

<hr>
<font size="+1"><b>

-   It is the environment in which a function was called

</b> </font>

<hr>
Check out my website at: <http://www.ryantillis.com/>
<hr>
