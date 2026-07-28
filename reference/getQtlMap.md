# Get QTL genetic map

Retrieves the genetic map for the QTL of a given trait.

## Usage

``` r
getQtlMap(trait = 1, sex = "A", simParam = NULL)
```

## Arguments

- trait:

  an integer for the

- sex:

  determines which sex specific map is returned. Options are "A" for
  average map, "F" for female map, and "M" for male map. All options are
  equivalent if not using sex specific maps.

- simParam:

  an object of
  [`SimParam`](https://gaynorr.github.io/AlphaSimR/reference/SimParam.md)

## Value

Returns a data.frame with:

- id:

  Unique identifier for the QTL

- chr:

  Chromosome containing the QTL

- site:

  Segregating site on the chromosome

- pos:

  Genetic map position

## Examples

``` r
#Create founder haplotypes
founderPop = quickHaplo(nInd=10, nChr=1, segSites=10)

#Set simulation parameters
SP = SimParam$new(founderPop)
SP$addTraitA(5)

#Pull SNP map
getQtlMap(trait=1, simParam=SP)
#>        id chr site       pos
#> 1_2   1_2   1    2 0.1111111
#> 1_3   1_3   1    3 0.2222222
#> 1_4   1_4   1    4 0.3333333
#> 1_9   1_9   1    9 0.8888889
#> 1_10 1_10   1   10 1.0000000
```
