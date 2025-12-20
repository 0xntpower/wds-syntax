# WDS Snippets Reference

Code snippets for exploit development and reverse engineering workflows.

## ROP Gadget Search

| Prefix | Description |
|--------|-------------|
| `rop` | Configurable ROP gadget search loop with badchar filtering |
| `gadget_pop` | Find POP r32, RET sequences (x86) |
| `gadget_pop64` | Find POP r64, RET sequences (x64) |
| `gadget_add_esp` | Find ADD ESP, imm32 gadgets |
| `gadget_add_rsp` | Find ADD RSP gadgets (x64) |
| `gadget_jmp` | Find JMP/CALL register gadgets |
| `pivot` | Stack pivot gadget search (x86) |
| `pivot64` | Stack pivot gadget search (x64) |

## Module Analysis

| Prefix | Description |
|--------|-------------|
| `aslr` | Check ASLR status for all modules (x86) |
| `aslr64` | Check ASLR status for all modules (x64) |
| `noaslr` | List modules without ASLR |
| `dep` | Check DEP/NX for all modules |
| `safeseh` | Check SafeSEH for all modules |

## Breakpoints

| Prefix | Description |
|--------|-------------|
| `bp_cond` | Conditional breakpoint |
| `bp_log` | Logging breakpoint (log and continue) |
| `ba` | Hardware breakpoint (read/write/execute) |

## Memory Search

| Prefix | Description |
|--------|-------------|
| `search` | Byte pattern search |
| `searchstr` | ASCII string search |
| `searchdword` | DWORD value search |
| `egg` | Egghunter marker search |

## Memory Analysis

| Prefix | Description |
|--------|-------------|
| `rwx` | Find RWX memory regions |
| `writable` | Find writable memory regions |
| `protect` | Memory protection info |
| `stack` | Stack dump with symbols |

## Exception Handling

| Prefix | Description |
|--------|-------------|
| `except` | Full exception analysis |
| `seh` | SEH chain dump |
| `crash` | Quick crash triage |

## Exploit Development

| Prefix | Description |
|--------|-------------|
| `badchar` | Badchar verification (0x01-0xFF) |
| `offset` | Calculate offset between addresses |
| `vprotect` | VirtualProtect ROP helper |

## Utilities

| Prefix | Description |
|--------|-------------|
| `uf` | Disassemble entire function |
| `peb` | Display PEB |
| `teb` | Display TEB |
| `log` | Start logging session |

## Usage

Type a prefix in any `.wds` file and press **Tab** to expand. Use **Tab** to jump between placeholders.

```
rop<Tab>
```
Expands to full ROP gadget search loop with configurable parameters.

Press `Ctrl+Space` to search through available snippets.
