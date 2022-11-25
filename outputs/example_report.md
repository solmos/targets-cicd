Example Rmarkdown Report
================
Sergio
Produced on 2022-11-25

- <a href="#data" id="toc-data">Data</a>
- <a href="#model" id="toc-model">Model</a>

This is an example `Rmarkdown` report produced through a workflow built
on the `targets` framework, made portable using `renv`, and ran manually
or automatically using `GitHub Actions`. In this example, we show a data
quality check workflow report for a nutrition survey of children 6-59
months old.

## Data

``` r
head(mtcars_clean)
#>                    mpg cyl disp  hp drat    wt  qsec vs am gear carb
#> Mazda RX4         21.0   6  160 110 3.90 2.620 16.46  0  1    4    4
#> Mazda RX4 Wag     21.0   6  160 110 3.90 2.875 17.02  0  1    4    4
#> Datsun 710        22.8   4  108  93 3.85 2.320 18.61  1  1    4    1
#> Hornet 4 Drive    21.4   6  258 110 3.08 3.215 19.44  1  0    3    1
#> Hornet Sportabout 18.7   8  360 175 3.15 3.440 17.02  0  0    3    2
#> Valiant           18.1   6  225 105 2.76 3.460 20.22  1  0    3    1
#>                   mpg_rounded
#> Mazda RX4                  21
#> Mazda RX4 Wag              21
#> Datsun 710                 23
#> Hornet 4 Drive             21
#> Hornet Sportabout          19
#> Valiant                    18
```

## Model

``` r
model_mtcars
#> 
#> Call:
#> lm(formula = mpg_rounded ~ hp, data = mtcars_clean)
#> 
#> Coefficients:
#> (Intercept)           hp  
#>    29.96526     -0.06794
```
