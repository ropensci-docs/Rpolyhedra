# PolyhedronStateDeserializer

Polyhedron state for deserialize from database

## Author

ken4rab

## Super class

[`Rpolyhedra::PolyhedronState`](https://docs.ropensci.org/Rpolyhedra/reference/PolyhedronState.md)
-\> `PolyhedronStateDeserializer`

## Public fields

- `serialized.polyhedron`:

  polyhedron definition serialized

## Methods

### Public methods

- [`PolyhedronStateDeserializer$new()`](#method-PolyhedronStateDeserializer-new)

- [`PolyhedronStateDeserializer$scrape()`](#method-PolyhedronStateDeserializer-scrape)

- [`PolyhedronStateDeserializer$clone()`](#method-PolyhedronStateDeserializer-clone)

Inherited methods

- [`Rpolyhedra::PolyhedronState$addError()`](https://docs.ropensci.org/Rpolyhedra/reference/PolyhedronState.html#method-addError)
- [`Rpolyhedra::PolyhedronState$applyTransformationMatrix()`](https://docs.ropensci.org/Rpolyhedra/reference/PolyhedronState.html#method-applyTransformationMatrix)
- [`Rpolyhedra::PolyhedronState$buildRGL()`](https://docs.ropensci.org/Rpolyhedra/reference/PolyhedronState.html#method-buildRGL)
- [`Rpolyhedra::PolyhedronState$checkEdgesConsistency()`](https://docs.ropensci.org/Rpolyhedra/reference/PolyhedronState.html#method-checkEdgesConsistency)
- [`Rpolyhedra::PolyhedronState$exportToXML()`](https://docs.ropensci.org/Rpolyhedra/reference/PolyhedronState.html#method-exportToXML)
- [`Rpolyhedra::PolyhedronState$getName()`](https://docs.ropensci.org/Rpolyhedra/reference/PolyhedronState.html#method-getName)
- [`Rpolyhedra::PolyhedronState$getSolid()`](https://docs.ropensci.org/Rpolyhedra/reference/PolyhedronState.html#method-getSolid)

------------------------------------------------------------------------

### Method `new()`

Initialize PolyhedronStateDeserializer object

#### Usage

    PolyhedronStateDeserializer$new(serialized.polyhedron)

#### Arguments

- `serialized.polyhedron`:

  a serialized polyhedron

#### Returns

A new PolyhedronStateDeserializer object.

------------------------------------------------------------------------

### Method `scrape()`

Generates a PolyhedronStateDefined from a serialized polyhedron

#### Usage

    PolyhedronStateDeserializer$scrape()

#### Returns

A new PolyhedronStateDefined object.

------------------------------------------------------------------------

### Method `clone()`

The objects of this class are cloneable with this method.

#### Usage

    PolyhedronStateDeserializer$clone(deep = FALSE)

#### Arguments

- `deep`:

  Whether to make a deep clone.
