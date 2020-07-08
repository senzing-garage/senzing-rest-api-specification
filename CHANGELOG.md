# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
[markdownlint](https://dlaa.me/markdownlint/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.8.2] - 2020-07-08

### Changed in 1.8.2

- Improved documentation
- Works with senzing versions up to 1.15.6
- Not supported for senzing version 2.0.0 and above

## [1.8.1] - 2020-04-15

### Changed in 1.8.1

- Added WHY operations
  - GET /data-sources/{dataSourceCode}/records/{recordId}/entity/why
  - GET /entities/{entityId}/why
  - GET /why/records
- Added support for the "withFeatureStatistics" and "withDerivedFeatures"
  parameters across the following endpoints:
  - GET /data-sources/{dataSourceCode}/records/{recordId}/entity
  - GET /data-sources/{dataSourceCode}/records/{recordId}/entity/why
  - GET /entities/{entityId
  - GET /entities/{entityId}/why
  - GET /why/records
  - GET /entity-paths
  - GET /entity-networks
- Added the "featureDetails" property to entity results to support obtaining
  the feature ID as well as the feature statistics (if requested).

## [1.8.0] - 2020-03-27

### Changed in 1.8.0

- Adds config modification operations (data sources, entity types, etc...)
- Adds bulk data analyze and load operations

## [1.7.5] - 2019-09-17

### Changes in 1.7.5

- Changed `configCompatibilityVersion` field in `GET /version` endpoint to be
a string rather than an integer.  When it was specified as an integer, this
was a mistake in the original release.  NOTE: this will require that client
code be regenerated.
