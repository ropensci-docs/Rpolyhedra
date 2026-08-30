# PolyhedronState

This abstract class provide the basis from which every polyhedron state
class derivate.

## Author

ken4rab

## Public fields

- `source`:

  polyhedron definition source

- `file.id`:

  polyhedron file id

- `errors`:

  Errors string

- `logger`:

  class logger

## Methods

### Public methods

- [`PolyhedronState$new()`](#method-PolyhedronState-new)

- [`PolyhedronState$addError()`](#method-PolyhedronState-addError)

- [`PolyhedronState$scrape()`](#method-PolyhedronState-scrape)

- [`PolyhedronState$getName()`](#method-PolyhedronState-getName)

- [`PolyhedronState$getSolid()`](#method-PolyhedronState-getSolid)

- [`PolyhedronState$checkEdgesConsistency()`](#method-PolyhedronState-checkEdgesConsistency)

- [`PolyhedronState$applyTransformationMatrix()`](#method-PolyhedronState-applyTransformationMatrix)

- [`PolyhedronState$buildRGL()`](#method-PolyhedronState-buildRGL)

- [`PolyhedronState$exportToXML()`](#method-PolyhedronState-exportToXML)

- [`PolyhedronState$clone()`](#method-PolyhedronState-clone)

------------------------------------------------------------------------

### Method `new()`

Create a polyhedronState object

#### Usage

    PolyhedronState$new(source, file.id)

#### Arguments

- `source`:

  the source file

- `file.id`:

  the file id

#### Returns

A new PolyhedronState object. '@description Adds an error to the error
string and log it as info

------------------------------------------------------------------------

### Method `addError()`

#### Usage

    PolyhedronState$addError(current.error)

#### Arguments

- `current.error`:

  the error to add

------------------------------------------------------------------------

### Method `scrape()`

Scrapes the polyhedra folder files

#### Usage

    PolyhedronState$scrape()

------------------------------------------------------------------------

### Method `getName()`

Get Polyhedron name

#### Usage

    PolyhedronState$getName()

#### Returns

string with polyhedron name

------------------------------------------------------------------------

### Method `getSolid()`

Returns the object corresponding to the solid

#### Usage

    PolyhedronState$getSolid()

------------------------------------------------------------------------

### Method `checkEdgesConsistency()`

Checks edge consistency

#### Usage

    PolyhedronState$checkEdgesConsistency()

------------------------------------------------------------------------

### Method `applyTransformationMatrix()`

Apply transformation matrix to polyhedron

#### Usage

    PolyhedronState$applyTransformationMatrix(transformation.matrix)

#### Arguments

- `transformation.matrix`:

  the transformation matrix to apply to the polyhedron

------------------------------------------------------------------------

### Method `buildRGL()`

Creates a 'rgl' representation of the object

#### Usage

    PolyhedronState$buildRGL(transformation.matrix)

#### Arguments

- `transformation.matrix`:

  the transformation matrix to apply to the polyhedron

------------------------------------------------------------------------

### Method `exportToXML()`

Gets an XML representation out of the polyhedron object

#### Usage

    PolyhedronState$exportToXML()

------------------------------------------------------------------------

### Method `clone()`

The objects of this class are cloneable with this method.

#### Usage

    PolyhedronState$clone(deep = FALSE)

#### Arguments

- `deep`:

  Whether to make a deep clone.
