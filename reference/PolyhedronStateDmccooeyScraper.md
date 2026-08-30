# PolyhedronStateDmccooeyScraper

Scrapes polyhedra from a dmccooey file format

## Author

ken4rab

## Super class

[`Rpolyhedra::PolyhedronState`](https://docs.ropensci.org/Rpolyhedra/reference/PolyhedronState.md)
-\> `PolyhedronStateDmccooeyScraper`

## Public fields

- `regexp.values.names`:

  regexp for scraping values names

- `regexp.rn`:

  regexp for scraping real numbers

- `regexp.values`:

  regexp for scraping values

- `regexp.vertex`:

  regexp for scraping vertices

- `regexp.faces`:

  regexp for scraping faces

- `polyhedra.dmccooey.lines`:

  dmccooey polyhedra definition lines

- `labels.map`:

  labels map where values are

- `values`:

  labels map where values are

- `vertices`:

  specification

- `vertices.replaced`:

  3D values

- `faces`:

  definition

## Methods

### Public methods

- [`PolyhedronStateDmccooeyScraper$new()`](#method-PolyhedronStateDmccooeyScraper-new)

- [`PolyhedronStateDmccooeyScraper$setupRegexp()`](#method-PolyhedronStateDmccooeyScraper-setupRegexp)

- [`PolyhedronStateDmccooeyScraper$scrapeValues()`](#method-PolyhedronStateDmccooeyScraper-scrapeValues)

- [`PolyhedronStateDmccooeyScraper$scrapeVertices()`](#method-PolyhedronStateDmccooeyScraper-scrapeVertices)

- [`PolyhedronStateDmccooeyScraper$scrapeFaces()`](#method-PolyhedronStateDmccooeyScraper-scrapeFaces)

- [`PolyhedronStateDmccooeyScraper$scrape()`](#method-PolyhedronStateDmccooeyScraper-scrape)

- [`PolyhedronStateDmccooeyScraper$getName()`](#method-PolyhedronStateDmccooeyScraper-getName)

- [`PolyhedronStateDmccooeyScraper$applyTransformationMatrix()`](#method-PolyhedronStateDmccooeyScraper-applyTransformationMatrix)

- [`PolyhedronStateDmccooeyScraper$buildRGL()`](#method-PolyhedronStateDmccooeyScraper-buildRGL)

- [`PolyhedronStateDmccooeyScraper$exportToXML()`](#method-PolyhedronStateDmccooeyScraper-exportToXML)

- [`PolyhedronStateDmccooeyScraper$clone()`](#method-PolyhedronStateDmccooeyScraper-clone)

Inherited methods

- [`Rpolyhedra::PolyhedronState$addError()`](https://docs.ropensci.org/Rpolyhedra/reference/PolyhedronState.html#method-addError)
- [`Rpolyhedra::PolyhedronState$checkEdgesConsistency()`](https://docs.ropensci.org/Rpolyhedra/reference/PolyhedronState.html#method-checkEdgesConsistency)
- [`Rpolyhedra::PolyhedronState$getSolid()`](https://docs.ropensci.org/Rpolyhedra/reference/PolyhedronState.html#method-getSolid)

------------------------------------------------------------------------

### Method `new()`

Initialize Dmccooey scraper

#### Usage

    PolyhedronStateDmccooeyScraper$new(file.id, polyhedra.dmccooey.lines)

#### Arguments

- `file.id`:

  identifier of the definition file.

- `polyhedra.dmccooey.lines`:

  raw Dmccooey definition file lines

#### Returns

A new PolyhedronStateDmccooeyScraper object.

------------------------------------------------------------------------

### Method `setupRegexp()`

setupRegexp for Dmccooey definition

#### Usage

    PolyhedronStateDmccooeyScraper$setupRegexp()

#### Returns

This PolyhedronStateDmccooeyScraper object with regexp defined.

------------------------------------------------------------------------

### Method `scrapeValues()`

scrape values from Dmccooey definition

#### Usage

    PolyhedronStateDmccooeyScraper$scrapeValues(values.lines)

#### Arguments

- `values.lines`:

  values definitions in Dmccooey source

#### Returns

This PolyhedronStateDmccooeyScraper object with values defined.

------------------------------------------------------------------------

### Method `scrapeVertices()`

scrape polyhedron vertices from definition

#### Usage

    PolyhedronStateDmccooeyScraper$scrapeVertices(vertices.lines)

#### Arguments

- `vertices.lines`:

  vertices definitions in Dmccooey source

#### Returns

This PolyhedronStateDmccooeyScraper object with faces defined.

------------------------------------------------------------------------

### Method `scrapeFaces()`

scrape polyhedron faces from definition

#### Usage

    PolyhedronStateDmccooeyScraper$scrapeFaces(faces.lines)

#### Arguments

- `faces.lines`:

  face

#### Returns

This PolyhedronStateDmccooeyScraper object with faces defined.

------------------------------------------------------------------------

### Method `scrape()`

scrape Dmccooey polyhedron definition

#### Usage

    PolyhedronStateDmccooeyScraper$scrape()

#### Returns

A new PolyhedronStateDefined object.

------------------------------------------------------------------------

### Method `getName()`

get Polyhedron name

#### Usage

    PolyhedronStateDmccooeyScraper$getName()

#### Returns

string with polyhedron name

------------------------------------------------------------------------

### Method `applyTransformationMatrix()`

Apply transformation matrix to polyhedron

#### Usage

    PolyhedronStateDmccooeyScraper$applyTransformationMatrix(transformation.matrix)

#### Arguments

- `transformation.matrix`:

  the transformation matrix to apply to the polyhedron

------------------------------------------------------------------------

### Method `buildRGL()`

Creates a 'rgl' representation of the object

#### Usage

    PolyhedronStateDmccooeyScraper$buildRGL(transformation.matrix)

#### Arguments

- `transformation.matrix`:

  the transformation matrix to apply to the polyhedron

------------------------------------------------------------------------

### Method `exportToXML()`

serializes object in XML

#### Usage

    PolyhedronStateDmccooeyScraper$exportToXML()

------------------------------------------------------------------------

### Method `clone()`

The objects of this class are cloneable with this method.

#### Usage

    PolyhedronStateDmccooeyScraper$clone(deep = FALSE)

#### Arguments

- `deep`:

  Whether to make a deep clone.
