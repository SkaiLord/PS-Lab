lab_2
================

``` r
vec <- c(1,2,3,4)
class(vec)
```

    ## [1] "numeric"

``` r
char_vec <- c(1,2,3,"4")
print(char_vec)
```

    ## [1] "1" "2" "3" "4"

``` r
class(char_vec)
```

    ## [1] "character"

``` r
#matrix declaration
data <- c(1,2,3,4,5,6)
m <- matrix(data)
print(m)
```

    ##      [,1]
    ## [1,]    1
    ## [2,]    2
    ## [3,]    3
    ## [4,]    4
    ## [5,]    5
    ## [6,]    6

``` r
m <- matrix(data=data,nrow=3,ncol=2)
print(m)
```

    ##      [,1] [,2]
    ## [1,]    1    4
    ## [2,]    2    5
    ## [3,]    3    6

``` r
# By row filling
m <- matrix(data=data,nrow=3,ncol=2, byrow=T)
print(m)
```

    ##      [,1] [,2]
    ## [1,]    1    2
    ## [2,]    3    4
    ## [3,]    5    6

``` r
# Matrix Access
print(m[1,2])
```

    ## [1] 2

``` r
print(m[1,])
```

    ## [1] 1 2

``` r
print(m[,2])
```

    ## [1] 2 4 6

``` r
# Incrementing matrix by constant
new_matrix <- m+5
print(new_matrix)
```

    ##      [,1] [,2]
    ## [1,]    6    7
    ## [2,]    8    9
    ## [3,]   10   11

``` r
# List all variables
ls()
```

    ## [1] "char_vec"   "data"       "m"          "new_matrix" "vec"

``` r
# remove variable
rm(char_vec)
ls()
```

    ## [1] "data"       "m"          "new_matrix" "vec"

``` r
# Sequence command - to print elements in certain order, seq(start,end,step)
seq(1,100)
```

    ##   [1]   1   2   3   4   5   6   7   8   9  10  11  12  13  14  15  16  17  18
    ##  [19]  19  20  21  22  23  24  25  26  27  28  29  30  31  32  33  34  35  36
    ##  [37]  37  38  39  40  41  42  43  44  45  46  47  48  49  50  51  52  53  54
    ##  [55]  55  56  57  58  59  60  61  62  63  64  65  66  67  68  69  70  71  72
    ##  [73]  73  74  75  76  77  78  79  80  81  82  83  84  85  86  87  88  89  90
    ##  [91]  91  92  93  94  95  96  97  98  99 100

``` r
seq(1,10,0.5)
```

    ##  [1]  1.0  1.5  2.0  2.5  3.0  3.5  4.0  4.5  5.0  5.5  6.0  6.5  7.0  7.5  8.0
    ## [16]  8.5  9.0  9.5 10.0

``` r
# Repeat command - to repeat a specific command n times
rep(seq(1,10), times=3)
```

    ##  [1]  1  2  3  4  5  6  7  8  9 10  1  2  3  4  5  6  7  8  9 10  1  2  3  4  5
    ## [26]  6  7  8  9 10

``` r
# Set random seed generator to runif(iterations,start,end)
set.seed(1)
runif(10,100,200)
```

    ##  [1] 126.5509 137.2124 157.2853 190.8208 120.1682 189.8390 194.4675 166.0798
    ##  [9] 162.9114 106.1786

``` r
# Round - rounding number, round(operation, place)
set.seed(2)
round(runif(10,100,200),2)
```

    ##  [1] 118.49 170.24 157.33 116.81 194.38 194.35 112.92 183.34 146.80 155.00

``` r
# Integer entries only
as.integer(runif(10,100,200))
```

    ##  [1] 155 123 176 118 140 185 197 122 144 107
