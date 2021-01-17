# R introduction

Install [R](https://cran.r-project.org) and [R Studio](https://rstudio.com/products/rstudio/). Install [GitHub Desktop](https://desktop.github.com) and optionally [Visual Studio Code](https://code.visualstudio.com).

## CRAN and where to find packages, helpful links

- [CRAN](https://cran.r-project.org)
- [Crantastic](http://crantastic.org)
- [Trending R packages on GitHub](https://github.com/trending/r)

## Common packages

- `dplyr` - For manipulating dataframes
- `tidyr` - For cleaning up information
- `stringr` - For manipulating strings and text data
- `lubridate` - For manipulating date information
- `httr` - For working with website data
- `ggvis` - For interactive visualizations
- `ggplot2` - For creating graphics and data visualizations
- `shiny` - For creating interactive applications that you can install on websites
- `rio` - Input & output, for importing and exporting data
- `rmarkdown` - For creating interactive notebooks/documents and sharing your data

- One package to load them all, `pacman` (package manager)

```R
# I recommend "pacman" for managing add-on packages. It will
# install packages, if needed, and then load the packages.
install.packages("pacman")

# Then load the package by using either of the following:
require(pacman)  # Gives a confirmation message.
library(pacman)  # No message.

# Or, by using "pacman::p_load" you can use the p_load
# function from pacman without actually loading pacman.
# These are packages I load every time.
pacman::p_load(pacman, dplyr, GGally, ggplot2, ggthemes, 
  ggvis, httr, lubridate, plotly, rio, rmarkdown, shiny, 
  stringr, tidyr)
```
