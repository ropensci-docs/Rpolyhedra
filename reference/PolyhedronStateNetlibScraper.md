# PolyhedronStateNetlibScraper

Scrapes polyhedra from a PHD file format.

## Author

ken4rab

## Super class

[`Rpolyhedra::PolyhedronState`](https://docs.ropensci.org/Rpolyhedra/reference/PolyhedronState.md)
-\> `PolyhedronStateNetlibScraper`

## Public fields

- `netlib.p3.lines`:

  The path to the PHD files

- `labels.rows`:

  Labels - row of appearance

- `labels.map`:

  Labels - Map of content

- `errors`:

  the errors found

## Methods

### Public methods

- [`PolyhedronStateNetlibScraper$new()`](#method-PolyhedronStateNetlibScraper-new)

- [`PolyhedronStateNetlibScraper$extractRowsFromLabel()`](#method-PolyhedronStateNetlibScraper-extractRowsFromLabel)

- [`PolyhedronStateNetlibScraper$getLabels()`](#method-PolyhedronStateNetlibScraper-getLabels)

- [`PolyhedronStateNetlibScraper$scrapeNet()`](#method-PolyhedronStateNetlibScraper-scrapeNet)

- [`PolyhedronStateNetlibScraper$extractCFOutBrackets()`](#method-PolyhedronStateNetlibScraper-extractCFOutBrackets)

- [`PolyhedronStateNetlibScraper$scrapeVertices()`](#method-PolyhedronStateNetlibScraper-scrapeVertices)

- [`PolyhedronStateNetlibScraper$setupLabelsOrder()`](#method-PolyhedronStateNetlibScraper-setupLabelsOrder)

- [`PolyhedronStateNetlibScraper$getDataFromLabel()`](#method-PolyhedronStateNetlibScraper-getDataFromLabel)

- [`PolyhedronStateNetlibScraper$getName()`](#method-PolyhedronStateNetlibScraper-getName)

- [`PolyhedronStateNetlibScraper$scrape()`](#method-PolyhedronStateNetlibScraper-scrape)

- [`PolyhedronStateNetlibScraper$applyTransformationMatrix()`](#method-PolyhedronStateNetlibScraper-applyTransformationMatrix)

- [`PolyhedronStateNetlibScraper$buildRGL()`](#method-PolyhedronStateNetlibScraper-buildRGL)

- [`PolyhedronStateNetlibScraper$exportToXML()`](#method-PolyhedronStateNetlibScraper-exportToXML)

- [`PolyhedronStateNetlibScraper$clone()`](#method-PolyhedronStateNetlibScraper-clone)

Inherited methods

- [`Rpolyhedra::PolyhedronState$addError()`](https://docs.ropensci.org/Rpolyhedra/reference/PolyhedronState.html#method-addError)
- [`Rpolyhedra::PolyhedronState$checkEdgesConsistency()`](https://docs.ropensci.org/Rpolyhedra/reference/PolyhedronState.html#method-checkEdgesConsistency)
- [`Rpolyhedra::PolyhedronState$getSolid()`](https://docs.ropensci.org/Rpolyhedra/reference/PolyhedronState.html#method-getSolid)

------------------------------------------------------------------------

### Method `new()`

Initializes the object, taking the file.id and PDH file as parameters

#### Usage

    PolyhedronStateNetlibScraper$new(file.id, netlib.p3.lines)

#### Arguments

- `file.id`:

  the file id

- `netlib.p3.lines`:

  the lines to add

#### Returns

A new PolyhedronStateNetlibScraper object.

------------------------------------------------------------------------

### Method `extractRowsFromLabel()`

Extracts data from the label, taking the label number and the expected
label as parameters

#### Usage

    PolyhedronStateNetlibScraper$extractRowsFromLabel(label.number, expected.label)

#### Arguments

- `label.number`:

  the label number

- `expected.label`:

  the expected label

------------------------------------------------------------------------

### Method `getLabels()`

get Labels from current netlib file description

#### Usage

    PolyhedronStateNetlibScraper$getLabels()

#### Returns

a list containing labels from netlib file description

------------------------------------------------------------------------

### Method `scrapeNet()`

scrape Net Model from netlib format

#### Usage

    PolyhedronStateNetlibScraper$scrapeNet(net.txt, offset = 0)

#### Arguments

- `net.txt`:

  a vector containing net model in netlib format

- `offset`:

  in numbering vertices

#### Returns

a list containing a net model

------------------------------------------------------------------------

### Method `extractCFOutBrackets()`

Remove brackets for current field content

#### Usage

    PolyhedronStateNetlibScraper$extractCFOutBrackets(x)

#### Arguments

- `x`:

  a string containing brackets

#### Returns

value

------------------------------------------------------------------------

### Method `scrapeVertices()`

scrape vertices described in netlib format

#### Usage

    PolyhedronStateNetlibScraper$scrapeVertices(vertices.txt)

#### Arguments

- `vertices.txt`:

  vector containing netlib format vertices

#### Returns

data.frame containing netlib vertices

------------------------------------------------------------------------

### Method `setupLabelsOrder()`

setupLabelsOrder

#### Usage

    PolyhedronStateNetlibScraper$setupLabelsOrder()

#### Arguments

- `vertices.txt`:

  vector containing netlib format vertices

#### Returns

data.frame containing netlib vertices

------------------------------------------------------------------------

### Method `getDataFromLabel()`

Get data from label specified as parameter

#### Usage

    PolyhedronStateNetlibScraper$getDataFromLabel(label)

#### Arguments

- `label`:

  the label to get data from

#### Returns

value

------------------------------------------------------------------------

### Method `getName()`

get Polyhedron name

#### Usage

    PolyhedronStateNetlibScraper$getName()

#### Returns

string with polyhedron name

------------------------------------------------------------------------

### Method `scrape()`

scrape Netlib polyhedron definition

#### Usage

    PolyhedronStateNetlibScraper$scrape()

#### Returns

A new PolyhedronStateDefined object.

------------------------------------------------------------------------

### Method `applyTransformationMatrix()`

Apply transformation matrix to polyhedron

#### Usage

    PolyhedronStateNetlibScraper$applyTransformationMatrix(transformation.matrix)

#### Arguments

- `transformation.matrix`:

  the transformation matrix to apply to the polyhedron

------------------------------------------------------------------------

### Method `buildRGL()`

Creates a 'rgl' representation of the object

#### Usage

    PolyhedronStateNetlibScraper$buildRGL(transformation.matrix)

#### Arguments

- `transformation.matrix`:

  the transformation matrix to apply to the polyhedron

------------------------------------------------------------------------

### Method `exportToXML()`

serializes object in XML

#### Usage

    PolyhedronStateNetlibScraper$exportToXML()

------------------------------------------------------------------------

### Method `clone()`

The objects of this class are cloneable with this method.

#### Usage

    PolyhedronStateNetlibScraper$clone(deep = FALSE)

#### Arguments

- `deep`:

  Whether to make a deep clone.
