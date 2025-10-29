# Contributing to DDR Extension Distribution

Thank you for your interest in contributing to the DDR VS Code Extension distribution!

## Ways to Contribute

### Reporting Issues

If you encounter problems with the extension:

1. **Search existing issues** to avoid duplicates
2. **Use the issue template** (if available)
3. **Provide detailed information**:
   - VS Code version
   - Operating system
   - Extension version
   - Steps to reproduce
   - Expected vs actual behavior
   - Screenshots (if applicable)

### Improving Documentation

Documentation improvements are always welcome:

- Fix typos or unclear instructions
- Add missing information
- Improve examples
- Translate documentation
- Add troubleshooting tips

### Suggesting Enhancements

To suggest new features or improvements:

1. Check if the suggestion already exists in issues
2. Open a new issue with the "enhancement" label
3. Describe the feature and its benefits
4. Explain use cases
5. Consider implementation details

## Documentation Structure

This repository contains:

```
ddr_ext_public/
├── README.md              # Main documentation
├── CHANGELOG.md           # Version history
├── LICENSE               # License information
├── docs/
│   ├── INSTALLATION.md   # Installation guide
│   ├── TROUBLESHOOTING.md # Troubleshooting guide
│   └── RELEASE_GUIDE.md  # Guide for maintainers
└── releases/
    └── README.md         # Release information
```

## Making Changes

### For Documentation Updates

1. **Fork the repository**
2. **Create a branch** for your changes:
   ```bash
   git checkout -b docs/improve-installation-guide
   ```
3. **Make your changes**
4. **Test the documentation**:
   - Check for broken links
   - Verify markdown rendering
   - Ensure instructions are clear
5. **Commit your changes**:
   ```bash
   git commit -m "docs: improve installation instructions for Windows"
   ```
6. **Push to your fork**:
   ```bash
   git push origin docs/improve-installation-guide
   ```
7. **Open a Pull Request**

### Commit Message Guidelines

Follow conventional commits:

- `docs:` - Documentation changes
- `fix:` - Bug fixes
- `feat:` - New features
- `chore:` - Maintenance tasks
- `refactor:` - Code refactoring
- `test:` - Test changes

Examples:
- `docs: add troubleshooting for Linux installation`
- `fix: correct broken link in README`
- `feat: add automated release workflow`

## Pull Request Process

1. **Ensure your PR**:
   - Has a clear title and description
   - References related issues (if any)
   - Contains focused, minimal changes
   - Updates relevant documentation

2. **Wait for review**:
   - Maintainers will review your PR
   - Address any feedback
   - Make requested changes

3. **After approval**:
   - Your PR will be merged
   - Changes will be available in the repository

## Code of Conduct

### Our Standards

- Be respectful and inclusive
- Welcome newcomers
- Accept constructive criticism
- Focus on what's best for the community
- Show empathy towards others

### Unacceptable Behavior

- Harassment or discriminatory language
- Trolling or insulting comments
- Personal or political attacks
- Publishing others' private information
- Other unethical or unprofessional conduct

## Questions?

If you have questions:

- Open an issue with the "question" label
- Check existing documentation
- Reach out to maintainers

## License

By contributing, you agree that your contributions will be licensed under the same license as the project (see [LICENSE](LICENSE)).

## Recognition

Contributors will be recognized in:
- Release notes (for significant contributions)
- Repository contributors page
- Project documentation (when appropriate)

Thank you for contributing! 🎉
