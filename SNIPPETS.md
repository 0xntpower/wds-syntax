# WDS Snippets Reference

code snippets for exploit development and reverse engineering workflows.

## ROP Gadget Search

| Prefix | Description |
|--------|-------------|
| `rop` | Configurable ROP gadget search with badchar filtering |
| `gadget_pop` | Find POP reg; RET sequences |
| `gadget_add_esp` | Find ADD ESP, value; RET |
| `gadget_jmp` | Find JMP/CALL register gadgets |
| `pivot` | Stack pivot gadget search |

## Module Analysis

| Prefix | Description |
|--------|-------------|
| `aslr` | Check ASLR status for all modules |
| `dep` | Check DEP/NX for all modules |
| `safeseh` | Check SafeSEH for all modules |
| `modinfo` | Comprehensive module protection analysis |

## Breakpoints

| Prefix | Description |
|--------|-------------|
| `bp_load` | Break on module load |
| `bp_cond` | Conditional breakpoint |
| `ba` | Hardware breakpoint (read/write/execute) |

## Memory & Analysis

| Prefix | Description |
|--------|-------------|
| `search` | Pattern search in memory |
| `searchstr` | ASCII string search |
| `searchuni` | Unicode string search |
| `writable` | Find writable memory regions |
| `stack` | Stack frame analysis |
| `heap` | Heap chunk analysis |

## Exception Handling

| Prefix | Description |
|--------|-------------|
| `except` | Full exception analysis |
| `seh` | SEH chain dump and disassembly |

## Exploit Development

| Prefix | Description |
|--------|-------------|
| `badchar` | Badchar checking loop |
| `pattern` | Pattern generation for offset finding |
| `offset` | Calculate offset from pattern value |
| `vprotect` | VirtualProtect ROP setup helper |

## Utilities

| Prefix | Description |
|--------|-------------|
| `distance` | Calculate offset between addresses |
| `protect` | Memory protection info |
| `symbol` | Symbol resolution |
| `struct` | Display data structure |
| `func` | Disassemble entire function |
| `log` | Start logging session |
| `cfg` | Control flow trace |
| `hookdet` | Inline hook detection |
| `iat` | Import Address Table analysis |

## Usage

Type a prefix in any `.wds` file and press **Tab** to expand. Use **Tab** to jump between placeholders.

```
rop<Tab>
```
Expands to full ROP gadget search loop with configurable parameters.

Press `ctrl + space` to search through avaliable snippets.