# ddr_ext_public

This repository provides VS Code extensions for download and installation.

## Installing VS Code Extensions

There are several ways to install VS Code extensions. Choose the method that works best for your needs.

### Method 1: Install from VS Code Marketplace (Recommended)

1. Open Visual Studio Code
2. Click on the Extensions icon in the Activity Bar (or press `Ctrl+Shift+X` / `Cmd+Shift+X`)
3. Search for the extension name in the search box
4. Click the **Install** button

### Method 2: Install from Command Line

You can install extensions using the `code` command:

```bash
code --install-extension <extension-id>
```

**Example:**
```bash
code --install-extension ms-python.python
```

### Method 3: Install from VSIX File

If you have a `.vsix` file (typically downloaded from this repository or GitHub releases):

#### Using VS Code UI:
1. Open Visual Studio Code
2. Go to Extensions view (`Ctrl+Shift+X` / `Cmd+Shift+X`)
3. Click on the `...` (Views and More Actions) menu at the top of the Extensions view
4. Select **Install from VSIX...**
5. Browse to the `.vsix` file and select it

#### Using Command Line:
```bash
code --install-extension path/to/extension.vsix
```

**Example:**
```bash
code --install-extension ddr-extension-1.0.0.vsix
```

## VS Code Extension Folder Structure

Understanding the folder structure helps when developing or troubleshooting extensions:

```
your-extension/
├── .vscode/              # VS Code configuration
│   ├── launch.json       # Debug configuration
│   └── tasks.json        # Build tasks
├── src/                  # Source files
│   └── extension.js      # Main extension file
├── test/                 # Test files
│   └── extension.test.js
├── .gitignore           # Git ignore file
├── .vscodeignore        # Files to exclude from package
├── CHANGELOG.md         # Version history
├── package.json         # Extension manifest
├── README.md            # Extension documentation
└── tsconfig.json        # TypeScript config (if using TypeScript)
```

### Key Files:

- **`package.json`**: The extension manifest containing metadata, dependencies, and contribution points
- **`src/extension.js`** or **`src/extension.ts`**: The main entry point for your extension
- **`.vscodeignore`**: Specifies files to exclude when packaging the extension

### Example `package.json`:

```json
{
  "name": "my-extension",
  "displayName": "My Extension",
  "description": "A sample VS Code extension",
  "version": "1.0.0",
  "engines": {
    "vscode": "^1.60.0"
  },
  "categories": [
    "Other"
  ],
  "activationEvents": [
    "onCommand:extension.helloWorld"
  ],
  "main": "./src/extension.js",
  "contributes": {
    "commands": [
      {
        "command": "extension.helloWorld",
        "title": "Hello World"
      }
    ]
  }
}
```

## Verifying Installation

After installation, verify the extension is installed:

1. Open the Extensions view (`Ctrl+Shift+X` / `Cmd+Shift+X`)
2. Look for the extension in the **Installed** section
3. Or use the command line:
   ```bash
   code --list-extensions
   ```

## Troubleshooting

### Extension Not Showing Up
- Restart VS Code after installation
- Check if the extension requires a specific VS Code version
- Look at the Output panel (`View > Output`) and select "Extensions" from the dropdown

### Installation Fails
- Check your internet connection (for marketplace installations)
- Verify the `.vsix` file is not corrupted
- Ensure you have the latest version of VS Code
- Try installing with administrator/sudo privileges if you get permission errors

### Extension Not Working
- Check the extension's output in the Output panel
- Reload VS Code window (`Ctrl+R` / `Cmd+R` or `Developer: Reload Window` from Command Palette)
- Check extension requirements in its documentation

## Additional Resources

- [VS Code Extension API Documentation](https://code.visualstudio.com/api)
- [Publishing Extensions](https://code.visualstudio.com/api/working-with-extensions/publishing-extension)
- [Extension Marketplace](https://marketplace.visualstudio.com/vscode)

## License

See [LICENSE](LICENSE) file for details.
