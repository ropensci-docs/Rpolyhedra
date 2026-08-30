# Polyhedra database

Scrapes all polyhedra in data folder to save a representation which is
accessible by the final users upon call to
[`getPolyhedron()`](https://docs.ropensci.org/Rpolyhedra/reference/getPolyhedron.md).

## Public fields

- `version`:

  version of database file

- `polyhedra.rds.file`:

  path of rds database file

- `sources.config`:

  Sources configuration for scraping different sources

- `ledger`:

  rr ledger of scraping process

- `logger`:

  class logger

## Methods

### Public methods

- [`PolyhedraDatabase$new()`](#method-PolyhedraDatabase-new)

- [`PolyhedraDatabase$getVersion()`](#method-PolyhedraDatabase-getVersion)

- [`PolyhedraDatabase$configPolyhedraRDSPath()`](#method-PolyhedraDatabase-configPolyhedraRDSPath)

- [`PolyhedraDatabase$existsSource()`](#method-PolyhedraDatabase-existsSource)

- [`PolyhedraDatabase$addSourceConfig()`](#method-PolyhedraDatabase-addSourceConfig)

- [`PolyhedraDatabase$existsPolyhedron()`](#method-PolyhedraDatabase-existsPolyhedron)

- [`PolyhedraDatabase$getPolyhedraSourceDir()`](#method-PolyhedraDatabase-getPolyhedraSourceDir)

- [`PolyhedraDatabase$getPolyhedronFilename()`](#method-PolyhedraDatabase-getPolyhedronFilename)

- [`PolyhedraDatabase$getPolyhedron()`](#method-PolyhedraDatabase-getPolyhedron)

- [`PolyhedraDatabase$addPolyhedron()`](#method-PolyhedraDatabase-addPolyhedron)

- [`PolyhedraDatabase$configPolyhedraSource()`](#method-PolyhedraDatabase-configPolyhedraSource)

- [`PolyhedraDatabase$saveRDS()`](#method-PolyhedraDatabase-saveRDS)

- [`PolyhedraDatabase$cover()`](#method-PolyhedraDatabase-cover)

- [`PolyhedraDatabase$scrape()`](#method-PolyhedraDatabase-scrape)

- [`PolyhedraDatabase$testRR()`](#method-PolyhedraDatabase-testRR)

- [`PolyhedraDatabase$generateTestTasks()`](#method-PolyhedraDatabase-generateTestTasks)

- [`PolyhedraDatabase$schedulePolyhedraSources()`](#method-PolyhedraDatabase-schedulePolyhedraSources)

- [`PolyhedraDatabase$getAvailableSources()`](#method-PolyhedraDatabase-getAvailableSources)

- [`PolyhedraDatabase$getAvailablePolyhedra()`](#method-PolyhedraDatabase-getAvailablePolyhedra)

- [`PolyhedraDatabase$clone()`](#method-PolyhedraDatabase-clone)

------------------------------------------------------------------------

### Method `new()`

Create a new PolyhedraDatabase object.

#### Usage

    PolyhedraDatabase$new()

#### Returns

A new \`PolyhedraDatabase\` object.

------------------------------------------------------------------------

### Method `getVersion()`

get the version of the current object.

#### Usage

    PolyhedraDatabase$getVersion()

#### Returns

Database version

------------------------------------------------------------------------

### Method `configPolyhedraRDSPath()`

sets the path of the RDS object

#### Usage

    PolyhedraDatabase$configPolyhedraRDSPath()

#### Returns

Database version

------------------------------------------------------------------------

### Method `existsSource()`

Determines if the source exists on the database

#### Usage

    PolyhedraDatabase$existsSource(source)

#### Arguments

- `source`:

  source description

#### Returns

boolean value

------------------------------------------------------------------------

### Method `addSourceConfig()`

add source.config to the database

#### Usage

    PolyhedraDatabase$addSourceConfig(source.config)

#### Arguments

- `source.config`:

  SourceConfig object able to scrape source polyhedra definitions

#### Returns

PolyhedraDatabase object

------------------------------------------------------------------------

### Method `existsPolyhedron()`

Determines if the database includes a polyhedron which name matches the
parameter value

#### Usage

    PolyhedraDatabase$existsPolyhedron(source = "netlib", polyhedron.name)

#### Arguments

- `source`:

  source description

- `polyhedron.name`:

  polyhedron description

#### Returns

boolean value

------------------------------------------------------------------------

### Method `getPolyhedraSourceDir()`

gets polyhedra sources folder

#### Usage

    PolyhedraDatabase$getPolyhedraSourceDir(source, create.dir = TRUE)

#### Arguments

- `source`:

  source description

- `create.dir`:

  if dir does not exists, create it

#### Returns

string with polyhedra sources path

------------------------------------------------------------------------

### Method `getPolyhedronFilename()`

gets the filename of the polyhedron matching parameter.

#### Usage

    PolyhedraDatabase$getPolyhedronFilename(source, polyhedron.name, extension)

#### Arguments

- `source`:

  source description

- `polyhedron.name`:

  polyhedron description

- `extension`:

  extension of the polyhedron filename

#### Returns

string with polyhedron filename

------------------------------------------------------------------------

### Method [`getPolyhedron()`](https://docs.ropensci.org/Rpolyhedra/reference/getPolyhedron.md)

gets polyhedron object which name matches the parameter value

#### Usage

    PolyhedraDatabase$getPolyhedron(
      source = "netlib",
      polyhedron.name,
      strict = FALSE
    )

#### Arguments

- `source`:

  source description

- `polyhedron.name`:

  polyhedron description

- `strict`:

  halts execution if polyhedron not found

#### Returns

Polyhedron object

------------------------------------------------------------------------

### Method `addPolyhedron()`

add polyhedron object to the database

#### Usage

    PolyhedraDatabase$addPolyhedron(
      source = "netlib",
      source.filename,
      polyhedron,
      overwrite = FALSE,
      save.on.change = FALSE
    )

#### Arguments

- `source`:

  source description

- `source.filename`:

  filename of the polyhedron source definition

- `polyhedron`:

  polyhedron object

- `overwrite`:

  overwrite exiting definition

- `save.on.change`:

  saves Database state after operation

#### Returns

Polyhedron object

------------------------------------------------------------------------

### Method `configPolyhedraSource()`

Process parameter filenames using source.config parameter

#### Usage

    PolyhedraDatabase$configPolyhedraSource(
      source.config,
      source.filenames = NULL,
      max.quant = 0,
      save.on.change = FALSE
    )

#### Arguments

- `source.config`:

  source configuration for scraping files

- `source.filenames`:

  filenames of the polyhedron source definition

- `max.quant`:

  maximum filenames to process

- `save.on.change`:

  saves Database state after operation

#### Returns

Modified \`PolyhedraDatabase\` object.

------------------------------------------------------------------------

### Method [`saveRDS()`](https://rdrr.io/r/base/readRDS.html)

saveRDS

#### Usage

    PolyhedraDatabase$saveRDS(save.on.change = TRUE)

#### Arguments

- `save.on.change`:

  saves Database state after operation

#### Returns

saveRDS return status

------------------------------------------------------------------------

### Method `cover()`

Cover objects and applies covering.code parameter

#### Usage

    PolyhedraDatabase$cover(
      mode,
      sources = names(self$sources.config),
      covering.code,
      polyhedra.names = NULL,
      max.quant = 0,
      save.on.change = FALSE,
      seed = NULL
    )

#### Arguments

- `mode`:

  covering mode. Available values are "scrape.queued",
  "scrape.retry","skipped", "test"

- `sources`:

  sources names

- `covering.code`:

  code for applying in covering

- `polyhedra.names`:

  polyhedra names to cover (optional)

- `max.quant`:

  maximum numbers of polyhedra to cover

- `save.on.change`:

  saves Database state after operation

- `seed`:

  seed for deterministic random generator

#### Returns

A list with resulting objects covered

------------------------------------------------------------------------

### Method `scrape()`

Scrape polyhedra queued sources

#### Usage

    PolyhedraDatabase$scrape(
      mode = "scrape.queued",
      sources = names(self$sources.config),
      max.quant = 0,
      time2scrape.source = 30,
      save.on.change = FALSE,
      skip.still.queued = FALSE
    )

#### Arguments

- `mode`:

  covering mode. Available values are "scrape.queued",
  "scrape.retry","skipped", "test"

- `sources`:

  sources names

- `max.quant`:

  maximum numbers of polyhedra to cover

- `time2scrape.source`:

  maximum time to spend scraping each source

- `save.on.change`:

  saves Database state after operation

- `skip.still.queued`:

  Flag unscraped files with status \`skipped“

- `covering.code`:

  code for applying in covering

- `polyhedra.names`:

  polyhedra names to cover (optional)

#### Returns

A list with resulting objects covered

------------------------------------------------------------------------

### Method `testRR()`

testRR

#### Usage

    PolyhedraDatabase$testRR(sources = names(self$sources.config), max.quant = 0)

#### Arguments

- `sources`:

  sources names

- `max.quant`:

  maximum numbers of polyhedra to cover

#### Returns

A list with resulting objects tested

------------------------------------------------------------------------

### Method `generateTestTasks()`

generate Test tasks for selected polyhedra

#### Usage

    PolyhedraDatabase$generateTestTasks(
      sources = names(self$sources.config),
      polyhedra.names = NULL,
      TestTaskClass,
      max.quant = 0
    )

#### Arguments

- `sources`:

  sources names

- `polyhedra.names`:

  polyhedra names to cover (optional)

- `TestTaskClass`:

  an R6 TestTaskClass class

- `max.quant`:

  maximum numbers of polyhedra to cover

#### Returns

A list with resulting TestTasks generated

------------------------------------------------------------------------

### Method `schedulePolyhedraSources()`

Schedules polyhedra sources for scraping

#### Usage

    PolyhedraDatabase$schedulePolyhedraSources(
      sources.config = getPackageEnvir(".available.sources"),
      source.filenames = NULL,
      max.quant = 0,
      save.on.change = FALSE
    )

#### Arguments

- `sources.config`:

  sources configurations for scraping files

- `source.filenames`:

  filenames of the polyhedron source definition

- `max.quant`:

  maximum filenames to process

- `save.on.change`:

  saves Database state after operation

#### Returns

Modified \`PolyhedraDatabase\` object.

------------------------------------------------------------------------

### Method [`getAvailableSources()`](https://docs.ropensci.org/Rpolyhedra/reference/getAvailableSources.md)

Returns available sources in current database

#### Usage

    PolyhedraDatabase$getAvailableSources()

#### Returns

A vector with names of available sources

------------------------------------------------------------------------

### Method [`getAvailablePolyhedra()`](https://docs.ropensci.org/Rpolyhedra/reference/getAvailablePolyhedra.md)

Retrieves all polyhedron within the source those names match with
search.string

#### Usage

    PolyhedraDatabase$getAvailablePolyhedra(
      sources = self$getAvailableSources(),
      search.string = NULL,
      ignore.case = TRUE
    )

#### Arguments

- `sources`:

  sources names

- `search.string`:

  string for matching polyhedron names

- `ignore.case`:

  ignore case in search string

#### Returns

A list with resulting objects covered

------------------------------------------------------------------------

### Method `clone()`

The objects of this class are cloneable with this method.

#### Usage

    PolyhedraDatabase$clone(deep = FALSE)

#### Arguments

- `deep`:

  Whether to make a deep clone.
