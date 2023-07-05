# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.4.0] - 2023-07-05

### Changed

- Replace icon and add logo.
- Update dependency giantswarm/linkerd-control-plane-app to v1.0.0
- Update dependency giantswarm/linkerd2-cni-app to v1.0.0
- Update dependency giantswarm/linkerd-viz-app to v1.0.0
- Update dependency giantswarm/linkerd-multicluster-app to v0.11.0
- Update dependency giantswarm/linkerd-multicluster-link-app to v0.11.0

## [0.3.1] - 2023-04-12

### Changed

- Promote bundle to stable catalog.

## [0.3.0] - 2023-03-09

### Changed

- Update dependency giantswarm/linkerd-control-plane-app to v0.11.0
- Update dependency giantswarm/linkerd-viz-app to v0.9.0
- Update dependency giantswarm/linkerd-multicluster-app to v0.10.0
- Update dependency giantswarm/linkerd-multicluster-link-app to v0.10.0
- Update dependency giantswarm/linkerd2-cni-app to v0.10.0

## [0.2.0] - 2023-03-08

### Changed

- Update dependency giantswarm/linkerd-control-plane-app to v0.10.0
- Update dependency giantswarm/linkerd-multicluster-app to v0.9.1
- Update dependency giantswarm/linkerd2-cni-app to v0.9.0

## [0.1.2] - 2023-02-28

### Added

- Added dependencies between apps ([#16](https://github.com/giantswarm/linkerd-bundle/pull/16)).
  - linkerd-control-plane and linkerd2-cni
  - linkerd-viz and linkerd-control-plane
  - linkerd-multicluster and linkerd-control-plane

## [0.1.1] - 2023-02-16

### Fixed

- Remove pod-security annotation until work on PSS is done ([#13](https://github.com/giantswarm/linkerd-bundle/pull/13)).

## [0.1.0] - 2023-02-14

### Added

- Added examples ([#11](https://github.com/giantswarm/linkerd-bundle/pull/11)).
- Added linkerd-multicluster and linkerd-multicluster-link apps ([#10](https://github.com/giantswarm/linkerd-bundle/pull/10)).
- Added linkerd-viz app ([#8](https://github.com/giantswarm/linkerd-bundle/pull/8)).
- Added linkerd-control-plane app ([#6](https://github.com/giantswarm/linkerd-bundle/pull/6)).
- Added App CR example in README ([#5](https://github.com/giantswarm/linkerd-bundle/pull/5))
- Added linkerd2-cni app with minimal configuration ([#4](https://github.com/giantswarm/linkerd-bundle/pull/4)).
- Added apps templates and helpers ([#3](https://github.com/giantswarm/linkerd-bundle/pull/3)).
- Added initial repo configuration.

[Unreleased]: https://github.com/giantswarm/linkerd-bundle/compare/v0.4.0...HEAD
[0.4.0]: https://github.com/giantswarm/linkerd-bundle/compare/v0.3.1...v0.4.0
[0.3.1]: https://github.com/giantswarm/linkerd-bundle/compare/v0.3.0...v0.3.1
[0.3.0]: https://github.com/giantswarm/linkerd-bundle/compare/v0.2.0...v0.3.0
[0.2.0]: https://github.com/giantswarm/linkerd-bundle/compare/v0.1.2...v0.2.0
[0.1.2]: https://github.com/giantswarm/linkerd-bundle/compare/v0.1.1...v0.1.2
[0.1.1]: https://github.com/giantswarm/linkerd-bundle/compare/v0.1.0...v0.1.1
[0.1.0]: https://github.com/giantswarm/linkerd-bundle/releases/tag/v0.1.0
