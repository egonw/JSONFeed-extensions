# Funding extension

This extension has been developed by ...

Following the [JSON Feed 1.1 specification](https://www.jsonfeed.org/version/1.1/), this document
describes a extension for acknowledgements of grants. The extension
name is `_funding`.

An simple example `item` with a `_funding` section:

```json
{
  "id": "https://doi.org/10.59350/krw9n-dv417",
  "url": "https://chem-bla-ics.linkedchemistry.info/2025/08/09/one-million-iupac-names-4.html",
  "title": "One Million IUPAC names #4: a lot is happening",
  "_funding": [
    {
      "award": {
        "title": "The Virtual Human Platform for Safety Assessment",
        "acronym": "VHP4Safety",
        "uri": "drc.filenumber:nwa129219272"
      },
      "funder": {
        "name": "Dutch Research Council",
        "ror": "04jsz6e67"
      }
    }
  ]
}
```

## Goals



## The Structure of the Extension

## Reviewers

## See Also

## Changes

Version ? — 2025-08-10

* Template
