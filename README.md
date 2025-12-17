![VSCode](https://img.shields.io/badge/VSCode-1.74%2B-007ACC?logo=visual-studio-code&logoColor=white)
![License](https://img.shields.io/badge/license-MIT-green)

# WDS Script Syntax

WinDbg script support for `.wds` files with syntax highlighting, smart indentation, and snippets for reverse engineering and exploit development.

## Features

- Complete WinDbg script syntax highlighting
- Dot command recognition (`.block`, `.for`, `.if`, `.foreach`)
- Pseudo-register support (`$t0-$t19`, `$arg1-$argN`)
- Full x86/x64 register highlighting
- Expression evaluator syntax (`@@C++()`, `@@masm()`)
- Memory search command patterns
- Smart indentation for control flow blocks
- 30+ code snippets for common exploit dev tasks

### Snippets

**ROP Gadget Search:**
- `rop` - Configurable ROP gadget search with badchar filtering
- `gadget_pop` - Find POP reg; RET sequences
- `gadget_add_esp` - Find ADD ESP, value; RET
- `gadget_jmp` - Find JMP/CALL register gadgets
- `pivot` - Stack pivot gadget search

**Module Analysis:**
- `aslr` - Check ASLR status for all modules
- `dep` - Check DEP/NX for all modules
- `safeseh` - Check SafeSEH for all modules
- `modinfo` - Comprehensive module protection analysis

**Memory & Analysis:**
- `search` - Pattern search in memory
- `searchstr` / `searchuni` - String search (ASCII/Unicode)
- `writable` - Find writable memory regions
- `stack` / `heap` - Stack/heap analysis
- `seh` - SEH chain dump and disassembly

**Exploit Dev Helpers:**
- `bp_cond` - Conditional breakpoint
- `ba` - Hardware breakpoint
- `vprotect` - VirtualProtect ROP setup
- `badchar` - Badchar checking loop
- `pattern` / `offset` - Pattern generation/offset finding

And many more - type a snippet prefix and press Tab to expand.

## Usage

Create files with `.wds` extension and write your WinDbg scripts. Execute in WinDbg using:

```
$$>< script.wds
```

### Script Formatting

WinDbg handles both formatted and compact scripts equally. This extension provides smart indentation for readability:

```windbg
.block
{
    .for (r $t0 = 0x58; @$t0 < 0x5F; r $t0 = @$t0 + 0x01)
    {
        .if (@@C++(@$t0 != 0x5C))
        {
            s-[1]b ${$arg1} ${$arg2} $t0 0xC3
        }
    }
}
```

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
