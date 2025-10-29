# DDR Extension for VS Code - Public Release

Download and install the DDR Extension for Visual Studio Code to work with Device Description Repository (DDR) files and access comprehensive DDR validation workflows.

## 📦 Installation

### Method 1: Install via VSIX File (Recommended)

1. **Download the Extension**
   - Download `ddr-ext-0.0.1.vsix` from this repository

2. **Install in VS Code**
   - Open Visual Studio Code
   - Press `Ctrl+Shift+P` (or `Cmd+Shift+P` on Mac) to open Command Palette
   - Type `Extensions: Install from VSIX...` and select it
   - Browse and select the downloaded `ddr-ext-0.0.1.vsix` file
   - Click "Install"

3. **Verify Installation**
   - The extension will be installed and activated automatically
   - You should see a notification: "DDR Extension activated!"

### Method 2: Install via Command Line

```bash
code --install-extension ddr-ext-0.0.1.vsix
```

## 🚀 Quick Start

1. **Open VS Code with a Workspace**
   - Open a folder or workspace in VS Code (required for the extension to activate)

2. **Access DDR Control Panel**
   - Look for the "DDR Explorer" icon in the Activity Bar (left sidebar)
   - Click to expand and see the "DDR Control Panel"

3. **Start Using Validation Flows**
   - Click any validation flow button to get started
   - Use the dashboard for overview and statistics

## 🎛️ Features

### Interactive Control Panel
- **Sidebar Interface**: Centralized control panel in VS Code sidebar
- **One-Click Access**: Direct buttons for all 6 validation flows
- **Visual Feedback**: Real-time notifications and status updates
- **VS Code Integration**: Native theme support and seamless integration

### DDR Validation Workflows
- **🔧 HBM3E Preparation Flow**: System setup and preparation
- **⚙️ EVB Bring-Up Flow**: Engineering Validation Board setup
- **💾 Memory Bring-Up Flow**: Memory controller initialization
- **🛠️ Test Engine Setup Flow**: DDR test engine configuration
- **✅ Validation Flow**: Comprehensive memory validation
- **⚙️ Advanced Features Flow**: Advanced features testing

### File Operations
- **DDR File Validation**: XML structure and schema validation
- **Auto-formatting**: Proper indentation and formatting
- **Error Diagnostics**: Real-time error reporting
- **Context Menu Integration**: Right-click options

## 📖 Usage Guide

### Accessing the Control Panel

1. **Open Workspace**: Ensure you have a folder/workspace open in VS Code
2. **Find DDR Explorer**: Look for the DDR Explorer icon in the Activity Bar
3. **Expand Panel**: Click to see the "DDR Control Panel" section

### Using Validation Flows

#### Quick Actions
- **📊 Open Dashboard**: Access main dashboard with statistics
- **🔄 Refresh Stats**: Update current system status

#### Validation Flow Buttons
Click any button to open the corresponding validation webview:

- **⚙️ Preparation Flow** → Opens HBM3E preparation interface
- **🔧 EVB Bring-Up** → Opens hardware setup interface
- **💾 Memory Bring-Up** → Opens memory controller interface
- **🛠️ Test Engine Setup** → Opens test engine configuration
- **✅ Validation Flow** → Opens comprehensive validation interface
- **⚙️ Advanced Features** → Opens advanced testing interface

#### Execute Flow Buttons
Each flow has an execute button (▶️) that will:
1. Automatically run the validation flow
2. Open the corresponding webview
3. Show progress and results

### Command Palette Access

You can also access features via Command Palette (`Ctrl+Shift+P`):

- `DDR: Hello DDR` - Test extension
- `DDR: Validate DDR File` - Validate current file
- `DDR: Format DDR File` - Format current file
- `DDR Webviews: Open Dashboard` - Open dashboard
- `DDR Validation: Execute [Flow Name]` - Execute specific flows

## 🔧 Configuration

The extension can be configured in VS Code settings:

- `ddr-ext.enableAutoValidation`: Auto-validate files on save (default: `true`)
- `ddr-ext.validationLevel`: Validation level - `error`, `warning`, `info` (default: `warning`)

## 🆘 Troubleshooting

### Extension Not Appearing
- **Check Workspace**: Ensure a folder/workspace is open
- **Check Extensions**: Verify extension is enabled in Extensions panel
- **Restart VS Code**: Try reloading the window (`Ctrl+Shift+P` → "Reload Window")

### Control Panel Empty
- **Check Sidebar**: Look for DDR Explorer in Activity Bar
- **Check Console**: Open Developer Tools (Help → Toggle Developer Tools)
- **Check Output**: View Output panel → DDR Extension

### Buttons Not Working
- **Check Notifications**: Look for error messages in VS Code
- **Check Console**: View browser console for JavaScript errors
- **Try Commands**: Use Command Palette as alternative

## 📋 System Requirements

- **VS Code**: Version 1.74.0 or higher
- **Operating System**: Windows, macOS, or Linux
- **Node.js**: Not required for end users (only for development)

## 🔄 Version Information

- **Current Version**: 0.0.1
- **Release Date**: October 2025
- **Compatibility**: VS Code 1.74.0+

## 📞 Support

For issues, questions, or feature requests:

1. **Check Troubleshooting**: Review the troubleshooting section above
2. **VS Code Output**: Check the DDR Extension output panel for error details
3. **Developer Tools**: Use Help → Toggle Developer Tools for advanced debugging

## 🎯 What's New in v0.0.1

- ✅ Interactive Control Panel with sidebar integration
- ✅ 6 comprehensive DDR validation workflows
- ✅ Dashboard with statistics and progress tracking
- ✅ One-click flow execution and webview access
- ✅ Modern VS Code theme-integrated interface
- ✅ Real-time message passing between components
- ✅ DDR file validation and formatting capabilities

---

**Ready to start validating DDR files?** Install the extension and click the DDR Explorer icon to begin! 🚀
