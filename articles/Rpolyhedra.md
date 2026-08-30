# Rpolyhedra

## Introduction

This package is a curation made based on the poly package found on
<https://netlib.org/polyhedra/> ([Original Help
message](https://raw.githubusercontent.com/ropensci/Rpolyhedra/master/man/html/poly_original_help_message.html)),
and the polyhedra database found on <http://dmccooey.com/polyhedra/>,
both of which provide polyhedra databases on its own format. As such,
Rpolyhedra provides with the following:

1.  A module to scrape the polyhedra for the different sources found
    with features for incremental correction of issues found and to be
    found in scraping process.
2.  A database of the scraped polyhedra.
3.  An R6 polyhedron representation with ‘rgl’ package visualizing
    capabilities.

## Usage

For final users, the package provides a common interface for accessing
public polyhedra databases, analyze properties, compare and visualize
them with RGL.

For advanced users, the package provides a simplified set of R6 objects
to scrape and compare polyhedra databases.

### Get available polyhedra

Once the original files had been processed, a simple call to
[`getAvailablePolyhedra()`](https://docs.ropensci.org/Rpolyhedra/reference/getAvailablePolyhedra.md)
retrieves a list of the available polyhedra with properties and status
in the polyhedra database:

``` r

#show only the first 10 polyhedra.
head(getAvailablePolyhedra(), n = 10)
```

    ##    source                      scraped.name            symbol vertices faces
    ## 1  netlib                       tetrahedron {3,3}\t@Y sub 3 @        4     4
    ## 31 netlib               square pyramid (j1)      \t@Y sub 4 @        5     5
    ## 42 netlib        triangular dipyramid (j12)      \t@Y sub 3 @        5     6
    ## 9  netlib                  triangular prism      \t@P sub 3 @        6     5
    ## 32 netlib           pentagonal pyramid (j2)      \t@Y sub 5 @        6     6
    ## 3  netlib                        octahedron {3,4}\t@S sub 3 @        6     8
    ## 37 netlib elongated triangular pyramid (j7)      \t@Y sub 3 @        7     7
    ## 74 netlib  augmented triangular prism (j49)      \t@Y sub 4 @        7     8
    ## 43 netlib        pentagonal dipyramid (j13)      \t@Y sub 5 @        7    10
    ## 2  netlib                              cube {4,3}\t@P sub 4 @        8     6
    ##     status
    ## 1  scraped
    ## 31 scraped
    ## 42 scraped
    ## 9  scraped
    ## 32 scraped
    ## 3  scraped
    ## 37 scraped
    ## 74 scraped
    ## 43 scraped
    ## 2  scraped

### Retrieve a polyhedron

The access to a particular polyhedron can be done with a call to
`getPolyhedron(<<source>>, <<polyhedron.name>>)`, which returns a
Polyhedron object. For example, to retrieve a cube from the netlib
database, the call would be:

``` r

cube <- getPolyhedron(source = "netlib", polyhedron.name = "cube")
```

## A demo

To try package functionality, a simple demo can be executed which shows
the 5 regular polyhedra.

``` r

# 1.  Obtain 5 regular solids
polyhedra.2.draw <- getAvailablePolyhedra(source = "netlib")
polyhedra.2.draw <- polyhedra.2.draw %>%
                        filter(scraped.name %in%
                            c("tetrahedron", "octahedron", "cube",
                               "icosahedron", "dodecahedron"))

# 2. Setup colors and scales
n <- nrow(polyhedra.2.draw)
polyhedron.colors <- rainbow(n)
polyhedron.scale <- 5

# 3. Open and setup RGL window
open3d()
```

    ## null 
    ##    2

``` r

par3d(FOV = 1)
rgl::bg3d( sphere =FALSE, fogtype = "none", color=c("black"))
rgl::view3d(theta = 0, phi=0, zoom=0.8, fov=1)

# 4. For each polyhedron, setup rotation, position and render
for (i in seq_len(n)) {
  # Obtain polyhedron
  polyhedron.row <- polyhedra.2.draw[i,]
  polyhedron.name <- polyhedron.row$scraped.name
  polyhedron <- getPolyhedron(source = polyhedron.row$source, polyhedron.name)

  # Setup angles, position into transformationMatrix
  current.angle <- i/n * 2 * pi
  tm <- rotationMatrix(current.angle, 1, 0, 0)
  x.pos <- round(polyhedron.scale * sin(current.angle), 2)
  y.pos <- round(polyhedron.scale * cos(current.angle), 2)
  tm <- tm %*% translationMatrix(x.pos, y.pos, 0)

  # Render
  print(paste("Drawing ", polyhedron.name, " rotated ", round(current.angle, 2),
              " in (1,0,0) axis. Translated to (", x.pos, ",", y.pos, ",0)",
              " with color ", polyhedron.colors[i], sep = ""))
  shape.rgl <- polyhedron$getRGLModel(transformation.matrix = tm)
  shade3d(shape.rgl, color = polyhedron.colors[i])
}
```

    ## [1] "Drawing tetrahedron rotated 1.26 in (1,0,0) axis. Translated to (4.76,1.55,0) with color #FF0000"
    ## [1] "Drawing octahedron rotated 2.51 in (1,0,0) axis. Translated to (2.94,-4.05,0) with color #CCFF00"
    ## [1] "Drawing cube rotated 3.77 in (1,0,0) axis. Translated to (-2.94,-4.05,0) with color #00FF66"
    ## [1] "Drawing icosahedron rotated 5.03 in (1,0,0) axis. Translated to (-4.76,1.55,0) with color #0066FF"
    ## [1] "Drawing dodecahedron rotated 6.28 in (1,0,0) axis. Translated to (0,5,0) with color #CC00FF"
