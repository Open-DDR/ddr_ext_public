# Quick Reference Guide

Quick commands and tips for working with VS Code extensions.

## Installation Commands

### Install from VSIX
```bash
code --install-extension path/to/extension.vsix
```

### Uninstall Extension
```bash
code --uninstall-extension publisher.extension-name
```

### List Installed Extensions
```bash
code --list-extensions
```

### List Extensions with Versions
```bash
code --list-extensions --show-versions
```

## VS Code Commands

### Open Extensions View
- **Windows/Linux**: `Ctrl+Shift+X`
- **macOS**: `Cmd+Shift+X`

### Open Command Palette
- **Windows/Linux**: `Ctrl+Shift+P`
- **macOS**: `Cmd+Shift+P`

### Reload Window
1. Open Command Palette
2. Type: "Developer: Reload Window"
3. Press Enter

## Keyboard Shortcuts

| Action | Windows/Linux | macOS |
|--------|--------------|-------|
| Open Extensions | `Ctrl+Shift+X` | `Cmd+Shift+X` |
| Command Palette | `Ctrl+Shift+P` | `Cmd+Shift+P` |
| Settings | `Ctrl+,` | `Cmd+,` |
| Open Terminal | `` Ctrl+` `` | `` Cmd+` `` |
| Toggle Sidebar | `Ctrl+B` | `Cmd+B` |

## File Locations

### Extensions Directory
- **Windows**: `%USERPROFILE%\.vscode\extensions`
- **macOS**: `~/.vscode/extensions`
- **Linux**: `~/.vscode/extensions`

### User Settings
- **Windows**: `%APPDATA%\Code\User\settings.json`
- **macOS**: `~/Library/Application Support/Code/User/settings.json`
- **Linux**: `~/.config/Code/User/settings.json`

### Workspace Settings
- Located in: `.vscode/settings.json` in your workspace folder

## Checking Version

### VS Code Version
```bash
code --version
```

### Extension Version
1. Open Extensions view
2. Find your extension
3. Version is shown in the extension details

## Common Tasks

### Enable/Disable Extension
1. Open Extensions view (`Ctrl+Shift+X`)
2. Find the extension
3. Click "Disable" or "Enable"

### View Extension Logs
1. Open Output panel: `View > Output`
2. Select extension from dropdown

### Clear Extension Cache
1. Close VS Code
2. Delete cache folder (see File Locations)
3. Restart VS Code

## Troubleshooting Quick Checks

```bash
# Check VS Code version
code --version

# List all extensions
code --list-extensions --show-versions

# Check extension directory
# Windows
dir %USERPROFILE%\.vscode\extensions

# macOS/Linux
ls -la ~/.vscode/extensions
```

## Resources

- Full Installation Guide: [docs/INSTALLATION.md](INSTALLATION.md)
- Troubleshooting: [docs/TROUBLESHOOTING.md](TROUBLESHOOTING.md)
- Release Guide: [docs/RELEASE_GUIDE.md](RELEASE_GUIDE.md)
