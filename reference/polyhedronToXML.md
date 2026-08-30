# Polyhedron to XML

Gets an XML representation out of the polyhedron object

## Usage

``` r
polyhedronToXML(polyhedron.state.defined, is.transformed.vertices = TRUE)
```

## Arguments

- polyhedron.state.defined:

  the polyhedron to get a representation from

- is.transformed.vertices:

  flag which states if vertices are in original position or
  transformationMatrix applied

## Value

an XML document, ready to be converted to String with XML::saveXML()

## Examples

``` r
# get the representation of a cube (netlib library)
XML::saveXML(polyhedronToXML(getPolyhedron("netlib", "cube")$state))
#> [1] "<?xml version=\"1.0\"?>\n<polyhedron name=\"cube\" dual=\"octahedron\">\n  <vertices>\n    <vertex>\n      <x>-0.735420625544347</x>\n      <y>-0.245140208514782</y>\n      <z>0</z>\n    </vertex>\n    <vertex>\n      <x>-0.735420625544347</x>\n      <y>0.245140208514782</y>\n      <z>0</z>\n    </vertex>\n    <vertex>\n      <x>-0.245140208514782</x>\n      <y>-0.735420625544347</y>\n      <z>0</z>\n    </vertex>\n    <vertex>\n      <x>-0.245140208514782</x>\n      <y>-0.245140208514782</y>\n      <z>0</z>\n    </vertex>\n    <vertex>\n      <x>-0.245140208514782</x>\n      <y>0.245140208514782</y>\n      <z>0</z>\n    </vertex>\n    <vertex>\n      <x>-0.245140208514782</x>\n      <y>0.735420625544347</y>\n      <z>0</z>\n    </vertex>\n    <vertex>\n      <x>0.245140208514782</x>\n      <y>-0.735420625544347</y>\n      <z>0</z>\n    </vertex>\n    <vertex>\n      <x>0.245140208514782</x>\n      <y>-0.245140208514782</y>\n      <z>0</z>\n    </vertex>\n    <vertex>\n      <x>0.245140208514782</x>\n      <y>0.245140208514782</y>\n      <z>0</z>\n    </vertex>\n    <vertex>\n      <x>0.245140208514782</x>\n      <y>0.735420625544347</y>\n      <z>0</z>\n    </vertex>\n    <vertex>\n      <x>0.735420625544347</x>\n      <y>-0.245140208514782</y>\n      <z>0</z>\n    </vertex>\n    <vertex>\n      <x>0.735420625544347</x>\n      <y>0.245140208514782</y>\n      <z>0</z>\n    </vertex>\n    <vertex>\n      <x>1.22570104257391</x>\n      <y>-0.245140208514782</y>\n      <z>0</z>\n    </vertex>\n    <vertex>\n      <x>1.22570104257391</x>\n      <y>0.245140208514782</y>\n      <z>0</z>\n    </vertex>\n    <vertex>\n      <x>-0.245140208514782</x>\n      <y>-0.245140208514782</y>\n      <z>-0.245140208514782</z>\n    </vertex>\n    <vertex>\n      <x>-0.245140208514782</x>\n      <y>-0.245140208514782</y>\n      <z>0.245140208514782</z>\n    </vertex>\n    <vertex>\n      <x>-0.245140208514782</x>\n      <y>0.245140208514782</y>\n      <z>-0.245140208514782</z>\n    </vertex>\n    <vertex>\n      <x>-0.245140208514782</x>\n      <y>0.245140208514782</y>\n      <z>0.245140208514782</z>\n    </vertex>\n    <vertex>\n      <x>0.245140208514782</x>\n      <y>-0.245140208514782</y>\n      <z>-0.245140208514782</z>\n    </vertex>\n    <vertex>\n      <x>0.245140208514782</x>\n      <y>-0.245140208514782</y>\n      <z>0.245140208514782</z>\n    </vertex>\n    <vertex>\n      <x>0.245140208514782</x>\n      <y>0.245140208514782</y>\n      <z>-0.245140208514782</z>\n    </vertex>\n    <vertex>\n      <x>0.245140208514782</x>\n      <y>0.245140208514782</y>\n      <z>0.245140208514782</z>\n    </vertex>\n  </vertices>\n  <faces>\n    <face id=\"1\" definition=\"16,15,19,20\"/>\n    <face id=\"2\" definition=\"18,16,20,22\"/>\n    <face id=\"3\" definition=\"18,17,15,16\"/>\n    <face id=\"4\" definition=\"15,17,21,19\"/>\n    <face id=\"5\" definition=\"20,19,21,22\"/>\n    <face id=\"6\" definition=\"22,21,17,18\"/>\n  </faces>\n  <identityMatrix>\n    <row>\n      <V1>1</V1>\n      <V2>0</V2>\n      <V3>0</V3>\n      <V4>0</V4>\n    </row>\n    <row>\n      <V1>0</V1>\n      <V2>1</V2>\n      <V3>0</V3>\n      <V4>0</V4>\n    </row>\n    <row>\n      <V1>0</V1>\n      <V2>0</V2>\n      <V3>1</V3>\n      <V4>0</V4>\n    </row>\n    <row>\n      <V1>0</V1>\n      <V2>0</V2>\n      <V3>0</V3>\n      <V4>1</V4>\n    </row>\n  </identityMatrix>\n</polyhedron>\n"
```
