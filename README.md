![VSCode](https://img.shields.io/badge/VSCode-1.74%2B-007ACC?logo=visual-studio-code&logoColor=white)
![License](https://img.shields.io/badge/license-MIT-green)

<img width="128" height="128" alt="icon-128" src="https://github.com/user-attachments/assets/d4b48324-6941-4467-bafc-ce64716561ba" />

# WDS Script Syntax

WinDbg script support for `.wds` files with syntax highlighting, smart indentation, and snippets for reverse engineering and exploit development.

## Features

- Complete WinDbg script syntax highlighting
- WinDbg compliant auto-indent for control flow blocks
- Dot command recognition (`.block`, `.for`, `.if`, `.foreach`)
- Pseudo-register support (`$t0-$t19`, `$arg1-$argN`)
- Full x86/x64 register highlighting
- Expression evaluator syntax (`@@C++()`, `@@masm()`)
- Memory search command patterns
- 30+ code snippets for common exploit dev tasks

## Usage

Create files with `.wds` extension and write your WinDbg scripts. Execute in WinDbg using:

```
$$>< script.wds
```

Type a snippet prefix and press **Tab** to expand:
```
rop<Tab>      → ROP gadget search with badchar filtering
aslr<Tab>     → Check ASLR for all modules  
pivot<Tab>    → Stack pivot gadget search
```

See [SNIPPETS.md](SNIPPETS.md) for the full list.

Press Enter after `{` to auto-indent. Type `}` to auto-dedent.

## Installation

### From Source
Copy to VSCode extensions directory:
- **Windows:** `%USERPROFILE%\.vscode\extensions\wds-syntax`
- **macOS/Linux:** `~/.vscode/extensions/wds-syntax`

Then restart VSCode.

### From VSIX
```bash
code --install-extension wds-syntax-1.0.0.vsix
```

## License

MIT