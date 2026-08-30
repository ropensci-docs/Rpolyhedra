# Scrape polyhedra sources

Scrapes polyhedra objects from text files of different sources, in order
to make them available to the package.

## Usage

``` r
scrapePolyhedraSources(sources.config =
         getUserEnvir(".available.sources"),
    max.quant.config.schedule = 0,
    max.quant.scrape = 0, time2scrape.source = 30,
    source.filenames = NULL, retry.scrape = FALSE,
    logger = lgr)
```

## Arguments

- sources.config:

  the sources that will be used by the function

- max.quant.config.schedule:

  number of files to schedule

- max.quant.scrape:

  number of files scrape

- time2scrape.source:

  time applied to scrape source

- source.filenames:

  if not null specify which source filenames to scrape

- retry.scrape:

  should it retry scrape?

- logger:

  logger for inheriting threshold from calling class/function

## Value

polyhedra db object
