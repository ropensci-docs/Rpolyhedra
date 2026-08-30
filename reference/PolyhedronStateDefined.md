# PolyhedronStateDefined

Polyhedron State scraped and defined

## Author

ken4rab

## Super class

[`Rpolyhedra::PolyhedronState`](https://docs.ropensci.org/Rpolyhedra/reference/PolyhedronState.md)
-\> `PolyhedronStateDefined`

## Public fields

- `file.id`:

  polyhedron filename in original

- `source`:

  polyhedron definition source (netlib\|dmccooey)

- `name`:

  polyhedron name (netlib\|dmccooey)

- `symbol`:

  the eqn(1) input for two symbols separated by a tab; the Johnson
  symbol, and the Schlafli symbol (netlib)

- `dual`:

  the name of the dual polyhedron optionally followed by a horizontal
  tab and the number of the dual (netlib)

- `sfaces`:

  polyhedron solid face list (netlib)

- `svertices`:

  polyhedron solid vertices list (netlib)

- `vertices`:

  Polyhedron vertices list (netlib\|dmccooey)

- `vertices.centered`:

  centered vertices for applying transformation matrices

- `net`:

  polyhedron 2D net model with vertices defined for a planar
  representation (netlib)

- `solid`:

  polyhedron list of edges which generate a solid (netlib\|dmccooey)

- `hinges`:

  Polyhedron hinge list (netlib)

- `dih`:

  Dih attribute (netlib)

- `edges`:

  polyhedron edges (netlib\|dmccooey)

- `transformation.matrix`:

  transformation matrix for calculations and visualizing polyhedron

## Methods

### Public methods

- [`PolyhedronStateDefined$new()`](#method-PolyhedronStateDefined-new)

- [`PolyhedronStateDefined$scrape()`](#method-PolyhedronStateDefined-scrape)

- [`PolyhedronStateDefined$saveToJson()`](#method-PolyhedronStateDefined-saveToJson)

- [`PolyhedronStateDefined$getName()`](#method-PolyhedronStateDefined-getName)

- [`PolyhedronStateDefined$getSymbol()`](#method-PolyhedronStateDefined-getSymbol)

- [`PolyhedronStateDefined$adjustVertices()`](#method-PolyhedronStateDefined-adjustVertices)

- [`PolyhedronStateDefined$getVertices()`](#method-PolyhedronStateDefined-getVertices)

- [`PolyhedronStateDefined$getNet()`](#method-PolyhedronStateDefined-getNet)

- [`PolyhedronStateDefined$getSolid()`](#method-PolyhedronStateDefined-getSolid)

- [`PolyhedronStateDefined$inferEdges()`](#method-PolyhedronStateDefined-inferEdges)

- [`PolyhedronStateDefined$checkEdgesConsistency()`](#method-PolyhedronStateDefined-checkEdgesConsistency)

- [`PolyhedronStateDefined$triangulate()`](#method-PolyhedronStateDefined-triangulate)

- [`PolyhedronStateDefined$getConvHull()`](#method-PolyhedronStateDefined-getConvHull)

- [`PolyhedronStateDefined$calculateMassCenter()`](#method-PolyhedronStateDefined-calculateMassCenter)

- [`PolyhedronStateDefined$getNormalizedSize()`](#method-PolyhedronStateDefined-getNormalizedSize)

- [`PolyhedronStateDefined$getTransformedVertices()`](#method-PolyhedronStateDefined-getTransformedVertices)

- [`PolyhedronStateDefined$resetTransformationMatrix()`](#method-PolyhedronStateDefined-resetTransformationMatrix)

- [`PolyhedronStateDefined$applyTransformationMatrix()`](#method-PolyhedronStateDefined-applyTransformationMatrix)

- [`PolyhedronStateDefined$buildRGL()`](#method-PolyhedronStateDefined-buildRGL)

- [`PolyhedronStateDefined$exportToXML()`](#method-PolyhedronStateDefined-exportToXML)

- [`PolyhedronStateDefined$expectEqual()`](#method-PolyhedronStateDefined-expectEqual)

- [`PolyhedronStateDefined$serialize()`](#method-PolyhedronStateDefined-serialize)

- [`PolyhedronStateDefined$clone()`](#method-PolyhedronStateDefined-clone)

Inherited methods

- [`Rpolyhedra::PolyhedronState$addError()`](https://docs.ropensci.org/Rpolyhedra/reference/PolyhedronState.html#method-addError)

------------------------------------------------------------------------

### Method `new()`

object initialization routine

#### Usage

    PolyhedronStateDefined$new(
      source,
      file.id,
      name,
      vertices,
      solid,
      net = NULL,
      symbol = "",
      dual = NULL,
      sfaces = NULL,
      svertices = NULL,
      hinges = NULL,
      dih = NULL,
      normalize.size = TRUE
    )

#### Arguments

- `source`:

  the library to use

- `file.id`:

  identifier of the definition file.

- `name`:

  the polyhedron name

- `vertices`:

  the vertices

- `solid`:

  the solid object

- `net`:

  the net

- `symbol`:

  the symbol

- `dual`:

  whether it is dual or not

- `sfaces`:

  the solid faces

- `svertices`:

  the solid vertices

- `hinges`:

  the hinges

- `dih`:

  the dih

- `normalize.size`:

  whether it has to normalize the size or not

#### Returns

A new PolyhedronStateDefined object.

------------------------------------------------------------------------

### Method `scrape()`

scrape polyhedron. As the state is defined this functions do nothing

#### Usage

    PolyhedronStateDefined$scrape()

#### Returns

current object

------------------------------------------------------------------------

### Method `saveToJson()`

saves the state to a JSON file

#### Usage

    PolyhedronStateDefined$saveToJson(pretty = FALSE)

#### Arguments

- `pretty`:

  whether json output is pretty or not

#### Returns

a json object

------------------------------------------------------------------------

### Method `getName()`

get Polyhedron name

#### Usage

    PolyhedronStateDefined$getName()

#### Returns

string with polyhedron name

------------------------------------------------------------------------

### Method `getSymbol()`

get Polyhedron symbol

#### Usage

    PolyhedronStateDefined$getSymbol()

#### Returns

string with polyhedron symbol

------------------------------------------------------------------------

### Method `adjustVertices()`

adjust polyhedron Vertices

#### Usage

    PolyhedronStateDefined$adjustVertices(normalize.size = TRUE)

#### Arguments

- `normalize.size`:

  whether it has to normalize the size or not

#### Returns

modified PolyhedronStateDefined object.

------------------------------------------------------------------------

### Method `getVertices()`

Get the polyhedron state

#### Usage

    PolyhedronStateDefined$getVertices(solid = FALSE)

#### Arguments

- `solid`:

  toggles the production of solid vertices.

------------------------------------------------------------------------

### Method `getNet()`

Gets the net property

#### Usage

    PolyhedronStateDefined$getNet()

------------------------------------------------------------------------

### Method `getSolid()`

Gets the solid property

#### Usage

    PolyhedronStateDefined$getSolid()

------------------------------------------------------------------------

### Method `inferEdges()`

Infer edges

#### Usage

    PolyhedronStateDefined$inferEdges(force.recalculation = FALSE)

#### Arguments

- `force.recalculation`:

  forces the recalculation of the edges

------------------------------------------------------------------------

### Method `checkEdgesConsistency()`

Checks edges consistency

#### Usage

    PolyhedronStateDefined$checkEdgesConsistency()

------------------------------------------------------------------------

### Method [`triangulate()`](https://dmurdoch.github.io/rgl/dev/reference/triangulate.html)

Triangulates the polyhedron

#### Usage

    PolyhedronStateDefined$triangulate(force = FALSE)

#### Arguments

- `force`:

  forces the triangulation.

------------------------------------------------------------------------

### Method `getConvHull()`

Gets the convex hull

#### Usage

    PolyhedronStateDefined$getConvHull(
      transformation.matrix = self$transformation.matrix,
      vertices.id.3d = private$vertices.id.3d
    )

#### Arguments

- `transformation.matrix`:

  the transformation matrix

- `vertices.id.3d`:

  the vertices ids

#### Returns

the convex hull

------------------------------------------------------------------------

### Method `calculateMassCenter()`

Calculates the center of mass.

#### Usage

    PolyhedronStateDefined$calculateMassCenter(
      vertices.id.3d = private$vertices.id.3d,
      applyTransformation = TRUE
    )

#### Arguments

- `vertices.id.3d`:

  the vertices ids

- `applyTransformation`:

  does it need to apply transformations?

------------------------------------------------------------------------

### Method `getNormalizedSize()`

Gets the normalized size

#### Usage

    PolyhedronStateDefined$getNormalizedSize(size)

#### Arguments

- `size`:

  the object's size

------------------------------------------------------------------------

### Method `getTransformedVertices()`

Gets the transformed vertices

#### Usage

    PolyhedronStateDefined$getTransformedVertices(
      vertices = self$vertices.centered,
      transformation.matrix = self$transformation.matrix
    )

#### Arguments

- `vertices`:

  input vertices

- `transformation.matrix`:

  the transformation matrix

------------------------------------------------------------------------

### Method `resetTransformationMatrix()`

Resets the transformation matrix

#### Usage

    PolyhedronStateDefined$resetTransformationMatrix()

------------------------------------------------------------------------

### Method `applyTransformationMatrix()`

Apply transformation matrix to polyhedron

#### Usage

    PolyhedronStateDefined$applyTransformationMatrix(transformation.matrix)

#### Arguments

- `transformation.matrix`:

  the transformation matrix to apply to the polyhedron

#### Returns

an applied transformation.matrix

------------------------------------------------------------------------

### Method `buildRGL()`

Build 'rgl'

#### Usage

    PolyhedronStateDefined$buildRGL(transformation.matrix = NULL)

#### Arguments

- `transformation.matrix`:

  the transformation matrix

------------------------------------------------------------------------

### Method `exportToXML()`

Exports the object to XML format

#### Usage

    PolyhedronStateDefined$exportToXML()

------------------------------------------------------------------------

### Method `expectEqual()`

Determines if a polyhedron is equal to this one.

#### Usage

    PolyhedronStateDefined$expectEqual(polyhedron)

#### Arguments

- `polyhedron`:

  the polyhedron to compare to.

------------------------------------------------------------------------

### Method [`serialize()`](https://rdrr.io/r/base/serialize.html)

Serialize the object.

#### Usage

    PolyhedronStateDefined$serialize()

------------------------------------------------------------------------

### Method `clone()`

The objects of this class are cloneable with this method.

#### Usage

    PolyhedronStateDefined$clone(deep = FALSE)

#### Arguments

- `deep`:

  Whether to make a deep clone.
