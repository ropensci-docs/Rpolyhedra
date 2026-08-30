# Get available polyhedra

Gets the list of names of available polyhedra and its status in the
polyhedra database, which can be later called with getPolyhedron

## Usage

``` r
getAvailablePolyhedra(sources, search.string)
```

## Arguments

- sources:

  A string vector containing the source, which can be obtained from
  getAvailableSources().

- search.string:

  A search string

## Value

polyhedra names vector

## See also

getAvailableSources

## Examples

``` r

# gets all polyhedra in the database
available.polyhedra <- getAvailablePolyhedra()

# returns all polyhedra from a given source, in this case, netlib
available.netlib.polyhedra <- getAvailablePolyhedra(sources = "netlib")

# search within the polyhedron names

cube <- getAvailablePolyhedra(sources = "netlib", search.string = "cube")
cube
#>    source                     scraped.name            symbol vertices faces
#> 2  netlib                             cube {4,3}\t@P sub 4 @        8     6
#> 90 netlib   augmented truncated cube (j66)      \t@Q sub 4 @       28    22
#> 91 netlib biaugmented truncated cube (j67)      \t@Q sub 4 @       32    30
#>     status
#> 2  scraped
#> 90 scraped
#> 91 scraped
```
