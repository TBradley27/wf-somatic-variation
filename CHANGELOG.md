# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [unreleased]
### Added
- GitHub issues template.
- Return of metadata with fastqingress.
- Check of number of samples and barcoded directories.
- Example of how to use the metadata from `fastqingress`.
- Implemented `--version`
- `fastcat_extra_args` option to `fastq_ingress` to pass arbitrary arguments to `fastcat` (defaults to empty string).
- `fastcat_stats` option to `fastq_ingress` to force generation of `fastcat` stats even when the input is only a single file (default is false).
### Changed
- `fastq_ingress` now returns `[metamap, path-to-fastcat-seqs, path-to-fastcat-stats | null]`.
- Bumped base container to v0.2.0.
- Use groovy script to ping after workflow has run.
- Removed sanitize fastq option.
- fastq_ingress now removes unclassified read folders by default.
- Workflow name and version is now more prominently displayed on start
### Fixed
- Output argument in Fastqingress homogenised.
- Sanitize fastq intermittent null object error.
- Add `*.pyc` and `*.pyo` ignores to wf-template .gitignore
### Note
- Bumped version to `v4` to align versioning with Launcher v4

## [v0.2.0]
### Added
- default process label parameter
- Added `params.wf.example_cmd` list to populate `--help`
### Changed
- Update WorkflowMain.groovy to provide better `--help`

## [v0.1.0]
### Changed
- `sample_name` to `sample_id` throughout to mathc MinKNOW samplesheet.
### Added
- Singularity profile include in base config.
- Numerous other changes that have been lost to the mists of time.

## [v0.0.7]
### Added
- Fastqingress module for common handling of (possibly
  multiplexed) inputs.
- Optimized container size through removal of various
  conda cruft.
### Changed
- Use mamba by default for building conda environments.
- Cut down README to items specific to workflow.
### Fixed
- Incorrect specification of conda environment file in Nextflow config.

## [v0.0.6]
### Changed
- Explicitely install into base conda env

## [v0.0.5]
### Added
- Software versioning report example.

## [v0.0.4]
### Changed
- Version bump to test CI.

## [v0.0.3]
### Changed
- Moved all CI to templates.
- Use canned aplanat report components.

## [v0.0.2]
### Added
- CI release checks.
- Create pre-releases in CI from dev branch.

## [v0.0.1]

First release.
