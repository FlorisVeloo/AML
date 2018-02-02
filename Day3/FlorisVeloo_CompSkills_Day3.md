**Data source:** U.S. Geological Survey, for highest and lowest points,
"Elevations and Distances in the United States," April 2005. retrieved
on 31-01-2018 from
<https://www.census.gov/library/publications/2011/compendia/statab/131ed/geography-environment.html>

**Description of data cleaning steps taken:**

1.  Move variable names to the appropriate column (move cell [4,5] to
    cell [4,6]).
2.  Remove column 5.
3.  Column 7 - text facet/text filter - search in filter to (\1)
    - edit matches found to nothing ((\1) to ) - apply.
4.  follow step 3. for column 8
5.  remove/edit manually row 15 in column 8 or follow step 3. with a
    adjusted search in text filter for (Z).

**Code of data cleaning steps:**

\[ { "op": "core/column-move", "description": "Move column Column 6 to
position 4", "columnName": "Column 6", "index": 4 }, { "op":
"core/column-removal", "description": "Remove column Column 5",
"columnName": "Column 5" }, { "op": "core/mass-edit", "description":
"Mass edit cells in column Column 7", "engineConfig": { "mode":
"record-based", "facets": \[ { "mode": "text", "invert": false,
"caseSensitive": false, "query": "(\\1)", "name": "Column 7", "type":
"text", "columnName": "Column 7" } \] }, "columnName": "Column 7",
"expression": "value", "edits": \[ { "fromBlank": false, "fromError":
false, "from": \[ "(\\1)" \], "to": "" } \] }, { "op": "core/mass-edit",
"description": "Mass edit cells in column Column 7", "engineConfig": {
"mode": "record-based", "facets": \[ { "mode": "text", "invert": false,
"caseSensitive": false, "query": "(\\1)", "name": "Column 8", "type":
"text", "columnName": "Column 8" } \] }, "columnName": "Column 7",
"expression": "value", "edits": \[ { "fromBlank": true, "fromError":
false, "from": \[\], "to": "" } \] }, { "op": "core/mass-edit",
"description": "Mass edit cells in column Column 8", "engineConfig": {
"mode": "record-based", "facets": \[ { "mode": "text", "invert": false,
"caseSensitive": false, "query": "(\\1)", "name": "Column 8", "type":
"text", "columnName": "Column 8" } \] }, "columnName": "Column 8",
"expression": "value", "edits": \[ { "fromBlank": false, "fromError":
false, "from": \[ "(\\1)" \], "to": "" } \] }\]
