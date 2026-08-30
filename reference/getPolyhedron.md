# Get polyhedron

Gets a polyhedron from the database. It returns an R6 Class with all its
characteristics and functions. The object returned, of type Polyhedron,
allows to the user to get access to all the functionality provided.

## Usage

``` r
getPolyhedron(source = "netlib", polyhedron.name)
```

## Arguments

- source:

  string vector, which can be obtained from getAvailableSources()

- polyhedron.name:

  a valid name of a polyhedron in the database. Current names can be
  found with getAvailablePolyhedra()

## Value

polyhedron R6 object

## See also

getAvailablePolyhedra, getAvailableSources

## Examples

``` r
tetrahedron <- getPolyhedron(
  source = "netlib",
  polyhedron.name = "tetrahedron"
)

# returns name of polyhedra
tetrahedron$getName()
#> [1] "tetrahedron"

# polyhedron state
tetrahedron.state <- tetrahedron$getState()

# Johnson symbol and Schlafli symbol
tetrahedron.state$getSymbol()
#> [1] "{3,3}\t@Y sub 3 @"

# vertex data.frame
tetrahedron.state$getVertices()
#>       Pos3D_1    Pos3D_2    Pos3D_3 Pos3D_1_exp Pos3D_2_exp Pos3D_3_exp
#> 1  -1.0000000 -0.5773503  0.0000000        -1.0  -0.5773503           0
#> 2  -0.5000000  0.2886751  0.0000000        -0.5   0.2886751           0
#> 3   0.0000000 -0.5773503  0.0000000         0.0  -0.5773503           0
#> 4   0.0000000  1.1547005  0.0000000         0.0   1.1547005           0
#> 5   0.5000000  0.2886751  0.0000000         0.5   0.2886751           0
#> 6   1.0000000 -0.5773503  0.0000000         1.0  -0.5773503           0
#> 7  -1.3333333 -0.7698004 -1.0886621          NA          NA          NA
#> 8  -0.8333333 -1.0584755 -0.2721655          NA          NA          NA
#> 9  -0.5000000 -0.2886751 -0.8164966          NA          NA          NA
#> 10 -0.4444444 -1.2188506 -1.1793840          NA          NA          NA
#>    Pos3D_1_exp_text Pos3D_2_exp_text Pos3D_3_exp_text
#> 1                -1   (-1/3)*sqrt(3)                0
#> 2              -1/2    (1/6)*sqrt(3)                0
#> 3                 0   (-1/3)*sqrt(3)                0
#> 4                 0    (2/3)*sqrt(3)                0
#> 5               1/2    (1/6)*sqrt(3)                0
#> 6                 1   (-1/3)*sqrt(3)                0
#> 7              <NA>             <NA>             <NA>
#> 8              <NA>             <NA>             <NA>
#> 9              <NA>             <NA>             <NA>
#> 10             <NA>             <NA>             <NA>

# List of faces of solid representation (3D)
tetrahedron.state$getSolid()
#> [[1]]
#> [1]  8 10  9
#> 
#> [[2]]
#> [1] 7 8 9
#> 
#> [[3]]
#> [1]  8  7 10
#> 
#> [[4]]
#> [1]  9 10  7
#> 

# List of faces of net representation (2D)
tetrahedron.state$getNet()
#> [[1]]
#> [1] 2 3 5
#> 
#> [[2]]
#> [1] 4 2 5
#> 
#> [[3]]
#> [1] 2 1 3
#> 
#> [[4]]
#> [1] 5 3 6
#> 
```
