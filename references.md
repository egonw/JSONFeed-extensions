# References extension

This extension has been developed by ...

Following the [JSON Feed 1.1 specification](https://www.jsonfeed.org/version/1.1/), this document
describes a extension for items for references to sources cited in items. The extension
name is `_references`.

An simple example `item` with a `_references` section:

```json
{
  "id": "https://doi.org/10.59350/krw9n-dv417",
  "url": "https://chem-bla-ics.linkedchemistry.info/2025/08/09/one-million-iupac-names-4.html",
  "title": "One Million IUPAC names #4: a lot is happening",
  "_references": [
    {
      "url": "https://doi.org/10.5281/zenodo.16755947",
      "doi": "10.5281/zenodo.16755947"
    }
  ]
}
```

## Goals

The goal of this extension is to make references cited the text of items in the feed easier to handle.

## The Structure of the Extension

A `_references` extension of an `item` is an array, and it is optional (as extensions are).
Each reference includes:

* `url` (required, string) is a unique URL for that reference. An URL based on an persistant unique
  identifier is therefore recommended.
* `doi` (optional, string) is the Digital Object Identifier (DOI) for the reference.

## Citation Typing Ontology intent annotation

Optionally, each reference can be linked to one or more [Citation Typing Ontology](http://purl.org/spar/cito/)
citation intent annotations. Therefore, each items in the `_references` array also allows
for the following object:

* `cito` (optional, array of strings) is an array of strings where each string is the local
  name of a CiTO annotation, e.g. `cites`, `usesMethodIn`, and `citesAsRecommendedReading`.

A simple example:

```json
"_references": [
  {
    "url": "https://doi.org/10.5281/zenodo.16755947",
    "doi": "10.5281/zenodo.16755947",
    "cito": [
      "citesAsRecommendedReading"
    ]
  }
]
```

## Reviewers

## See Also

## Changes

Version 1 — 2025-08-10

* Initial version.
