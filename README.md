# SFX Language Support for Visual Studio Code

Language support for **SFX (Situation Framework eXchange)** - a beginner-friendly programming language with mathematical honesty, 1-based indexing, and reactive programming.

## Features

- **Syntax Highlighting**: Full syntax highlighting for SFX files (.sfex)
- **Bracket Matching**: Auto-closing brackets, quotes, and braces
- **Indentation**: Smart indentation support
- **Comments**: Line and block comment toggling

## Installation

### From VSIX
1. Download the latest `.vsix` file from releases
2. Open VS Code
3. Go to Extensions (Ctrl+Shift+X)
4. Click the `...` menu → Install from VSIX
5. Select the downloaded file

### From Marketplace (Coming Soon)
Search for "SFX Language Support" in the VS Code Extensions marketplace.

## Language Features

SFX is designed to be beginner-friendly with:
- **Mathematical honesty**: `0.1 + 0.2 = 0.3` (arbitrary precision)
- **1-based indexing**: `List[1]` is the first item
- **No null pointers**: Safe defaults (0, "", False, [])
- **Narrative syntax**: `Name is "John"` instead of `name = "John"`
- **Context-oriented**: Situations modify object behavior at runtime
- **Reactive programming**: Self-healing data with automatic property observers

## Example Code

```sfex
Concept: Product
    Price
    Tax
    Total

    When Price changes:
        Set This.Tax to This.Price * 0.1
        Set This.Total to This.Price + This.Tax

Story:
    Create Product Called Phone
    Set Phone.Price to 100
    Print Phone.Total  # Automatically 110!
```

## Links

- [SFX Repository](https://github.com/roriau0422/sfex-lang)
- [Documentation](https://github.com/roriau0422/sfex-lang/blob/main/README.md)
- [Report Issues](https://github.com/roriau0422/sfex-vscode-extension/issues)

## Release Notes

### 0.3.2
- Updated for SFX v0.3.2
- File extension changed from .mon to .sfex
- Enhanced syntax highlighting
- Support for new language features (FastNumber, Option, WeakRef)

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

MIT License - see LICENSE file for details
