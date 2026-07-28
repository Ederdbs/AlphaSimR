# Genetic value

A wrapper for accessing the gv slot

## Usage

``` r
gv(pop)
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
gv(pop)
#>            Trait1
#>  [1,]  2.07517519
#>  [2,]  0.56268499
#>  [3,] -0.04911191
#>  [4,] -1.18503179
#>  [5,] -0.20830447
#>  [6,]  0.30106821
#>  [7,]  0.05614109
#>  [8,] -0.89593745
#>  [9,] -1.23209057
#> [10,]  0.57540674
```
