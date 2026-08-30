# Scrape polyhedra objects

Gets polyhedra objects from text files of different sources, scheduling
and scraping using predefined configurations.

## Usage

``` r
scrapePolyhedra(
  scrape.config,
  source.filenames = NULL,
  sources.config = getUserEnvir(".available.sources"),
  logger = lgr
)
```

## Arguments

- scrape.config:

  predefined configuration for scraping

- source.filenames:

  if not null specify which source filenames to scrape

- sources.config:

  the sources that will be used by the function

- logger:

  logger for inheriting threshold from calling class/function

## Value

polyhedra db object
