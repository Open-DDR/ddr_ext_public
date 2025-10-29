# Repository Structure

This document provides an overview of the repository structure and how to navigate it.

## Directory Layout

```
ddr_ext_public/
│
├── .github/                    # GitHub-specific configurations
│   ├── ISSUE_TEMPLATE/         # Issue templates
│   │   ├── bug_report.md       # Bug report template
│   │   └── feature_request.md  # Feature request template
│   └── workflows/              # GitHub Actions workflows
│       └── release.yml.example # Sample release workflow
│
├── docs/                       # Documentation
│   ├── INSTALLATION.md         # Detailed installation guide
│   ├── TROUBLESHOOTING.md      # Troubleshooting guide
│   ├── RELEASE_GUIDE.md        # Guide for maintainers
│   └── QUICK_REFERENCE.md      # Quick command reference
│
├── releases/                   # Extension releases
│   └── README.md               # Release information
│
├── .gitattributes              # Git LFS configuration for VSIX files
├── .gitignore                  # Files to ignore in Git
├── CHANGELOG.md                # Version history
├── CONTRIBUTING.md             # Contribution guidelines
├── LICENSE                     # License information
└── README.md                   # Main documentation (start here!)
```

## For End Users

**Start here:** [README.md](../README.md)

### Quick Start
1. Download a `.vsix` file from [releases/](../releases/)
2. Follow installation instructions in [README.md](../README.md)
3. If you have issues, check [TROUBLESHOOTING.md](TROUBLESHOOTING.md)

### Detailed Documentation
- **Installing the extension**: [INSTALLATION.md](INSTALLATION.md)
- **Common issues**: [TROUBLESHOOTING.md](TROUBLESHOOTING.md)
- **Quick commands**: [QUICK_REFERENCE.md](QUICK_REFERENCE.md)

## For Contributors

**Start here:** [CONTRIBUTING.md](../CONTRIBUTING.md)

### How to Contribute
1. Read [CONTRIBUTING.md](../CONTRIBUTING.md)
2. Open an issue or submit a PR
3. Follow the issue templates in `.github/ISSUE_TEMPLATE/`

### Reporting Issues
- **Bug reports**: Use `.github/ISSUE_TEMPLATE/bug_report.md`
- **Feature requests**: Use `.github/ISSUE_TEMPLATE/feature_request.md`

## For Maintainers

**Start here:** [RELEASE_GUIDE.md](RELEASE_GUIDE.md)

### Releasing Extensions
1. Read [RELEASE_GUIDE.md](RELEASE_GUIDE.md)
2. Package your extension using `vsce package`
3. Upload `.vsix` file to `releases/` folder
4. Update [CHANGELOG.md](../CHANGELOG.md)
5. Create a GitHub release (optional)

### Automation
- Sample workflow: `.github/workflows/release.yml.example`
- Copy and customize for automated releases

## Navigation Tips

### Looking for...
- **How to install?** → [README.md](../README.md) or [INSTALLATION.md](INSTALLATION.md)
- **Installation not working?** → [TROUBLESHOOTING.md](TROUBLESHOOTING.md)
- **Quick command reference?** → [QUICK_REFERENCE.md](QUICK_REFERENCE.md)
- **How to contribute?** → [CONTRIBUTING.md](../CONTRIBUTING.md)
- **How to release?** → [RELEASE_GUIDE.md](RELEASE_GUIDE.md)
- **What changed?** → [CHANGELOG.md](../CHANGELOG.md)
- **Available downloads?** → [releases/](../releases/)

## File Purposes

### User-Facing Files
- `README.md` - Main entry point with installation instructions
- `LICENSE` - Legal terms
- `CHANGELOG.md` - Version history and changes
- `releases/` - Download location for extensions

### Documentation Files
- `docs/INSTALLATION.md` - Comprehensive installation guide
- `docs/TROUBLESHOOTING.md` - Problem-solving guide
- `docs/QUICK_REFERENCE.md` - Quick command reference
- `docs/RELEASE_GUIDE.md` - For maintainers releasing extensions

### Development Files
- `CONTRIBUTING.md` - How to contribute to the project
- `.github/ISSUE_TEMPLATE/` - Templates for issues
- `.github/workflows/` - CI/CD automation examples
- `.gitattributes` - Git LFS configuration
- `.gitignore` - Files excluded from version control

## Key Features

### 🎯 For Users
- Clear installation instructions
- Multiple installation methods
- Comprehensive troubleshooting guide
- Quick reference for common tasks

### 🔧 For Maintainers
- Complete release guide
- Automation examples
- Version management guidelines
- Best practices

### 🤝 For Contributors
- Clear contribution guidelines
- Issue templates
- Code of conduct
- Recognition system

## Getting Help

1. **Check existing documentation** - Most questions are answered in the docs
2. **Search issues** - Someone may have asked before
3. **Open an issue** - Use the appropriate template
4. **Be patient** - Maintainers will respond as soon as possible

## Quick Links

- [Main README](../README.md)
- [Installation Guide](INSTALLATION.md)
- [Troubleshooting](TROUBLESHOOTING.md)
- [Release Guide](RELEASE_GUIDE.md)
- [Contributing](../CONTRIBUTING.md)
- [Changelog](../CHANGELOG.md)
- [Releases](../releases/)
