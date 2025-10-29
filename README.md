# DDR VS Code Extension Distribution

This repository provides a public distribution point for downloading and installing the DDR VS Code extension.

## 📦 Download

Download the latest version of the extension from the [Releases](releases/) folder.

## 🚀 Installation Methods

### Method 1: Install from VSIX file (Recommended)

1. **Download** the `.vsix` file from the [releases](releases/) folder
2. **Open VS Code**
3. **Install the extension**:
   - **Option A**: Via Command Palette
     - Press `Ctrl+Shift+P` (Windows/Linux) or `Cmd+Shift+P` (Mac)
     - Type "Extensions: Install from VSIX"
     - Select the downloaded `.vsix` file
   
   - **Option B**: Via Extensions View
     - Click on the Extensions icon in the Activity Bar (or press `Ctrl+Shift+X`)
     - Click on the `...` (More Actions) button at the top of the Extensions view
     - Select "Install from VSIX..."
     - Choose the downloaded `.vsix` file
   
   - **Option C**: Via Command Line
     ```bash
     code --install-extension path/to/extension.vsix
     ```

4. **Reload VS Code** when prompted

### Method 2: Install from VS Code Marketplace

If the extension is published to the VS Code Marketplace:

1. Open VS Code
2. Go to Extensions (`Ctrl+Shift+X` / `Cmd+Shift+X`)
3. Search for "DDR"
4. Click **Install**

## 📋 Requirements

- **VS Code version**: 1.60.0 or higher (check specific extension requirements)
- **Operating System**: Windows, macOS, or Linux

## 🔧 Verification

After installation, verify the extension is active:

1. Open the Extensions view (`Ctrl+Shift+X`)
2. Search for "DDR" in the installed extensions
3. Ensure the extension is enabled

## 📚 Documentation

For detailed documentation, see the [docs](docs/) folder:
- [Installation Guide](docs/INSTALLATION.md) - Detailed installation instructions
- [Troubleshooting](docs/TROUBLESHOOTING.md) - Common issues and solutions
- [Quick Reference](docs/QUICK_REFERENCE.md) - Quick commands and shortcuts
- [Repository Structure](docs/STRUCTURE.md) - Overview of repository layout

## 🆘 Support

If you encounter any issues:
1. Check the [Troubleshooting Guide](docs/TROUBLESHOOTING.md)
2. Open an issue in this repository
3. Contact the development team

## 📄 License

See [LICENSE](LICENSE) file for details.
