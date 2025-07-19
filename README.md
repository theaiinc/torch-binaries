# Torch Binaries Repository

This repository hosts pre-compiled binaries for the **Torch CLI** (`@theaiinc/torch`), a powerful AI coding agent command-line interface.

## 🎯 Purpose

This repository serves as the binary distribution hub for the Torch CLI npm packages. When users install `@theaiinc/torch` or platform-specific packages like `@theaiinc/torch-darwin-arm64`, the npm packages download the appropriate binary from this repository's releases.

## 📦 Supported Platforms

- **Windows x64**: `torch-win32-x64`
- **macOS ARM64 (Apple Silicon)**: `torch-darwin-arm64`
- **Linux x64**: `torch-linux-x64`

## 🔄 How It Works

### For Users

1. **Install via npm**: `npm install -g @theaiinc/torch`
2. **Automatic Download**: The npm package's `postinstall.js` script automatically downloads the correct binary for your platform from this repository's releases
3. **Ready to Use**: The binary is placed in `bin/torch` and made executable

### For Developers

The npm packages use a postinstall script that:

- Detects the user's platform (OS + architecture)
- Downloads the appropriate binary from the latest release
- Places it in the correct location
- Makes it executable

## 🚀 Release Process

### Creating a New Release

1. **Build Binaries**: Build the Torch CLI for all supported platforms
2. **Create Release**: Go to [Releases](https://github.com/theaiinc/torch-binaries/releases)
3. **Upload Assets**: Upload binaries with these exact names:
   - `torch-win32-x64` (Windows x64)
   - `torch-darwin-arm64` (macOS ARM64)
   - `torch-linux-x64` (Linux x64)
4. **Tag Version**: Use semantic versioning (e.g., `v0.0.41`)
5. **Publish**: Make the release public

### Version Synchronization

- **Release tags** must match the npm package versions
- **Binary names** must match the platform-specific npm package names
- **Asset names** must exactly match the expected download names

## 🐛 Reporting Issues

### All Torch Issues

Please report **all issues** related to Torch CLI here: **[Create an Issue](https://github.com/theaiinc/torch/issues)**

This includes:

- **Binary downloads failing**
- **Platform compatibility problems**
- **Missing binaries for your platform**
- **Binary execution errors**
- **Version mismatches**
- **Torch CLI features and bugs**
- **Installation problems**
- **Configuration issues**
- **Performance problems**
- **Any other Torch-related issues**

## 📋 Issue Guidelines

When reporting binary-related issues, please include:

1. **Platform Information**:

   - Operating System and version
   - Architecture (x64, arm64, etc.)
   - Node.js version

2. **Error Details**:

   - Complete error message
   - Steps to reproduce
   - Expected vs actual behavior

3. **Installation Context**:
   - How you installed Torch (npm, direct download, etc.)
   - Any custom configuration

## 🔧 Troubleshooting

### Common Issues

**Binary Download Fails**

- Check your internet connection
- Verify the release exists and is public
- Ensure the binary asset name matches your platform

**Permission Denied**

- The binary should be automatically made executable
- Try: `chmod +x /path/to/torch`

**Version Mismatch**

- Ensure npm package version matches release tag
- Try reinstalling: `npm uninstall -g @theaiinc/torch && npm install -g @theaiinc/torch`

### Manual Installation

If automatic download fails, you can manually download and install:

1. Go to [Releases](https://github.com/theaiinc/torch-binaries/releases)
2. Download the appropriate binary for your platform
3. Make it executable: `chmod +x torch-{platform}`
4. Move to a directory in your PATH: `sudo mv torch-{platform} /usr/local/bin/torch`

## 🤝 Contributing

### Building Binaries

To contribute new binaries or updates:

1. **Build Process**: Follow the build instructions in the main Torch repository
2. **Testing**: Test the binary on the target platform
3. **Naming**: Ensure the binary name matches the expected format
4. **Release**: Create a new release with the correct tag and assets

### Platform Support

Interested in adding support for a new platform?

1. **Check Demand**: Open an issue to discuss the need
2. **Build Support**: Ensure the build system supports the platform
3. **Testing**: Provide testing on the target platform
4. **Documentation**: Update this README with the new platform

## 📄 License

This repository is part of the Torch CLI project. See the main Torch repository for license information.

## 🔗 Related Links

- **Main Torch Repository**: [theaiinc/torch](https://github.com/theaiinc/torch)
- **NPM Package**: [@theaiinc/torch](https://www.npmjs.com/package/@theaiinc/torch)
- **Documentation**: See the main Torch repository for comprehensive documentation
