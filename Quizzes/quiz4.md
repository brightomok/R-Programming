Ryan Tillis - R Programming - Data Science - Quiz 4 - Coursera
================
<a href="http://www.ryantillis.com"> Ryan Tillis </a>
June 15, 2016

R Programming Quiz 4
--------------------

This is Quiz 4 from the R Programming course within the Data Science Specialization.

### Questions

<hr>
<font size="+2">1. </font> What is produced at the end of this snippet of R code?

``` r
set.seed(1)
rpois(5, 2)
```

    ## [1] 1 1 2 4 1

<hr>
<font size="+1"> <b>

-   A vector with the numbers 1, 1, 2, 4, 1

</b> </font>

<hr>
``` r
set.seed(1)
rpois(5, 2)
```

    ## [1] 1 1 2 4 1

<hr>
<font size="+2">2. </font> What R function can be used to generate standard Normal random variables?

<hr>
<font size="+1"> <b>

-   rnorm

</b> </font>

<hr>
``` r
rnorm(10, 0, 1)
```

    ##  [1]  1.272429321  0.414641434 -1.539950042 -0.928567035 -0.294720447
    ##  [6] -0.005767173  2.404653389  0.763593461 -0.799009249 -1.147657009

<hr>
<font size="+2">3. </font> When simulating data, why is using the set.seed() function important? Select all that apply.

<hr>
<font size="+1"> <b>

-   It ensures that the sequence of random numbers starts in a specific place and is therefore reproducible.

</b> </font>

<hr>
##### Explanation:

Set.seed allows other to get the same psuedorandom sequence to verify results.

<hr>
``` r
set.seed(22)
```

<hr>
<font size="+2">4. </font> Which function can be used to evaluate the inverse cumulative distribution function for the Poisson distribution?

<hr>
<font size="+1"> <b>

-   qpois

</b> </font>

<hr>
##### Explanation:

See documentation ?qpois

<hr>
<font size="+2">5. </font> What does the following code do?

``` r
set.seed(10)
x <- rep(0:1, each = 5)
e <- rnorm(10, 0, 20)
y <- 0.5 + 2 * x + e
```

<hr>
<font size="+1"> <b>

-   Generate data from a Normal linear model

</b> </font>

<hr>
<hr>
<font size="+2">6. </font> What R function can be used to generate Binomial random variables?

<hr>
<font size="+1"> <b>

-   rbinom

</b> </font>

<hr>
<hr>
<font size="+2">7. </font> What aspect of the R runtime does the profiler keep track of when an R expression is evaluated?

<hr>
<font size="+1"> <b>

-   the function call stack

</b> </font>

<hr>
<font size="+2">8. </font> Consider the following R code

library(datasets) Rprof() fit &lt;- lm(y ~ x1 + x2) Rprof(NULL)

<hr>
<font size="+1"> <b>

-   100%

</b> </font>

<hr>
<font size="+2">9. </font> When using 'system.time()', what is the user time?

<hr>
<font size="+1"> <b>

-   It is the time spent by the CPU evaluating an expression

</b> </font>

<hr>
<font size="+2">10. </font> If a computer has more than one available processor and R is able to take advantage of that, then which of the following is true when using 'system.time()'?

<hr>
<font size="+1"> <b>

-   Elapsed time may be smaller than user time

</b> </font>

<hr>
Check out my website at: <http://www.ryantillis.com/>

<hr>
