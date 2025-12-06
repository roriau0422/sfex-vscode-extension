# Building and Publishing the SFX VSCode Extension

## Prerequisites

Install `vsce` (Visual Studio Code Extension manager):
```bash
npm install -g @vscode/vsce
```

## Building

Package the extension into a `.vsix` file:
```bash
vsce package
```

This will create `sfex-lang-0.3.2.vsix` in the current directory.

## Installing Locally

1. Open VS Code
2. Go to Extensions (Ctrl+Shift+X)
3. Click the `...` menu → Install from VSIX
4. Select `sfex-lang-0.3.2.vsix`

## Testing

1. Install the extension locally (see above)
2. Open a `.sfex` file
3. Verify syntax highlighting works
4. Test auto-completion of brackets and quotes

## Publishing to Marketplace

### First Time Setup

1. Create a publisher account at https://marketplace.visualstudio.com/manage
2. Generate a Personal Access Token (PAT) from Azure DevOps
3. Login with vsce:
   ```bash
   vsce login your-publisher-name
   ```

### Publishing

```bash
vsce publish
```

This will:
- Increment the version
- Package the extension
- Publish to the marketplace

### Publishing a Specific Version

```bash
vsce publish 0.3.3
```

## Updating

1. Update version in `package.json`
2. Update `CHANGELOG.md`
3. Commit changes
4. Package and publish

## Directory Structure

```
sfex-vscode-extension/
├── syntaxes/
│   ├── sfex.tmLanguage.json      # Syntax highlighting rules
│   └── language-configuration.json # Language config
├── package.json                   # Extension metadata
├── README.md                      # User documentation
├── CHANGELOG.md                   # Version history
├── LICENSE                        # MIT License
└── BUILD.md                       # This file
```

## Notes

- The extension is minimal and doesn't require npm dependencies
- No build step needed - just packaging with vsce
- Icon can be added later (update package.json icon field)
