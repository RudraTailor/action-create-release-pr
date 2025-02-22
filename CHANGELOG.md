# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [1.4.3]
### Changed
- Bump `@actions/core` ([#102](https://github.com/MetaMask/action-create-release-pr/pull/102))

## [1.4.2]
### Changed
- Resolve GitHub action deprecation warnings ([#98](https://github.com/MetaMask/action-create-release-pr/pull/98), [#100](https://github.com/MetaMask/action-create-release-pr/pull/100))
  - GitHub actions have been updated to v3, and the deprecated `set-output` command is no longer used.

## [1.4.1]
### Fixed
- Handle GitHub being slow to create a pull request ([#96](https://github.com/MetaMask/action-create-release-pr/pull/96))

## [1.4.0]
### Changed
- Resolve workspaces recursively for better Yarn 3 support ([#85](https://github.com/MetaMask/action-create-release-pr/pull/85))

## [1.3.0]
### Fixed
- Synchronize monorepo packages for versions in range 0.x.x ([#80](https://github.com/MetaMask/action-create-release-pr/pull/80))
  - Before this change, monorepo packages on major version `0` would break if any sibling packages contained breaking changes, which is permitted by SemVer.

## [1.2.0]
### Added
- Instructions for adding new packages to monorepos ([#74](https://github.com/MetaMask/action-create-release-pr/pull/74))
- Draft PR status option ([#76](https://github.com/MetaMask/action-create-release-pr/pull/76))

## [1.1.0]
### Added
- Write file identifying the initiator of the workflow using this action ([#72](https://github.com/MetaMask/action-create-release-pr/pull/72))
  - This is can be used to upload the artifact required by [MetaMask/action-require-additional-reviewer](https://github.com/MetaMask/action-require-additional-reviewer) in subsequent workflows.

### Changed
- Prevent `Uncategorized` change category from appearing in new releases ([#69](https://github.com/MetaMask/action-create-release-pr/pull/69))

## [1.0.2]
### Changed
- Bump `@metamask/auto-changelog` from `2.3.0` to `2.4.0` ([#59](https://github.com/MetaMask/action-create-release-pr/pull/59))

## [1.0.1]
### Changed
- Improve usage instructions ([#53](https://github.com/MetaMask/action-create-release-pr/pull/53))

### Fixed
- Error logging on Action failure ([#56](https://github.com/MetaMask/action-create-release-pr/pull/56))

## [1.0.0]
### Uncategorized
- First stable release

### Changed
- Default release branch prefix ([#49](https://github.com/MetaMask/action-create-release-pr/pull/49))
  - The default prefix is now `release/`, matching [`action-publish-release@v1`](https://github.com/MetaMask/action-publish-release).

### Fixed
- Faulty usage instructions in readme ([#48](https://github.com/MetaMask/action-create-release-pr/pull/48))

## [0.1.1]
### Fixed
- This action ([#42](https://github.com/MetaMask/action-create-release-pr/pull/42))
  - Due to a poorly formatted Bash invocation in `action.yml`, this Action was completely broken.

## [0.1.0]
### Added
- Add `release-branch-prefix` input ([#38](https://github.com/MetaMask/action-create-release-pr/pull/38))
  - This matches the name of the corresponding input to [MetaMask/action-publish-release@v0.1.0](https://github.com/MetaMask/action-publish-release).

### Changed
- Remove " RC" suffix from PR title ([#39](https://github.com/MetaMask/action-create-release-pr/pull/39))
  - The PR title is now just the SemVer version of the release.

## [0.0.20]
### Changed
- **(BREAKING)** Change release branch prefix from 'release-v' to 'automation_release-' ([#35](https://github.com/MetaMask/action-create-release-pr/pull/35))

### Fixed
- Changelog updating in monorepos and repositories with merge commits ([#33](https://github.com/MetaMask/action-create-release-pr/pull/33))
  - Done by updating `@metamask/auto-changelog` to `2.3.0`. See [MetaMask/auto-changelog#87](https://github.com/MetaMask/auto-changelog/pull/87) for details.

## [0.0.19]
### Fixed
- Monorepo package diffing ([#31](https://github.com/MetaMask/action-create-release-pr/pull/31))
  - In ([#20](https://github.com/MetaMask/action-create-release-pr/pull/20)), we started returning the cached result for the first diffed package for every diffed package.

## [0.0.18]
### Fixed
- Changelog updating ([#28](https://github.com/MetaMask/action-create-release-pr/pull/28))
  - The updated changelog content was never written to disk.

## [0.0.17]
### Changed
- **(BREAKING)** Re-implement in TypeScript, add monorepo support ([#15](https://github.com/MetaMask/action-create-release-pr/pull/15))
- Use `workspaces` manifest entry to find workspaces ([#20](https://github.com/MetaMask/action-create-release-pr/pull/20))
- Add `@lavamoat/allow-scripts` and `setup` command ([#21](https://github.com/MetaMask/action-create-release-pr/pull/21))
- Add README description ([#22](https://github.com/MetaMask/action-create-release-pr/pull/22))
- Remove package manager restriction ([#23](https://github.com/MetaMask/action-create-release-pr/pull/23))
  - Previously, use of Yarn `^1.0.0` was mandated.
- Migrate various utilities to `@metamask/action-utils` ([#24](https://github.com/MetaMask/action-create-release-pr/pull/24))

## [0.0.16]
### Uncategorized
- First semi-stable release. Polyrepos only.

[Unreleased]: https://github.com/MetaMask/action-create-release-pr/compare/v1.4.3...HEAD
[1.4.3]: https://github.com/MetaMask/action-create-release-pr/compare/v1.4.2...v1.4.3
[1.4.2]: https://github.com/MetaMask/action-create-release-pr/compare/v1.4.1...v1.4.2
[1.4.1]: https://github.com/MetaMask/action-create-release-pr/compare/v1.4.0...v1.4.1
[1.4.0]: https://github.com/MetaMask/action-create-release-pr/compare/v1.3.0...v1.4.0
[1.3.0]: https://github.com/MetaMask/action-create-release-pr/compare/v1.2.0...v1.3.0
[1.2.0]: https://github.com/MetaMask/action-create-release-pr/compare/v1.1.0...v1.2.0
[1.1.0]: https://github.com/MetaMask/action-create-release-pr/compare/v1.0.2...v1.1.0
[1.0.2]: https://github.com/MetaMask/action-create-release-pr/compare/v1.0.1...v1.0.2
[1.0.1]: https://github.com/MetaMask/action-create-release-pr/compare/v1.0.0...v1.0.1
[1.0.0]: https://github.com/MetaMask/action-create-release-pr/compare/v0.1.1...v1.0.0
[0.1.1]: https://github.com/MetaMask/action-create-release-pr/compare/v0.1.0...v0.1.1
[0.1.0]: https://github.com/MetaMask/action-create-release-pr/compare/v0.0.20...v0.1.0
[0.0.20]: https://github.com/MetaMask/action-create-release-pr/compare/v0.0.19...v0.0.20
[0.0.19]: https://github.com/MetaMask/action-create-release-pr/compare/v0.0.18...v0.0.19
[0.0.18]: https://github.com/MetaMask/action-create-release-pr/compare/v0.0.17...v0.0.18
[0.0.17]: https://github.com/MetaMask/action-create-release-pr/compare/v0.0.16...v0.0.17
[0.0.16]: https://github.com/MetaMask/action-create-release-pr/releases/tag/v0.0.16
