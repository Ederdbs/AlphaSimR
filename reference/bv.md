# Breeding value

Returns breeding values for all traits

## Usage

``` r
bv(pop, simParam = NULL)
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
bv(pop, simParam=SP)
#>           Trait1
#>  [1,]  1.5276158
#>  [2,] -1.0437701
#>  [3,] -0.7382409
#>  [4,] -1.1241948
#>  [5,]  0.8481598
#>  [6,]  0.9105736
#>  [7,] -0.1745911
#>  [8,] -1.2636856
#>  [9,]  1.2475354
#> [10,] -0.1894021
```
