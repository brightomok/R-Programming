Ryan Tillis - R Programming - Caching Inverse Matrix - Coursera
================
<a href="http://www.ryantillis.com"> Ryan Tillis </a>
6/28/2016

Assignment: Caching the Inverse of a Matrix
-------------------------------------------

Matrix inversion is usually a costly computation and there may be some benefit to caching the inverse of a matrix rather than compute it repeatedly (there are also alternatives to matrix inversion that we will not discuss here). Your assignment is to write a pair of functions that cache the inverse of a matrix.

Write the following functions:

makeCacheMatrix: This function creates a special "matrix" object that can cache its inverse. cacheSolve: This function computes the inverse of the special "matrix" returned by makeCacheMatrix above. If the inverse has already been calculated (and the matrix has not changed), then the cachesolve should retrieve the inverse from the cache. Computing the inverse of a square matrix can be done with the solve function in R. For example, if X is a square invertible matrix, then solve(X) returns its inverse.

For this assignment, assume that the matrix supplied is always invertible.

``` r
makeVector <- function(x = numeric()) {
       m <- NULL
       set <- function(y) {
              x <<- y
              m <<- NULL
       }
       get <- function() x
       setmean <- function(mean) m <<- mean
       getmean <- function() m
       list(set = set, get = get,
            setmean = setmean,
            getmean = getmean)
}

cachemean <- function(x, ...) {
       m <- x$getmean()
       if(!is.null(m)) {
              message("getting cached data")
              return(m)
       }
       data <- x$get()
       m <- mean(data, ...)
       x$setmean(m)
       m
}
```

Solution
--------

For this assignment, assume that the matrix supplied is always invertible.

Testing
-------

Below we call the function with a matrix, compute the inverse, retrieve the inverse from the cache list, change the call matrix to the inverse, compute the inverse on that and return the original function.

``` r
x1 <- makeInverse(matrix(c(1,2,3,4),2,2))
x1$getsolve() #Inverse not computed yet
```

    ## NULL

``` r
cachesolve(x1) #inverse returned after computation
```

    ##      [,1] [,2]
    ## [1,]   -2  1.5
    ## [2,]    1 -0.5

``` r
cachesolve(x1) #invers returned from cache
```

    ## retrieving inverse

    ##      [,1] [,2]
    ## [1,]   -2  1.5
    ## [2,]    1 -0.5

``` r
x1$set(x1$getsolve()) #Setting the function call to be the computed inverse
cachesolve(x1) #Inverse of the inverse is the original matrix
```

    ##      [,1] [,2]
    ## [1,]    1    3
    ## [2,]    2    4

<hr>
See more at <a href="http://www.ryantillis.com"> my website. </a>

<hr>
