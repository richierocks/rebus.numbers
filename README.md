[![Project Status: Active - The project has reached a stable, usable state and is being actively developed.](http://www.repostatus.org/badges/0.1.0/active.svg)](http://www.repostatus.org/#active)
[![Is the package on CRAN?](http://www.r-pkg.org/badges/version/rebus.base)](http://www.r-pkg.org/pkg/rebus.base)
[![SemaphoreCI Build Status](https://semaphoreci.com/api/v1/projects/247c4ca2-6390-4337-a700-67f38bec6616/635308/badge.svg)](https://semaphoreci.com/richierocks/rebus-numbers)
[![AppVeyor Build Status](https://ci.appveyor.com/api/projects/status/2digni6g0ephnql9?svg=true)](https://ci.appveyor.com/project/richierocks/rebus-numbers)

# rebus.numbers: Regular Expression Builder, Um, Something (Number-Related Functionality)

This package contains number-related functionality for the [*rebus*](https://github.com/richierocks/rebus) package.  It is primarily intended for other R package developers.  For interactive use, try *rebus* instead.

## Build regular expressions in a human readable way

Regular expressions are a very powerful tool, but the syntax is terse enough
to be difficult to read.  This makes bugs easy to introduce and hard to
find.  This package contains functions to make building regular expressions
easier.

## Installation

To install the stable version, type:

```{r}
install.packages("rebus.numbers")
```

To install the development version, you first need the *devtools* package.

```{r}
install.packages("devtools")
```

Then you can install the *rebus.numbers* package using

```{r}
library(devtools)
install_github("richierocks/rebus.numbers")
```

## Package contents

`number_range` creates a regex that matches a range of integers.  For example, `number_range(-12, 123)` generates `(?:-(?:[1-9]|1[0-2])|(?:0[0-9]{2}|1[0-1][0-9]|12[0-3]))`.

`roman` generates a regex to match roman numerals, and `ROMAN` provides the constant form.  For example `roman(2, 3)` matches two or three roman numbers.

