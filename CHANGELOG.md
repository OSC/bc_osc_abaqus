# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](http://keepachangelog.com/en/1.0.0/)
and this project adheres to [Semantic Versioning](http://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.10.0] - 2023-01-09

- Support for partical access to hugemem nodes in [23](https://github.com/OSC/bc_osc_abaqus/pull/23).

## [0.9.2] - 2022-04-08

- Added abaques CAE licens in [20](https://github.com/OSC/bc_osc_abaqus/pull/20).
- Use the newer packaging scheme in [19](https://github.com/OSC/bc_osc_abaqus/pull/19).


## [0.9.1] - 2021-12-17

### Fixed
- [17](https://github.com/OSC/bc_osc_abaqus/pull/17) corrects using setting mins and maxes.

## [0.9.0] - 2021-12-16
### Changed
- Use the new dynamic JS feature of OnDemand to control the core numbers in forms using the form.yml.erb
  [14](https://github.com/OSC/bc_osc_abaqus/pull/14)

## [0.8.0] - 2020-01-19
### Changed
- [12](https://github.com/OSC/bc_osc_abaqus/pull/12) changed the bc_account text field
  to account which is a select widget with only valid groups as options. This also removed
  owens-slurm cluster and torque related configs.

## [0.7.1] - 2020-11-22
### Changed
- Change Slurm license to be osc in
  [11](https://github.com/OSC/bc_osc_abaqus/pull/11)

## [0.7.0] - 2020-11-18
### Added
- Added owens-slurm cluster to begin migrating Owens to Slurm in
  [10](https://github.com/OSC/bc_osc_abaqus/pull/10)

## [0.6.0] - 2020-05-20
### Changed
- The gitlab ci now clones more consistent builds and deploys to the right repositories

### Added
- abaqus/2020 module as an option

## [0.5.3] - 2019-07-10
### Added
- Added xalt

## [0.5.2] - 2019-06-03
### Changed
- Intel 18.0.3 replaces 16.0.3 and is now always loaded, instead of only when a GPU node is selected

## [0.5.1] - 2019-01-21
### Fixed
- Fixed front end to allow ppn control to remain blank

## [0.5.0] - 2019-01-09
### Added
- Added control to select number of CPUs

## [0.4.0] - 2018-09-13
### Added
- Added Abaqus 2018 to the app.

## [0.3.0] - 2018-03-09
### Added
- Added Abaqus 2017 to the app.
  [#4](https://github.com/OSC/bc_osc_abaqus/issues/4)
- Display ABAQUS output to user if it crashes.
  [#5](https://github.com/OSC/bc_osc_abaqus/issues/5)

### Changed
- Modified the `CHANGELOG.md` formatting.
- Refactored to use new Dashboard ERB templating.
- Updated the date in `LICENSE.txt`.
- Changed the product icon.

### Removed
- Removed support for requesting multiple nodes as we can't verify it will use
  these nodes.

## [0.2.0] - 2017-12-11
### Changed
- Port to Owens Cluster.

## [0.1.0] - 2017-06-14
### Changed
- Refactored for the new Batch Connect app.

## [0.0.8] - 2017-05-15
### Changed
- Future-proof fluxbox configuration.

## [0.0.7] - 2017-05-12
### Changed
- Remove FVWM and added Fluxbox as the window manager.

## [0.0.6] - 2017-04-24
### Changed
- Version assets removing need for `bin/setup`.

## [0.0.5] - 2017-04-21
### Added
- Added `bin/setup` script for easier deployment.

## [0.0.4] - 2017-03-22
### Fixed
- Set working directory to `$HOME` for FVWM as well.

## [0.0.3] - 2017-03-22
### Fixed
- Specify gpus when requesting `vis` node.
- Set working directory to `$HOME`.

## [0.0.2] - 2017-01-10
### Added
- Added more versions of Abaqus.

## 0.0.1 - 2016-12-20
### Added
- Initial release!

[Unreleased]: https://github.com/OSC/bc_osc_abaqus/compare/v0.10.0...HEAD
[0.10.0]: https://github.com/OSC/bc_osc_abaqus/compare/v0.9.2...v0.10.0
[0.9.2]: https://github.com/OSC/bc_osc_abaqus/compare/v0.9.1...v0.9.2
[0.9.1]: https://github.com/OSC/bc_osc_abaqus/compare/v0.9.0...v0.9.1
[0.9.0]: https://github.com/OSC/bc_osc_abaqus/compare/v0.8.0...v0.9.0
[0.8.0]: https://github.com/OSC/bc_osc_abaqus/compare/v0.7.1...v0.8.0
[0.7.1]: https://github.com/OSC/bc_osc_abaqus/compare/v0.7.0...v0.7.1
[0.7.0]: https://github.com/OSC/bc_osc_abaqus/compare/v0.6.0...v0.7.0
[0.6.0]: https://github.com/OSC/bc_osc_abaqus/compare/v0.5.3...v0.6.0
[0.5.3]: https://github.com/OSC/bc_osc_abaqus/compare/v0.5.2...v0.5.3
[0.5.2]: https://github.com/OSC/bc_osc_abaqus/compare/v0.5.1...v0.5.2
[0.5.1]: https://github.com/OSC/bc_osc_abaqus/compare/v0.5.0...v0.5.1
[0.5.0]: https://github.com/OSC/bc_osc_abaqus/compare/v0.4.0...v0.5.0
[0.4.0]: https://github.com/OSC/bc_osc_abaqus/compare/v0.3.0...v0.4.0
[0.3.0]: https://github.com/OSC/bc_osc_abaqus/compare/v0.2.0...v0.3.0
[0.2.0]: https://github.com/OSC/bc_osc_abaqus/compare/v0.1.0...v0.2.0
[0.1.0]: https://github.com/OSC/bc_osc_abaqus/compare/v0.0.8...v0.1.0
[0.0.8]: https://github.com/OSC/bc_osc_abaqus/compare/v0.0.7...v0.0.8
[0.0.7]: https://github.com/OSC/bc_osc_abaqus/compare/v0.0.6...v0.0.7
[0.0.6]: https://github.com/OSC/bc_osc_abaqus/compare/v0.0.5...v0.0.6
[0.0.5]: https://github.com/OSC/bc_osc_abaqus/compare/v0.0.4...v0.0.5
[0.0.4]: https://github.com/OSC/bc_osc_abaqus/compare/v0.0.3...v0.0.4
[0.0.3]: https://github.com/OSC/bc_osc_abaqus/compare/v0.0.2...v0.0.3
[0.0.2]: https://github.com/OSC/bc_osc_abaqus/compare/v0.0.1...v0.0.2
