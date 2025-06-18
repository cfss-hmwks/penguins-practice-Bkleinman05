## R Markdown

Here we are going to learn a bit about penguins

## Penguins

See below for averages on penguins.

    ## Warning: package 'dplyr' was built under R version 4.4.3

    ## Warning: package 'palmerpenguins' was built under R version 4.4.3

    ## # A tibble: 3 × 3
    ##   sex    avg_bill avg_mass
    ##   <fct>     <dbl>    <dbl>
    ## 1 female     37.3    3369.
    ## 2 male       40.4    4043.
    ## 3 <NA>       37.8    3540

## The Penguins of Torgersen

The following tracks the change in average body mass and bill length
measured for the penguins of Torgersen from 2007 to 2009.

    penguins %>%
      filter(island ==  "Torgersen") %>%
      group_by(year) %>%
      summarize(body_mass = mean(body_mass_g, na.rm = TRUE)) 

    ## # A tibble: 3 × 2
    ##    year body_mass
    ##   <int>     <dbl>
    ## 1  2007     3763.
    ## 2  2008     3856.
    ## 3  2009     3489.

    penguins %>%
      filter(island ==  "Torgersen") %>%
      group_by(year) %>%
      summarize(ave_bill_lenght = mean(bill_length_mm, na.rm = TRUE)) 

    ## # A tibble: 3 × 2
    ##    year ave_bill_lenght
    ##   <int>           <dbl>
    ## 1  2007            38.8
    ## 2  2008            38.8
    ## 3  2009            39.3

# Final task

You need to make a README.md doc – practice by outputting a .md file
here and renaming it to README.md before pushing to github
