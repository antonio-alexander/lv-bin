# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.1.0] - 2021-01-09

- Updated the cmd generate utility to provide feedback on non-zero code or non-zero standard error.
- Added ability to resolve system paths with a filename (including extension)
- Modified the logic of the private fg_paths to not automatically insert <application_director>/data/bin on first run if the initial item is empty. It also now has logic to detect if the path is empty (and not add it) and won't add duplicate paths at runtime.
- Removed all of the lv-bin packages and moved them to their own repos.

## [1.0.0] - 

- Initial release
