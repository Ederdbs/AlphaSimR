# Pull SNP genotypes

Retrieves SNP genotype data

## Usage

``` r
pullSnpGeno(pop, snpChip = 1, chr = NULL, asRaw = FALSE, simParam = NULL)
```

## Arguments

- pop:

  an object of
  [`Pop-class`](https://gaynorr.github.io/AlphaSimR/reference/Pop-class.md)

- snpChip:

  an integer. Indicates which SNP chip's genotypes to retrieve.

- chr:

  a vector of chromosomes to retrieve. If NULL, all chromosome are
  retrieved.

- asRaw:

  return in raw (byte) format

- simParam:

  an object of
  [`SimParam`](https://gaynorr.github.io/AlphaSimR/reference/SimParam.md)

## Value

Returns a matrix of SNP genotypes.

## Examples

``` r
#Create founder haplotypes
founderPop = quickHaplo(nInd=10, nChr=1, segSites=15)

#Set simulation parameters
SP = SimParam$new(founderPop)
SP$addTraitA(10)
SP$addSnpChip(5)

#Create population
pop = newPop(founderPop, simParam=SP)
pullSnpGeno(pop, simParam=SP)
#>    1_2 1_11 1_13 1_14 1_15
#> 1    1    1    1    1    1
#> 2    1    2    1    1    1
#> 3    2    0    0    1    1
#> 4    2    1    0    1    1
#> 5    1    1    1    1    1
#> 6    0    0    1    0    1
#> 7    1    2    1    0    1
#> 8    2    1    1    1    1
#> 9    0    0    1    1    1
#> 10   2    1    0    2    1
```
