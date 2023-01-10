
# CItest

<!-- badges: start -->
<!-- badges: end -->

This package contains the code for the conditional independence test proposed in 

Cai, Zhanrui, Runze Li, and Yaowu Zhang. "A distribution free conditional independence test with applications to causal discovery." Journal of Machine Learning Research 23.85 (2022): 1-41.

The main function is CI.test(). The kernel bandwidth can be chosen by the user's favoriate method.

## Installation

You can install package with the following lines:

``` r
library(devtools)
install_github("zhanruicai/CItest")
```

## Example

This is a toy example.

``` r
library(CItest)
n = 100
X1 = rnorm(n); X2 = rnorm(n); Z = rnorm(n)
X = X1+Z
Y = X2+Z
h = 1*1.06*sd(Z)*(4/(3*n))^{1/(1+4)}
CI.test(X, Y, Z, h)
```

