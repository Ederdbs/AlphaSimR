# Dominance deviations

Returns dominance deviations for all traits

## Usage

``` r
dd(pop, simParam = NULL)
```

## Arguments

- pop:

  an object of
  [`Pop-class`](https://gaynorr.github.io/AlphaSimR/reference/Pop-class.md)

- simParam:

  an object of
  [`SimParam`](https://gaynorr.github.io/AlphaSimR/reference/SimParam.md)

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
dd(pop, simParam=SP)
#>            Trait1
#>  [1,] -0.72960208
#>  [2,]  0.38078818
#>  [3,] -0.22873454
#>  [4,]  0.19896776
#>  [5,]  0.29889970
#>  [6,]  0.03008080
#>  [7,] -0.06011405
#>  [8,]  0.08167870
#>  [9,] -0.25305682
#> [10,]  0.28109235
```
