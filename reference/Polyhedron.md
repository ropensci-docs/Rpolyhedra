# Polyhedron

Polyhedron container class, which is accessible by the final users upon
call

## Author

ken4rab

## Public fields

- `file.id`:

  Polyhedron file.id

- `state`:

  Polyhedron state

- `logger`:

  class logger

## Methods

### Public methods

- [`Polyhedron$new()`](#method-Polyhedron-new)

- [`Polyhedron$scrapeNetlib()`](#method-Polyhedron-scrapeNetlib)

- [`Polyhedron$scrapeDmccooey()`](#method-Polyhedron-scrapeDmccooey)

- [`Polyhedron$deserialize()`](#method-Polyhedron-deserialize)

- [`Polyhedron$getName()`](#method-Polyhedron-getName)

- [`Polyhedron$getState()`](#method-Polyhedron-getState)

- [`Polyhedron$getSolid()`](#method-Polyhedron-getSolid)

- [`Polyhedron$isChecked()`](#method-Polyhedron-isChecked)

- [`Polyhedron$getRGLModel()`](#method-Polyhedron-getRGLModel)

- [`Polyhedron$exportToXML()`](#method-Polyhedron-exportToXML)

- [`Polyhedron$getErrors()`](#method-Polyhedron-getErrors)

- [`Polyhedron$checkProperties()`](#method-Polyhedron-checkProperties)

- [`Polyhedron$clone()`](#method-Polyhedron-clone)

------------------------------------------------------------------------

### Method `new()`

Create a polyhedronState object

#### Usage

    Polyhedron$new(file.id, state = NULL)

#### Arguments

- `file.id`:

  the file id

- `state`:

  polyhedron state object

#### Returns

A new Polyhedron object.

------------------------------------------------------------------------

### Method `scrapeNetlib()`

scrape Netlib polyhedron definition

#### Usage

    Polyhedron$scrapeNetlib(netlib.p3.lines)

#### Arguments

- `netlib.p3.lines`:

  vector with netlib definition lines

#### Returns

A new PolyhedronStateDefined object.

------------------------------------------------------------------------

### Method `scrapeDmccooey()`

scrape Dmccooey polyhedron definition

#### Usage

    Polyhedron$scrapeDmccooey(polyhedra.dmccooey.lines)

#### Arguments

- `polyhedra.dmccooey.lines`:

  vector with Dmccooey definition lines

#### Returns

A new PolyhedronStateDefined object.

------------------------------------------------------------------------

### Method `deserialize()`

deserialize a polyhedron state definition

#### Usage

    Polyhedron$deserialize(serialized.polyhedron)

#### Arguments

- `serialized.polyhedron`:

  a serialized version of a polyhedron state

#### Returns

A new PolyhedronStateDefined object.

------------------------------------------------------------------------

### Method `getName()`

get Polyhedron name

#### Usage

    Polyhedron$getName()

#### Returns

string with polyhedron name

------------------------------------------------------------------------

### Method `getState()`

Gets polyhedron state

#### Usage

    Polyhedron$getState()

#### Returns

A new PolyhedronState object.

------------------------------------------------------------------------

### Method `getSolid()`

Gets a solid definition

#### Usage

    Polyhedron$getSolid()

#### Returns

A list of vertex vectors composing polyhedron faces.

------------------------------------------------------------------------

### Method `isChecked()`

checks Edges consistency

#### Usage

    Polyhedron$isChecked()

#### Returns

A boolean value

------------------------------------------------------------------------

### Method `getRGLModel()`

Return an 'rgl' model with an optional transformation described by
transformation.matrix parameter

#### Usage

    Polyhedron$getRGLModel(transformation.matrix = NULL)

#### Arguments

- `transformation.matrix`:

  transformation matrix parameter

#### Returns

An tmesh3d object

------------------------------------------------------------------------

### Method `exportToXML()`

exports an XML definition of current polyhedron

#### Usage

    Polyhedron$exportToXML()

#### Returns

A character object with the XML definition

------------------------------------------------------------------------

### Method `getErrors()`

returns the errors found when processing current polyhedron

#### Usage

    Polyhedron$getErrors()

#### Returns

a data.frame with polyhedron errors

------------------------------------------------------------------------

### Method `checkProperties()`

check properties of current polyhedron

#### Usage

    Polyhedron$checkProperties(expected.vertices, expected.faces)

#### Arguments

- `expected.vertices`:

  expected vertices number

- `expected.faces`:

  expected faces number

#### Returns

Unmodified polyhedron object

------------------------------------------------------------------------

### Method `clone()`

The objects of this class are cloneable with this method.

#### Usage

    Polyhedron$clone(deep = FALSE)

#### Arguments

- `deep`:

  Whether to make a deep clone.
