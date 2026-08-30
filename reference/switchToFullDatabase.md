# Switch to full database

Prompts user for changing database to fulldb in user filespace. Also,
allows the user to switch back to the package database, which is a
minimal one for testing purposes.

## Usage

``` r
switchToFullDatabase(env = NA, logger = lgr)
```

## Arguments

- env:

  The environment to run on, can be PACKAGE,

- logger:

  logger for inheriting threshold from calling class/function HOME or
  NA. If NA, it asks the user for a an Environment.

## Value

.data.env
