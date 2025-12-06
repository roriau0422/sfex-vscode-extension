# Change Log

All notable changes to the SFX Language Support extension will be documented in this file.

## [0.3.2] - 2025-12-06

### Added
- **Complete syntax highlighting** extracted from actual compiler source code
  - All keywords: Story, Concept, Situation, If, When, For, Repeat, Try, Catch, etc.
  - Control flow: If/Else/ElseIf, When/Otherwise, Repeat/While, For/Each, Break, Continue, Return
  - Exception handling: Try, Catch, Always
  - Context switching: Switch on/off
  - Special keywords: Use, Create, Called, Set, Print, Do, Background, Proceed, changes
- **Type highlighting**
  - Primitives: Number, FastNumber, String, Boolean
  - Collections: List, Map, Vector
  - Advanced: Option, WeakRef, WeakList, WeakMap, TaskHandle, Error
- **Standard library highlighting**
  - Modules: Data, File, HTTP, WebSocket, TCP, UDP, Env, System, Time, Math, LLM
  - Formats: JSON, XML, HTML, CSV, TOML
  - Concurrency: Task, Channel
  - Module.Function call patterns
- **Built-in function highlighting**
  - Print, Set, Create, Switch, Use, WeakRef, FastNumber, Some, None
  - This keyword and property access
  - Special properties: Length, Size, IsValid, IsSome, IsNone
- **String interpolation** highlighting for `{variable}` patterns
- **Code snippets** for common patterns (25+ snippets)
  - story, concept, situation, method, when observer
  - if, ifelse, when pattern match, for, repeat
  - try-catch, create, set, print
  - HTTP, file operations, JSON, LLM, tasks
- Single-quote string support
- Improved operator highlighting (comparison, logical, arithmetic, assignment)

### Changed
- File extension: .mon → .sfex
- Project name: Mono → SFX (Situation Framework eXchange)
- Complete rewrite of TextMate grammar based on actual lexer/parser implementation
- Enhanced pattern matching for better accuracy

### Fixed
- Accurate keyword recognition from compiler token definitions
- Proper type and constant highlighting
- Better method and property access patterns
- Correct operator precedence in highlighting

## [0.3.0] - Previous Release

### Added
- Initial release
- Basic syntax highlighting
- Language configuration
- Support for .mon files
