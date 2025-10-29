# Troubleshooting Guide

This guide helps you resolve common issues when installing or using the DDR VS Code extension.

## Table of Contents
- [Installation Issues](#installation-issues)
- [Extension Not Working](#extension-not-working)
- [Performance Issues](#performance-issues)
- [Common Error Messages](#common-error-messages)
- [Getting Help](#getting-help)

## Installation Issues

### Issue: "Unable to install extension"

**Symptoms:**
- Installation fails with an error message
- Extension doesn't appear in installed extensions

**Solutions:**

1. **Check VS Code Version**
   - Verify you're running a compatible version of VS Code
   - Run: `code --version`
   - Update VS Code if necessary: https://code.visualstudio.com/

2. **Verify VSIX File Integrity**
   - Ensure the `.vsix` file downloaded completely
   - Check file size matches the expected size
   - Try re-downloading the file
   - Verify file extension is `.vsix` (not `.vsix.zip` or other)

3. **Check File Permissions**
   - Ensure you have read permissions for the `.vsix` file
   - On macOS/Linux: `chmod +r ddr-extension.vsix`

4. **Try Different Installation Method**
   - If UI installation fails, try command line:
     ```bash
     code --install-extension /path/to/extension.vsix
     ```
   - If command line fails, try UI method

5. **Check Disk Space**
   - Ensure you have sufficient disk space
   - Extensions are installed in:
     - **Windows**: `%USERPROFILE%\.vscode\extensions`
     - **macOS**: `~/.vscode/extensions`
     - **Linux**: `~/.vscode/extensions`

### Issue: "Extension is already installed"

**Solution:**
If you're trying to update, uninstall the old version first:
```bash
code --uninstall-extension publisher.extension-name
code --install-extension /path/to/new-version.vsix
```

### Issue: Installation hangs or freezes

**Solutions:**

1. **Close and restart VS Code**
2. **Try command line installation**
3. **Check for other extensions causing conflicts**
4. **Disable other extensions temporarily**
5. **Clear VS Code cache:**
   - Close VS Code
   - Delete cache folder:
     - **Windows**: `%APPDATA%\Code\Cache`
     - **macOS**: `~/Library/Application Support/Code/Cache`
     - **Linux**: `~/.config/Code/Cache`
   - Restart VS Code

## Extension Not Working

### Issue: Extension installed but not active

**Solutions:**

1. **Verify Extension is Enabled**
   - Open Extensions view (`Ctrl+Shift+X`)
   - Find the extension
   - Check if it shows "Disable" (meaning it's enabled)
   - If it shows "Enable", click it

2. **Reload VS Code**
   - Press `Ctrl+Shift+P` / `Cmd+Shift+P`
   - Type: "Developer: Reload Window"
   - Press Enter

3. **Check Workspace Trust**
   - Some extensions require workspace trust
   - Click "Trust" in the workspace trust dialog if prompted

4. **Check Extension Logs**
   - Open Output panel: `View > Output`
   - Select the extension from the dropdown
   - Look for error messages

### Issue: Extension features not visible

**Solutions:**

1. **Check Command Palette**
   - Press `Ctrl+Shift+P` / `Cmd+Shift+P`
   - Type the extension name or feature
   - Verify commands are available

2. **Check Extension Settings**
   - Open Settings (`Ctrl+,`)
   - Search for the extension name
   - Verify settings are configured correctly

3. **Check File Associations**
   - Ensure you're working with the correct file type
   - Some features only activate for specific file types

### Issue: "Extension activation failed"

**Solutions:**

1. **Check Dependencies**
   - Some extensions require other software installed
   - Check extension documentation for requirements

2. **Review Error Message**
   - Open Developer Tools: `Help > Toggle Developer Tools`
   - Check Console tab for detailed errors

3. **Reinstall Extension**
   - Uninstall the extension
   - Restart VS Code
   - Reinstall the extension

## Performance Issues

### Issue: VS Code becomes slow after installing extension

**Solutions:**

1. **Disable Extension Temporarily**
   - See if performance improves
   - Report performance issues to extension developers

2. **Check Extension Settings**
   - Some features may have performance impact
   - Adjust settings to reduce resource usage

3. **Update VS Code**
   - Newer versions may have performance improvements
   - Download from: https://code.visualstudio.com/

4. **Check System Resources**
   - Monitor CPU and memory usage
   - Close unnecessary applications

## Common Error Messages

### "Extension 'X' cannot be installed on this version of VS Code"

**Solution:**
- Update VS Code to the minimum required version
- Or download a compatible version of the extension

### "ENOENT: no such file or directory"

**Solution:**
- Verify the full path to the `.vsix` file
- Use absolute paths instead of relative paths
- Check for typos in the file path

### "Unable to extract extension"

**Solution:**
- The `.vsix` file may be corrupted
- Re-download the file
- Verify file integrity (check file size)

### "Extension is malformed"

**Solution:**
- The `.vsix` file is corrupted or incomplete
- Download a fresh copy
- Ensure download completed successfully

## Compatibility Issues

### Issue: Extension conflicts with other extensions

**Solutions:**

1. **Identify Conflicting Extension**
   - Disable other extensions one by one
   - Test after each disable
   - Note which extension causes the conflict

2. **Report Conflict**
   - Open an issue describing the conflict
   - Include both extension names and versions

3. **Choose One Extension**
   - If conflict can't be resolved, use only one extension

## Developer Mode Issues

### Issue: Extension doesn't work in development mode

**Solutions:**

1. **Check Extension Host Log**
   - `Help > Toggle Developer Tools`
   - Check Console for errors

2. **Reload Extension Host**
   - Press `Ctrl+Shift+P` / `Cmd+Shift+P`
   - Type: "Developer: Reload Window"

## Getting Help

If you can't resolve your issue:

1. **Gather Information**
   - VS Code version: `code --version`
   - Operating system and version
   - Extension version
   - Error messages (full text)
   - Steps to reproduce the issue

2. **Check Existing Issues**
   - Search the repository issues
   - Your problem may already be reported

3. **Open a New Issue**
   - Use the issue template if available
   - Provide all gathered information
   - Include screenshots if relevant

4. **Contact Support**
   - Follow repository guidelines for support
   - Be patient and provide requested information

## Diagnostic Commands

Run these commands to gather diagnostic information:

```bash
# Check VS Code version
code --version

# List all installed extensions
code --list-extensions --show-versions

# Check extension installation directory
# Windows
dir %USERPROFILE%\.vscode\extensions

# macOS/Linux
ls -la ~/.vscode/extensions
```

## Additional Resources

- [VS Code Extension Troubleshooting](https://code.visualstudio.com/docs/editor/extension-marketplace#_troubleshooting)
- [VS Code GitHub Issues](https://github.com/microsoft/vscode/issues)
- [VS Code Documentation](https://code.visualstudio.com/docs)
