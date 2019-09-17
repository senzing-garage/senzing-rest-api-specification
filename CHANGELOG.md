# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
[markdownlint](https://dlaa.me/markdownlint/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.7.5] - 2019-09-17

### Changes in 1.7.5

- Changed `configCompatibilityVersion` field in `GET /version` endpoint to be
a string rather than an integer.  When it was specified as an integer, this 
was a mistake in the original release.  NOTE: this will require that client
code be regenerated.

