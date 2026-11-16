
<!-- README.md is generated from README.Rmd. Please edit that file -->

# assignmentB2KeryanneGagnon

<!-- badges: start -->

<!-- badges: end -->

The goal of assignmentB2KeryanneGagnon is to allow users to count the
missing values in a data frame for all columns, except one which is used
to group the variables (and missing values).

## Installation

Package installation can be done directly by calling:

``` r
pak::pak("UBC-STAT545-F2026/assignmentB2KeryanneGagnon")
```

## Example

This is a basic example which shows you how to use the
`count_all_missing_by_group` function from the
`assignmentB2KeryanneGagnon` package:

``` r
library(assignmentB2KeryanneGagnon)
count_all_missing_by_group(airquality, Month)
#> # A tibble: 5 × 6
#>   Month Ozone Solar.R  Wind  Temp   Day
#>   <int> <int>   <int> <int> <int> <int>
#> 1     5     5       4     0     0     0
#> 2     6    21       0     0     0     0
#> 3     7     5       0     0     0     0
#> 4     8     5       3     0     0     0
#> 5     9     1       0     0     0     0
count_all_missing_by_group(airquality, Month, .groups = "keep")
#> # A tibble: 5 × 6
#> # Groups:   Month [5]
#>   Month Ozone Solar.R  Wind  Temp   Day
#>   <int> <int>   <int> <int> <int> <int>
#> 1     5     5       4     0     0     0
#> 2     6    21       0     0     0     0
#> 3     7     5       0     0     0     0
#> 4     8     5       3     0     0     0
#> 5     9     1       0     0     0     0
```
