# Get available sources

Gets the list of names of available sources in database to be used later
as references to the package.

## Usage

``` r
getAvailableSources()
```

## Value

sources string vector, which can be obtained from getAvailableSources()

## See also

getAvailablePolyhedra, getPolyhedron

## Examples

``` r
# gets all sources in the database
available.sources <- getAvailableSources()

# returns all polyhedra from all sources
available.polyhedra <- getAvailablePolyhedra(sources = available.sources)

# search within the polyhedron names from all sources
cubes <- getAvailablePolyhedra(
  sources = available.sources,
  search.string = "cube"
)
cubes
#>    source                     scraped.name            symbol vertices faces
#> 2  netlib                             cube {4,3}\t@P sub 4 @        8     6
#> 90 netlib   augmented truncated cube (j66)      \t@Q sub 4 @       28    22
#> 91 netlib biaugmented truncated cube (j67)      \t@Q sub 4 @       32    30
#>     status
#> 2  scraped
#> 90 scraped
#> 91 scraped
```
