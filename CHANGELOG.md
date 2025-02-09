# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/)
and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added

### Changed

### Deprecated

### Removed

### Fixed
- `ObjectDisposedException` that can happen when matching the same response multiple times, and client disposes the response.

### Security

## 2.0.0

### Added

- Added support for the `IHttpClientBuilder` methods.
- Added support for `HttpRecorderContext`.

### Changed

- [BREAKING]: Removed the `innerHandler` parameter in the `RequestsSignatureDelegatingHandler` constructor; you must now use the `InnerHandler` property.
- [BREAKING]: Moved from NewtonSoft to System.Text.Json serialization.

### Deprecated

### Removed

### Fixed

- `ObjectDisposedException` that can happen on complex interactions involving multiple requests/responses that are being disposed.
- `ArgumentException`: *Object is not a array with the same number of elements as the array to compare it* to when comparing requests by content with different body sizes.

### Security

## 1.1.0

### Added

- `IInteractionAnonymizer` to anonymize interactions (with `RulesInteractionAnonymizer` implementation)

### Changed

### Deprecated

### Removed

### Fixed

### Security

## 1.0.0

### Added

- `HttpRecorderDelegatingHandler` that drives the interaction recording with 4 record modes: Auto, Record, Replay, Passthrough
- `HttpArchiveInteractionRepository` that store interactions using HAR format
- `RulesMatcher` to allow the customization of interactions matching

### Changed

### Deprecated

### Removed

### Fixed

### Security
