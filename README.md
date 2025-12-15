[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](https://www.gnu.org/licenses/gpl-3.0)
[![CI](https://github.com/ultrasardine/LiveVisionKit/workflows/Continuous%20Integration/badge.svg)](https://github.com/ultrasardine/LiveVisionKit/actions)
[![LVK Discord](https://badgen.net/discord/online-members/8azsNh6rsX)](https://discord.gg/8azsNh6rsX)
[![Releases](https://img.shields.io/github/downloads/ultrasardine/LiveVisionKit/total)](https://github.com/ultrasardine/LiveVisionKit/releases/latest)
![Windows](https://img.shields.io/badge/Windows-✅-green)
![Linux](https://img.shields.io/badge/Linux-✅-green)
![macOS](https://img.shields.io/badge/macOS-🚧-yellow)

---------------

## 🚨 Community Fork Notice

This is a **community-maintained fork** of the original LiveVisionKit project. The original project by Crowsinc is on indefinite pause, but this fork continues active development with focus on:

- ✅ **macOS Support** - Adding full macOS build and runtime support
- 🔒 **Security Enhancements** - Improved security practices and vulnerability management
- 🏗️ **Modern Standards** - Updated to current C++20 and industry best practices
- 🤝 **Community Driven** - Open source governance and contribution guidelines

**Original Project**: [Crowsinc/LiveVisionKit](https://github.com/Crowsinc/LiveVisionKit) | **Community Fork**: [ultrasardine/LiveVisionKit](https://github.com/ultrasardine/LiveVisionKit)

---------------
![LiveVisionKit](/Assets/LiveVisionKit_Logo.png)
---------------
LiveVisionKit (LVK) is a set of real-time video processing filters for manipulating and enhancing livestreams or recorded videos. Features include video stabilization, adaptive de-blocking, lens correction, image enhancement, and more. LiveVisionKit may be used via the OBS-Studio plugin, with more options coming in the future!

## 🚀 Quick Links

- **📥 Download Latest Release**: [GitHub Releases](https://github.com/ultrasardine/LiveVisionKit/releases)
- **📖 Documentation**: [Project Wiki](https://github.com/ultrasardine/LiveVisionKit/wiki)
- **🔧 Build Instructions**: [Build Guide](https://github.com/ultrasardine/LiveVisionKit/wiki/Build-Guide)
- **🐛 Report Issues**: [Issue Tracker](https://github.com/ultrasardine/LiveVisionKit/issues)
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

LiveVisionKit provides real-time video processing capabilities including:

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

We're actively working on full macOS support! Track progress in [Issue #1](https://github.com/ultrasardine/LiveVisionKit/issues/1).

- ✅ Build system adaptation
- 🚧 Dependency management (Homebrew)
- 🚧 OBS plugin integration
- 🚧 AVFoundation framework support
- ⏳ Code signing and distribution

## 📦 Installation

### Pre-built Releases

Download the latest release for your platform from [GitHub Releases](https://github.com/ultrasardine/LiveVisionKit/releases).

### OBS Studio Plugin

1. Download the appropriate release for your platform
2. Extract the plugin files to your OBS plugins directory:
   - **Windows**: `%APPDATA%\obs-studio\plugins\`
   - **Linux**: `~/.config/obs-studio/plugins/`
   - **macOS**: `~/Library/Application Support/obs-studio/plugins/`
3. Restart OBS Studio
4. Find LiveVisionKit filters in the "Filters" menu

### Package Managers

```bash
# Homebrew (macOS) - Coming Soon
brew install ultrasardine/tap/livevisionkit

# Chocolatey (Windows) - Coming Soon
choco install livevisionkit

# Snap (Linux) - Coming Soon
snap install livevisionkit
```


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
git clone https://github.com/ultrasardine/LiveVisionKit.git
cd LiveVisionKit

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

For detailed build instructions, see [Build Guide](https://github.com/ultrasardine/LiveVisionKit/wiki/Build-Guide).

## 🎯 Usage

### OBS Studio Plugin

1. Install the plugin (see [Installation](#installation))
2. In OBS Studio, right-click on a source
3. Select "Filters" → "Effect Filters"
4. Add LiveVisionKit filters (Stabilization, De-blocking, etc.)
5. Configure filter settings as needed

### Command Line Tool

```bash
# Process a video file
./livevisionkit-cli input.mp4 output.mp4 --stabilize --deblock

# Batch process multiple files
./livevisionkit-cli *.mp4 --output-dir processed/ --stabilize
```

## 🎬 Demonstrations

These videos showcase LiveVisionKit filters in various real-world scenarios:

- **🎮 VR Stabilization**: [YouTube Demo](https://youtu.be/NfL5KXUfUko)
- **🎥 IRL Streaming**: [YouTube Demo](https://youtu.be/se3dSCvFdXc)
- **💻 Tech Content**: [YouTube Demo](https://youtu.be/z3ujzoVfejw)
- **🔧 De-blocking Filter**: [YouTube Demo](https://youtu.be/LCrVeJ-H1IY)

*Filter quality varies depending on content type and scene characteristics.*

## 🤝 Contributing

We welcome contributions from the community! Here's how you can help:

### Ways to Contribute

- 🐛 **Report Bugs**: Use our [issue tracker](https://github.com/ultrasardine/LiveVisionKit/issues)
- ✨ **Suggest Features**: Submit feature requests with use cases
- 💻 **Code Contributions**: Fix bugs, add features, improve performance
- 📚 **Documentation**: Improve guides, add examples, fix typos
- 🌐 **Translations**: Help translate on [Crowdin](https://crowdin.com/project/livevisionkit)
- 🧪 **Testing**: Test on different platforms and report issues

### Getting Started

1. Read our [Contributing Guide](CONTRIBUTING.md)
2. Check the [Code of Conduct](CODE_OF_CONDUCT.md)
3. Look for [good first issues](https://github.com/ultrasardine/LiveVisionKit/labels/good%20first%20issue)
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
- **📋 GitHub Issues**: [Report bugs and request features](https://github.com/ultrasardine/LiveVisionKit/issues)
- **📖 Wiki**: [Browse documentation](https://github.com/ultrasardine/LiveVisionKit/wiki)
- **📧 Email**: For security issues, see [Security Policy](SECURITY.md)

### Contributors

Thanks to all contributors who help make LiveVisionKit better! 🎉

<!-- Contributors will be automatically listed here -->

### Recognition

- **🏆 Hall of Fame**: Major contributors recognized in releases
- **🎖️ Discord Roles**: Active contributors get special roles
- **📝 Changelog**: All contributions documented in [CHANGELOG.md](CHANGELOG.md)

## 📄 License

LiveVisionKit is licensed under the [GNU General Public License v3.0](LICENSE).

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

![GitHub stars](https://img.shields.io/github/stars/ultrasardine/LiveVisionKit?style=social)
![GitHub forks](https://img.shields.io/github/forks/ultrasardine/LiveVisionKit?style=social)
![GitHub issues](https://img.shields.io/github/issues/ultrasardine/LiveVisionKit)
![GitHub pull requests](https://img.shields.io/github/issues-pr/ultrasardine/LiveVisionKit)

---

**Made with ❤️ by the LiveVisionKit community**

*Empowering creators with professional-grade video processing tools*
