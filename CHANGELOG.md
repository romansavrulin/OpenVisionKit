# Changelog

All notable changes to OpenVisionKit will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

### Added
- macOS build support implementation (in progress)
- Comprehensive open source project compliance
- GitHub issue and PR templates
- Security policy and vulnerability reporting process
- Code of conduct for community guidelines
- Contributing guidelines with development standards
- Industry standards compliance documentation

### Changed
- Enhanced development safety guidelines
- Improved documentation structure
- Updated steering documents with workflow requirements
- **BREAKING**: Project renamed from LiveVisionKit to OpenVisionKit

### Security
- Added security policy and vulnerability disclosure process
- Enhanced build system security features
- Improved input validation requirements

## Project Status

**Note**: OpenVisionKit is a community-driven fork that evolved from the original LiveVisionKit project (which is on indefinite pause by Crowsinc). This community fork under `ultrasardine` continues development with focus on:

- macOS platform support
- Community-driven improvements
- Security and stability enhancements
- Open source best practices compliance

## Previous Releases

For information about previous releases from the original repository, please refer to:
- [Original Release History](https://github.com/Crowsinc/LiveVisionKit/releases)
- [Original Project Wiki](https://github.com/Crowsinc/LiveVisionKit/wiki)

---

## Release Types

### Major Releases (X.0.0)
- Breaking API changes
- Major new features
- Platform support additions
- Significant architecture changes

### Minor Releases (X.Y.0)
- New features and enhancements
- Performance improvements
- New filters or capabilities
- Non-breaking API additions

### Patch Releases (X.Y.Z)
- Bug fixes
- Security patches
- Documentation updates
- Build system improvements

---

## Contributing to Changelog

When contributing changes, please:

1. **Add entries** to the `[Unreleased]` section
2. **Use appropriate categories**: Added, Changed, Deprecated, Removed, Fixed, Security
3. **Follow the format**: Brief description with issue/PR references
4. **Include breaking changes** in the Changed section with clear migration notes
5. **Reference issues/PRs** using `(#123)` format

### Example Entry Format

```markdown
### Added
- New video stabilization algorithm with improved performance (#123)
- macOS support for OBS Studio plugin (#456)

### Changed
- **BREAKING**: Updated VideoFilter API to support async processing (#789)
- Improved memory usage in filter chains by 15% (#101)

### Fixed
- Fixed memory leak in OpenCV integration (#234)
- Resolved thread safety issue in composite filters (#567)

### Security
- Fixed buffer overflow vulnerability in video decoder (#890)
```

---

**Note**: This changelog follows the community fork development. For historical changes from the original project, please refer to the original repository's release notes.