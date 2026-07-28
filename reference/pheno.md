# Phenotype

A wrapper for accessing the pheno slot

## Usage

``` r
pheno(pop)
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
pheno(pop)
#>           Trait1
#>  [1,] -1.2406059
#>  [2,]  2.2622720
#>  [3,]  3.8127948
#>  [4,] -2.4160262
#>  [5,] -1.3738402
#>  [6,] -0.6764369
#>  [7,] -0.6330352
#>  [8,]  0.9064265
#>  [9,]  2.6489134
#> [10,] -0.6220745
```
