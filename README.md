# R introduction

See video content [here](https://www.youtube.com/watch?v=_V8eKsto3Ug).

Install [R](https://cran.r-project.org) and [R Studio](https://rstudio.com/products/rstudio/). Install [GitHub Desktop](https://desktop.github.com) and optionally [Visual Studio Code](https://code.visualstudio.com).

## CRAN and where to find packages, helpful links

- [CRAN](https://cran.r-project.org)
- [Crantastic](http://crantastic.org)
- [Trending R packages on GitHub](https://github.com/trending/r)

## Common commands

- `Ctrl-L` Clear console
- `F1` after function opens its docs in the Help pane

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
  ggvis, httr, lubridate, plotly, psych, rio, rmarkdown, shiny, 
  stringr, tidyr)
```

## Histogram

Make a quick plot to view the data.

- `hist(iris$Petal.Length)`

## Summary and describe

Do graphical summaries/histograms first. Pictures first, numbers later.

- `summary()`
- `describe()` from `psych` package, for quantitative variables only

## Data types and data structures

Common data types:

- Numeric (integer, single precision, double precision)
- Character variables for text (no strings in R, only character)
- Logical (true/false or boolean)
- Complex
- Raw

These can be arranged into data structures. Common structures:

- Vector
  - (1+ numbers in a one-dimensional array, all in a line)
  - All of the same data type
  - R's basic data object
- Matrix/array
  - Has rows and columns, it's two-dimensional data
  - Need to be the same length
  - Need to be the same data class
  - Columns are not named, need to be referred to be their index number
  - Array is 3+ dimensions
- Dataframe - optimal level of complexity for working with data structure in R
  - Can have vectors of multiple types
  - All need to be the same length
  - Like a spreadsheet
  - R has special functions for working specifically with dataframes
- List
  - Most flexible data format
  - Ordered collection of elements
  - Can have any class, length, or structure
  - Can include lists inside

Coercion (changing data type) is good. Such as:

- Changing character to logical
- Matrix to dataframe, very common (`df <- as.data.frame(matrix(1:9, nrow = 3))`)
- Double to integer (`coerced <- as.integer()`)

Check type with `typeof()` or `is.vector()` etc...
