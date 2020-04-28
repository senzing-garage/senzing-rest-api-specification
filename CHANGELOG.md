# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
[markdownlint](https://dlaa.me/markdownlint/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [2.0.0] - 2020-04-28

### Changed in 2.0.0

- Added many examples to use use with Swagger Editor
  - NOTE: some limitations and bugs with Swagger editor make some of these
    difficult to use with the “Try it Out” function — for example, necessary
    line breaks are removed from “JSON lines” input files when curl commands
    are generated.

- Changed `SzEntityIdentifier` and `SzEntittyIdentifiers` to more formerly
  define the string format for a string-delimited record ID (it is now part of
  the schema definition, not just noted in the parameters).

- Potentially Backward-Compatibility Breaking Changes by API Endpoint:
  - `GET /entity-classes`
  - `GET /entity-classes/{entityClassCode}`
  - `POST /entity-types`
  - `POST /entity-classes/{entityClassCode}/entity-types`
  - `GET /entity-classes/{entityClassCode}/entity-types/{entityTypeCode}`
    - Removed support for any entity class other than ACTOR as it was discovered
      that the underlying product does not properly support entity resolution
      when using entity classes other than ACTOR and it may not for some time.
      This will change if and when additional entity classes are supported.

  - `POST /entity-classes`
    - Removed this operation as it was discovered that the underlying product
      does not fully properly support entity resolution when using entity
      classes other than ACTOR and it may not for some time.  This will change
      if and when additional entity classes are supported.

  - `GET /entities/{entityId}`
  - `GET /data-sources/{dataSourceCode}/records/{recordId}/entity`
    - The `withRelated` parameter is no longer a `boolean` value that accepts
      `true` or `false`.  It now accepts an enumerated value of `NONE`,
      `PARTIAL` or `FULL`.

  - `GET /config/current`
    - Renamed to `GET /configs/active` since “current” is ambiguous with regards
      to the “currently active config” versus the configuration managers
      currently configured “default config”.

  - `GET /config/default`
    - Renamed to `GET /configs/template` since “default” is ambiguous with the
      configuration managers “default config” setting.

  - `GET /entities`
    - Removed the `attr_[PROPERTY_NAME]` parameters and replaced with the
      multi-valued `attr` parameter so that this parameter could better be
      documented in the Open API Spec and examples provided via Swagger Editor.

  - `GET /entity-networks`
    - Changed the default value for `maxDegrees` parameter from 5 to 3

  - `POST /bulk-data/load`
    - Added the single-valued `mapDataSources` parameter which accepts 
      URL-encoded JSON to map the original data sources to target data 
      sources.
    - Replaced the `dataSource_[DATA_SOURCE_CODE]` parameters with the 
      multi-valued `mapDataSource` parameter so that this parameter 
      could better be documented in Open API Spec and examples provided via
      Swagger Editor.
    - Added the single-valued `mapEntityTypes` parameter which accepts 
      URL-encoded JSON to map the original entity types to target entity 
      types.
    - Replaced the `entityType_[ENTITY_TYPE_CODE]` parameters with the
      multi-valued `mapEntityType` parameter so that this parameter could
      better be documented in Open API Spec and examples provided via
      Swagger Editor.

- Other Changes by API Endpoint:
  - `GET /license`
    - Added the previously undocumented (but always-supported) the “withRaw”
      parameter.

  - `GET /version`
    - Added the previously undocumented (but always-supported) the “withRaw”
      parameter.

## [1.8.1] - 2020-04-15

### Changed in 1.8.1

- Added WHY operations
  - `GET /data-sources/{dataSourceCode}/records/{recordId}/entity/why`
  - `GET /entities/{entityId}/why`
  - `GET /why/records`
- Added support for the `withFeatureStatistics` and `withDerivedFeatures`
  parameters across the following endpoints:
  - `GET /data-sources/{dataSourceCode}/records/{recordId}/entity`
  - `GET /data-sources/{dataSourceCode}/records/{recordId}/entity/why`
  - `GET /entities/{entityId}`
  - `GET /entities/{entityId}/why`
  - `GET /why/records`
  - `GET /entity-paths`
  - `GET /entity-networks`
- Added the `featureDetails` property to entity results to support obtaining
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
