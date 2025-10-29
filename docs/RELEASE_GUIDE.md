# Release Guide for Maintainers

This guide explains how to package and release VS Code extensions to this repository.

## Table of Contents
- [Prerequisites](#prerequisites)
- [Packaging the Extension](#packaging-the-extension)
- [Publishing to This Repository](#publishing-to-this-repository)
- [Version Management](#version-management)
- [Best Practices](#best-practices)

## Prerequisites

Before creating a release, ensure you have:

- **Node.js** (LTS version recommended)
- **npm** or **yarn** package manager
- **vsce** (Visual Studio Code Extension Manager)
  ```bash
  npm install -g @vscode/vsce
  # or
  yarn global add @vscode/vsce
  ```
- **Git** for version control
- Write access to this repository

## Packaging the Extension

### Step 1: Prepare Your Extension

1. **Update Version Number**
   - Edit `package.json`
   - Update the `version` field following [Semantic Versioning](https://semver.org/)
   - Example: `"version": "1.2.3"`

2. **Update CHANGELOG**
   - Document all changes in `CHANGELOG.md`
   - Include new features, bug fixes, and breaking changes

3. **Test Thoroughly**
   - Test all features in VS Code
   - Test on multiple platforms if possible (Windows, macOS, Linux)
   - Verify extension activates correctly
   - Check for console errors

4. **Update README**
   - Ensure documentation is up-to-date
   - Add screenshots if features changed
   - Update usage instructions

### Step 2: Package the Extension

Run the following command in your extension's root directory:

```bash
vsce package
```

This creates a `.vsix` file like: `your-extension-1.2.3.vsix`

**Options:**

```bash
# Package for a specific target platform
vsce package --target win32-x64
vsce package --target darwin-x64
vsce package --target linux-x64

# Package without running prepublish script
vsce package --no-yarn

# Package for pre-release
vsce package --pre-release
```

**Common Targets:**
- `win32-x64` - Windows 64-bit
- `win32-ia32` - Windows 32-bit
- `win32-arm64` - Windows ARM
- `darwin-x64` - macOS Intel
- `darwin-arm64` - macOS Apple Silicon
- `linux-x64` - Linux 64-bit
- `linux-arm64` - Linux ARM
- `alpine-x64` - Alpine Linux

### Step 3: Verify the Package

1. **Test the VSIX file**
   ```bash
   code --install-extension your-extension-1.2.3.vsix
   ```

2. **Check file contents**
   ```bash
   # VSIX files are ZIP archives, you can inspect them
   unzip -l your-extension-1.2.3.vsix
   ```

3. **Verify package size**
   - Ensure size is reasonable
   - Check for unintended large files
   - Use `.vscodeignore` to exclude unnecessary files

## Publishing to This Repository

### Method 1: Upload to Releases Folder

1. **Copy VSIX File**
   ```bash
   cp your-extension-1.2.3.vsix /path/to/ddr_ext_public/releases/
   ```

2. **Create Release Information**
   - Create a `README.md` in the releases folder (if not exists)
   - Document the release with version info
   - Include release notes

3. **Commit and Push**
   ```bash
   cd /path/to/ddr_ext_public
   git add releases/your-extension-1.2.3.vsix
   git add releases/README.md
   git commit -m "Release version 1.2.3"
   git push
   ```

### Method 2: Create GitHub Release

If using GitHub Releases:

1. **Create a Git Tag**
   ```bash
   git tag -a v1.2.3 -m "Version 1.2.3"
   git push origin v1.2.3
   ```

2. **Create GitHub Release**
   - Go to repository on GitHub
   - Click "Releases" → "Draft a new release"
   - Select the tag you created
   - Add release title: "v1.2.3"
   - Add release notes from CHANGELOG
   - Upload the `.vsix` file as an asset
   - Click "Publish release"

## Version Management

### Semantic Versioning

Follow [Semantic Versioning](https://semver.org/):

- **MAJOR** (1.0.0): Breaking changes
- **MINOR** (0.1.0): New features (backward compatible)
- **PATCH** (0.0.1): Bug fixes (backward compatible)

### Pre-release Versions

For beta or alpha releases:
- `1.0.0-alpha.1`
- `1.0.0-beta.1`
- `1.0.0-rc.1`

### Version Command

Update version using npm:
```bash
# Patch release (0.0.1 → 0.0.2)
npm version patch

# Minor release (0.1.0 → 0.2.0)
npm version minor

# Major release (1.0.0 → 2.0.0)
npm version major
```

## File Size Optimization

### Use .vscodeignore

Create a `.vscodeignore` file to exclude unnecessary files:

```
# Development files
.vscode/
.vscode-test/
src/
test/
tests/
**/*.ts
**/*.map
tsconfig.json
.gitignore

# Documentation
.github/
docs/
*.md
!README.md
!CHANGELOG.md
!LICENSE

# Dependencies
node_modules/
.npm/
.yarn/

# Build files
*.vsix
.eslintrc*
.prettierrc*
webpack.config.js
```

### Check Package Contents

```bash
vsce ls
```

## Best Practices

### Before Release

- [ ] Update version number in `package.json`
- [ ] Update CHANGELOG.md with all changes
- [ ] Test extension thoroughly
- [ ] Test installation from VSIX
- [ ] Update README.md if needed
- [ ] Review and update documentation
- [ ] Check for security vulnerabilities (`npm audit`)
- [ ] Verify no sensitive data in package

### During Release

- [ ] Package extension: `vsce package`
- [ ] Test VSIX installation
- [ ] Upload to releases folder or GitHub
- [ ] Create release notes
- [ ] Tag the release in git
- [ ] Verify download and installation

### After Release

- [ ] Announce release (if applicable)
- [ ] Monitor for issues
- [ ] Respond to user feedback
- [ ] Update documentation based on feedback

## Automating Releases

### Using GitHub Actions

Create `.github/workflows/release.yml`:

```yaml
name: Release Extension

on:
  push:
    tags:
      - 'v*'

jobs:
  release:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      
      - name: Setup Node.js
        uses: actions/setup-node@v3
        with:
          node-version: '18'
      
      - name: Install dependencies
        run: npm ci
      
      - name: Package extension
        run: |
          npm install -g @vscode/vsce
          vsce package
      
      - name: Create Release
        uses: softprops/action-gh-release@v1
        with:
          files: '*.vsix'
        env:
          GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
```

## Troubleshooting

### "vsce: command not found"

Install vsce globally:
```bash
npm install -g @vscode/vsce
```

### "ERROR: Missing publisher name"

Add publisher in `package.json`:
```json
{
  "publisher": "your-publisher-name"
}
```

### Package too large

- Check `.vscodeignore` is configured correctly
- Run `vsce ls` to see what's included
- Remove unnecessary dependencies
- Use `bundledDependencies` for required runtime dependencies

### Platform-specific issues

Package for specific platforms:
```bash
vsce package --target win32-x64 --target darwin-x64 --target linux-x64
```

## Resources

- [vsce Documentation](https://code.visualstudio.com/api/working-with-extensions/publishing-extension)
- [Extension Guidelines](https://code.visualstudio.com/api/references/extension-guidelines)
- [Extension Manifest](https://code.visualstudio.com/api/references/extension-manifest)
- [Semantic Versioning](https://semver.org/)
