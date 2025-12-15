[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![CI](https://github.com/ultrasardine/OpenVisionKit/workflows/Continuous%20Integration/badge.svg)](https://github.com/ultrasardine/OpenVisionKit/actions)
[![OVK Discord](https://badgen.net/discord/online-members/8azsNh6rsX)](https://discord.gg/8azsNh6rsX)
[![Releases](https://img.shields.io/github/downloads/ultrasardine/OpenVisionKit/total)](https://github.com/ultrasardine/OpenVisionKit/releases/latest)
![Windows](https://img.shields.io/badge/Windows-✅-green)
![Linux](https://img.shields.io/badge/Linux-✅-green)
![macOS](https://img.shields.io/badge/macOS-🚧-yellow)

---------------

## 🚨 Community Fork Notice

**OpenVisionKit** is a community-driven, open source video processing library that evolved from the original LiveVisionKit project. When the original project by Crowsinc went on indefinite pause, the community stepped up to continue development as a **volunteer-driven, non-commercial project** with focus on:

- ✅ **macOS Support** - Adding full macOS build and runtime support
- 🔒 **Security Enhancements** - Improved security practices and vulnerability management
- 🏗️ **Modern Standards** - Updated to current C++20 and industry best practices
- 🤝 **Community Driven** - Open source governance and contribution guidelines
- 🆓 **No Funding Required** - Pure community effort with no commercial backing

**Original Project**: [Crowsinc/LiveVisionKit](https://github.com/Crowsinc/LiveVisionKit) | **OpenVisionKit**: [ultrasardine/OpenVisionKit](https://github.com/ultrasardine/OpenVisionKit)

> **Note**: OpenVisionKit operates entirely through volunteer contributions. We do not accept donations or have any funding mechanisms. All development is done by community members in their spare time.

---------------
![OpenVisionKit](/Assets/LiveVisionKit_Logo.png)
---------------
OpenVisionKit (OVK) is a set of real-time video processing filters for manipulating and enhancing livestreams or recorded videos. Features include video stabilization, adaptive de-blocking, lens correction, image enhancement, and more. OpenVisionKit may be used via the OBS-Studio plugin, with more options coming in the future!

## 🚀 Quick Links

- **📥 Download Latest Release**: [GitHub Releases](https://github.com/ultrasardine/OpenVisionKit/releases)
- **📖 Documentation**: [Project Wiki](https://github.com/ultrasardine/OpenVisionKit/wiki)
- **🔧 Build Instructions**: [Build Guide](https://github.com/ultrasardine/OpenVisionKit/wiki/Build-Guide)
- **🐛 Report Issues**: [Issue Tracker](https://github.com/ultrasardine/OpenVisionKit/issues)
- **💬 Community Support**: [Discord Server](https://discord.gg/8azsNh6rsX)
- **🤝 Contributing**: [Contributing Guide](CONTRIBUTING.md)
- **🔒 Security**: [Security Policy](SECURITY.md)

## 📋 Table of Contents

- [Features](#features)
- [Platform Support](#platform-support)
- [Installation](#installation)
- [Building from Source](#building-from-source)
- [Usage](#usage)
- [Contributing](#contributing)
- [Community](#community)
- [License](#license)

## ✨ Features

OpenVisionKit provides real-time video processing capabilities including:

- **🎯 Video Stabilization** - Advanced stabilization algorithms for smooth footage
- **🔧 Adaptive De-blocking** - Intelligent artifact removal and quality enhancement
- **📐 Lens Correction** - Distortion correction and geometric adjustments
- **🎨 Image Enhancement** - Color correction, contrast, and brightness optimization
- **⚡ Real-time Processing** - Optimized for live streaming (<33ms per frame)
- **🔌 OBS Studio Integration** - Seamless plugin for popular streaming software
- **🎬 Batch Processing** - Command-line tool for video file processing

## 🖥️ Platform Support

| Platform | Status | Architecture | Notes |
|----------|--------|--------------|-------|
| **Windows** | ✅ Stable | x64 | Windows 10+ |
| **Linux** | ✅ Stable | x64 | Ubuntu 18.04+ |
| **macOS** | 🚧 In Development | x64, ARM64 | macOS 10.15+ |

### macOS Support Progress

We're actively working on full macOS support as a community effort! Track progress in [Issue #1](https://github.com/ultrasardine/OpenVisionKit/issues/1).

**Current Status:**
- ✅ Build system adaptation
- 🚧 Dependency management (Homebrew)
- 🚧 OBS plugin integration
- 🚧 AVFoundation framework support
- ⏳ Code signing and distribution

*Progress depends on volunteer contributor availability and community testing.*

## 📦 Installation

### Pre-built Releases

Download the latest community-built release for your platform from [GitHub Releases](https://github.com/ultrasardine/OpenVisionKit/releases).

*Note: Releases are built and tested by community volunteers. Windows and Linux builds are currently available, with macOS support in development.*

### OBS Studio Plugin

1. Download the appropriate release for your platform
2. Extract the plugin files to your OBS plugins directory:
   - **Windows**: `%APPDATA%\obs-studio\plugins\`
   - **Linux**: `~/.config/obs-studio/plugins/`
   - **macOS**: `~/Library/Application Support/obs-studio/plugins/`
3. Restart OBS Studio
4. Find OpenVisionKit filters in the "Filters" menu

### Package Managers

Package manager support is planned for future releases:

```bash
# Homebrew (macOS) - Planned
brew install ultrasardine/tap/openvisionkit

# Chocolatey (Windows) - Planned  
choco install openvisionkit

# Snap (Linux) - Planned
snap install openvisionkit
```

*Note: Package manager distribution depends on community contributions and maintainer availability.*


## 🏗️ Building from Source

### Prerequisites

- **C++20 compatible compiler** (GCC 10+, Clang 12+, MSVC 2019+)
- **CMake 3.16+**
- **OpenCV 4.8.0+**
- **Eigen3 3.4+**
- **Qt5 5.15+**

### Quick Build

```bash
# Clone the repository
git clone https://github.com/ultrasardine/OpenVisionKit.git
cd OpenVisionKit

# Install dependencies (platform-specific)
./Scripts/setup_deb.sh      # Linux
./Scripts/setup_macos.sh    # macOS (in development)
.\Scripts\setup_w64.ps1     # Windows

# Build
mkdir build && cd build
cmake ..
cmake --build . -j$(nproc)  # Linux/macOS
cmake --build . -j           # Windows
```

For detailed build instructions, see our community-maintained [Build Guide](https://github.com/ultrasardine/OpenVisionKit/wiki/Build-Guide).

## 🎯 Usage

### OBS Studio Plugin

1. Install the plugin (see [Installation](#installation))
2. In OBS Studio, right-click on a source
3. Select "Filters" → "Effect Filters"
4. Add OpenVisionKit filters (Stabilization, De-blocking, etc.)
5. Configure filter settings as needed

### Command Line Tool

```bash
# Process a video file
./openvisionkit-cli input.mp4 output.mp4 --stabilize --deblock

# Batch process multiple files
./openvisionkit-cli *.mp4 --output-dir processed/ --stabilize
```

## 🎬 Demonstrations

These videos showcase OpenVisionKit filters in various real-world scenarios:

- **🎮 VR Stabilization**: [YouTube Demo](https://youtu.be/NfL5KXUfUko)
- **🎥 IRL Streaming**: [YouTube Demo](https://youtu.be/se3dSCvFdXc)
- **💻 Tech Content**: [YouTube Demo](https://youtu.be/z3ujzoVfejw)
- **🔧 De-blocking Filter**: [YouTube Demo](https://youtu.be/LCrVeJ-H1IY)

*Filter quality varies depending on content type and scene characteristics.*

## 🤝 Contributing

We welcome contributions from the community! Here's how you can help:

### Ways to Contribute

- 🐛 **Report Bugs**: Use our [issue tracker](https://github.com/ultrasardine/OpenVisionKit/issues)
- ✨ **Suggest Features**: Submit feature requests with use cases
- 💻 **Code Contributions**: Fix bugs, add features, improve performance
- 📚 **Documentation**: Improve guides, add examples, fix typos
- 🌐 **Translations**: Help translate on [Crowdin](https://crowdin.com/project/openvisionkit)
- 🧪 **Testing**: Test on different platforms and report issues

### Getting Started

1. Read our [Contributing Guide](CONTRIBUTING.md)
2. Check the [Code of Conduct](CODE_OF_CONDUCT.md)
3. Look for [good first issues](https://github.com/ultrasardine/OpenVisionKit/labels/good%20first%20issue)
4. Join our [Discord](https://discord.gg/8azsNh6rsX) for discussions

### Development Standards

- **Safety First**: Follow memory safety and thread safety guidelines
- **Performance**: Maintain real-time processing constraints
- **Testing**: Add tests for new functionality
- **Documentation**: Update docs for user-facing changes
- **Code Quality**: Follow C++20 standards and project conventions

## 👥 Community

### Get Support

- **💬 Discord**: [Join our server](https://discord.gg/8azsNh6rsX) for real-time help
- **📋 GitHub Issues**: [Report bugs and request features](https://github.com/ultrasardine/OpenVisionKit/issues)
- **📖 Wiki**: [Browse documentation](https://github.com/ultrasardine/OpenVisionKit/wiki)
- **📧 Email**: For security issues, see [Security Policy](SECURITY.md)

### Contributors

Thanks to all volunteer contributors who help make OpenVisionKit better! 🎉

This project exists entirely through community contributions. Every bug report, feature request, code contribution, and documentation improvement helps the project grow.

<!-- Contributors will be automatically listed here -->

### Recognition

- **🏆 Hall of Fame**: Major contributors recognized in releases
- **🎖️ Discord Roles**: Active contributors get special roles  
- **📝 Changelog**: All contributions documented in [CHANGELOG.md](CHANGELOG.md)
- **🙏 Acknowledgment**: All contributors credited in project documentation

*We believe in recognizing every contribution, no matter how small!*

## 📄 License

OpenVisionKit is licensed under the [GNU General Public License v3.0](LICENSE).

### What this means:

- ✅ **Free to use** for any purpose
- ✅ **Free to modify** and distribute
- ✅ **Source code included** with all distributions
- ⚠️ **Copyleft**: Derivative works must also be GPL v3
- ⚠️ **No warranty**: Software provided "as is"

For more details, see the [full license text](LICENSE).

## 🔒 Security

Security is important to us. If you discover a security vulnerability:

- **Don't** create a public issue
- **Do** report it privately via our [Security Policy](SECURITY.md)
- **Do** allow time for us to address it before disclosure

## 📊 Project Stats

![GitHub stars](https://img.shields.io/github/stars/ultrasardine/OpenVisionKit?style=social)
![GitHub forks](https://img.shields.io/github/forks/ultrasardine/OpenVisionKit?style=social)
![GitHub issues](https://img.shields.io/github/issues/ultrasardine/OpenVisionKit)
![GitHub pull requests](https://img.shields.io/github/issues-pr/ultrasardine/OpenVisionKit)

---

## 🙏 Acknowledgments

- **Original Creator**: Thanks to Crowsinc for creating LiveVisionKit and making it open source
- **Community Contributors**: All the volunteers who contribute code, documentation, testing, and support
- **Open Source Libraries**: OpenCV, Eigen3, Qt5, and other dependencies that make this project possible
- **Users and Testers**: Everyone who uses OpenVisionKit and provides feedback

---

**Made with ❤️ by volunteers around the world**

*A community-driven project empowering creators with professional-grade video processing tools*

**No funding • No ads • No tracking • Just great open source software** 🚀
