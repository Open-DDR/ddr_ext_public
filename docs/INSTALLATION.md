# Installation Guide

This guide provides detailed instructions for installing the DDR VS Code extension.

## Table of Contents
- [Prerequisites](#prerequisites)
- [Installation Methods](#installation-methods)
- [Post-Installation](#post-installation)
- [Updating the Extension](#updating-the-extension)
- [Uninstalling](#uninstalling)

## Prerequisites

Before installing the extension, ensure you have:

- **Visual Studio Code** version 1.60.0 or higher
  - Check your version: `Help > About` or run `code --version`
  - Download latest VS Code: https://code.visualstudio.com/
- **Sufficient disk space** (~10-50 MB depending on the extension)
- **Internet connection** (for downloading the extension)

## Installation Methods

### Method 1: Install from VSIX File (Offline Installation)

This is the recommended method for installing extensions from this repository.

#### Step-by-Step Instructions:

1. **Download the VSIX file**
   - Navigate to the [releases](../releases/) folder
   - Download the latest `.vsix` file (e.g., `ddr-extension-1.0.0.vsix`)
   - Save it to a location you can easily access

2. **Install via VS Code UI**
   
   **Option A: Using Command Palette**
   - Open VS Code
   - Press `Ctrl+Shift+P` (Windows/Linux) or `Cmd+Shift+P` (macOS)
   - Type: `Extensions: Install from VSIX`
   - Press Enter
   - Navigate to and select your downloaded `.vsix` file
   - Click "Install"
   
   **Option B: Using Extensions Panel**
   - Open VS Code
   - Click the Extensions icon in the Activity Bar (left sidebar)
     - Or press `Ctrl+Shift+X` (Windows/Linux) or `Cmd+Shift+X` (macOS)
   - Click the `...` (More Actions) button at the top of the Extensions view
   - Select "Install from VSIX..."
   - Navigate to and select your downloaded `.vsix` file
   - Click "Install"

3. **Install via Command Line**
   
   Open a terminal and run:
   ```bash
   code --install-extension /path/to/ddr-extension-1.0.0.vsix
   ```
   
   **Windows Example:**
   ```cmd
   code --install-extension C:\Downloads\ddr-extension-1.0.0.vsix
   ```
   
   **macOS/Linux Example:**
   ```bash
   code --install-extension ~/Downloads/ddr-extension-1.0.0.vsix
   ```

4. **Reload VS Code**
   - Click "Reload Now" when prompted
   - Or manually reload: `Ctrl+Shift+P` → "Developer: Reload Window"

### Method 2: Install from VS Code Marketplace

If the extension has been published to the marketplace:

1. **Via VS Code UI**
   - Open VS Code
   - Go to Extensions view (`Ctrl+Shift+X` / `Cmd+Shift+X`)
   - Search for "DDR" or the exact extension name
   - Click the **Install** button

2. **Via Command Line**
   ```bash
   code --install-extension publisher.extension-name
   ```

### Method 3: Install from GitHub Release (If Available)

If releases are published on GitHub:

1. Go to the [GitHub Releases](../../releases) page
2. Download the latest `.vsix` file from the release assets
3. Follow the VSIX installation steps from Method 1

## Post-Installation

### Verify Installation

1. **Check Installed Extensions**
   - Open Extensions view (`Ctrl+Shift+X`)
   - Type `@installed` in the search box
   - Look for "DDR" or the extension name
   - The extension should show as "Enabled"

2. **Verify via Command Line**
   ```bash
   code --list-extensions
   ```
   Look for the extension ID in the output.

### Configure the Extension

After installation, you may need to configure the extension:

1. Open Settings: `File > Preferences > Settings` (or `Ctrl+,`)
2. Search for "DDR" or the extension name
3. Configure available settings according to your needs

### Test the Extension

1. Open a relevant file or project
2. Check if extension features are working:
   - Look for new commands in the Command Palette
   - Check for new menu items
   - Verify any status bar items or views

## Updating the Extension

### Update from VSIX File

1. Download the new version's `.vsix` file
2. Install it using the same method as initial installation
   - The new version will automatically replace the old one
3. Reload VS Code when prompted

### Update from Marketplace

If installed from the marketplace:
- VS Code will automatically check for updates
- Click "Update" when a new version is available
- Or manually check: Extensions view → Click the extension → Check for "Update" button

## Uninstalling

### Via VS Code UI

1. Open Extensions view (`Ctrl+Shift+X`)
2. Find the extension
3. Click the gear icon ⚙️
4. Select "Uninstall"
5. Reload VS Code when prompted

### Via Command Line

```bash
code --uninstall-extension publisher.extension-name
```

### Clean Uninstall

To remove all extension data:

1. Uninstall the extension (steps above)
2. Remove extension settings:
   - Open Settings (`Ctrl+,`)
   - Search for the extension name
   - Reset or remove all extension-specific settings
3. Delete workspace-specific settings if needed:
   - Open `.vscode/settings.json` in your workspace
   - Remove extension-related configurations

## Troubleshooting

If you encounter issues during installation, see the [Troubleshooting Guide](TROUBLESHOOTING.md).

## Additional Resources

- [VS Code Extension Documentation](https://code.visualstudio.com/docs/editor/extension-marketplace)
- [VS Code CLI Reference](https://code.visualstudio.com/docs/editor/command-line)
