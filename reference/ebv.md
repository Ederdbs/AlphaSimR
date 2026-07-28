# Estimated breeding value

A wrapper for accessing the ebv slot

## Usage

``` r
ebv(pop)
```

## Arguments

- pop:

  a
  [`Pop-class`](https://gaynorr.github.io/AlphaSimR/reference/Pop-class.md)
  or similar object

## Examples

``` r
#Create founder haplotypes
founderPop = quickHaplo(nInd=10, nChr=1, segSites=10)

#Set simulation parameters
SP = SimParam$new(founderPop)
SP$addTraitAD(10, meanDD=0.5)
SP$setVarE(h2=0.5)

#Create population
pop = newPop(founderPop, simParam=SP)
pop@ebv = matrix(rnorm(pop@nInd), nrow=pop@nInd, ncol=1)
ebv(pop)
#>             [,1]
#>  [1,]  2.1126351
#>  [2,] -0.9256496
#>  [3,]  0.2113636
#>  [4,]  0.3777271
#>  [5,] -0.1808833
#>  [6,] -0.6428780
#>  [7,] -0.2777257
#>  [8,]  0.1154823
#>  [9,] -0.1849495
#> [10,]  0.3117223
```
