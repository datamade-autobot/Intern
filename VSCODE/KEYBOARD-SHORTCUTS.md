# Essential VS Code Keyboard Shortcuts

## Philosophy

Learn shortcuts for actions you do 10+ times per day. Don't memorize everything at once.

## The Big 3 (Learn These First)

| Shortcut | Action | Why It Matters |
|----------|--------|----------------|
| `Cmd/Ctrl + P` | Quick Open file | Fastest way to navigate |
| `Cmd/Ctrl + Shift + P` | Command Palette | Access any VS Code command |
| `Cmd/Ctrl + ,` | Settings | Customize your IDE |

## File Navigation

| Shortcut | Action |
|----------|--------|
| `Cmd/Ctrl + P` | Quick Open (fuzzy file search) |
| `Cmd/Ctrl + Tab` | Switch between open files |
| `Cmd/Ctrl + \` | Split editor |
| `Cmd/Ctrl + W` | Close file |
| `Cmd/Ctrl + K, Cmd/Ctrl + W` | Close all files |
| `Cmd/Ctrl + Shift + T` | Reopen closed file |
| `Cmd/Ctrl + K, Z` | Zen mode (distraction-free) |

**Pro Tip:** In Quick Open, type `:` followed by line number to jump directly to that line (e.g., `file.ts:42`)

## Editing

### Basic
| Shortcut | Action |
|----------|--------|
| `Cmd/Ctrl + X` | Cut line (no selection needed) |
| `Cmd/Ctrl + C` | Copy line |
| `Cmd/Ctrl + V` | Paste |
| `Cmd/Ctrl + Z` | Undo |
| `Cmd/Ctrl + Shift + Z` | Redo |
| `Cmd/Ctrl + /` | Toggle comment |
| `Cmd/Ctrl + D` | Select next occurrence |
| `Cmd/Ctrl + Shift + L` | Select all occurrences |

### Advanced
| Shortcut | Action |
|----------|--------|
| `Alt + Up/Down` | Move line up/down |
| `Shift + Alt + Up/Down` | Copy line up/down |
| `Cmd/Ctrl + Shift + K` | Delete line |
| `Cmd/Ctrl + Enter` | Insert line below |
| `Cmd/Ctrl + Shift + Enter` | Insert line above |
| `Cmd/Ctrl + ]` | Indent line |
| `Cmd/Ctrl + [` | Outdent line |
| `Cmd/Ctrl + Shift + \` | Jump to matching bracket |

### Multi-Cursor Editing
| Shortcut | Action |
|----------|--------|
| `Alt + Click` | Add cursor at click position |
| `Cmd/Ctrl + Alt + Up/Down` | Add cursor above/below |
| `Cmd/Ctrl + D` | Add next occurrence to selection |
| `Cmd/Ctrl + U` | Undo last cursor action |
| `Esc` | Cancel multi-cursor mode |

**Example Use Case:**
```
1. Place cursor on variable name
2. Press Cmd/Ctrl + D repeatedly to select all occurrences
3. Start typing to rename everywhere at once
```

## Search & Replace

| Shortcut | Action |
|----------|--------|
| `Cmd/Ctrl + F` | Find in file |
| `Cmd/Ctrl + H` | Find and replace in file |
| `Cmd/Ctrl + Shift + F` | Find in workspace |
| `Cmd/Ctrl + Shift + H` | Replace in workspace |
| `F3` / `Cmd/Ctrl + G` | Find next |
| `Shift + F3` / `Cmd/Ctrl + Shift + G` | Find previous |

**Pro Tips:**
- Use regex mode (`Alt + R`) for advanced patterns
- `Alt + Enter` selects all matches for multi-cursor editing

## Code Navigation

| Shortcut | Action |
|----------|--------|
| `Cmd/Ctrl + Click` | Go to definition |
| `F12` | Go to definition |
| `Cmd/Ctrl + F12` | Go to implementation |
| `Shift + F12` | Find all references |
| `Alt + Left/Right` | Navigate backward/forward |
| `Cmd/Ctrl + Shift + O` | Go to symbol in file |
| `Cmd/Ctrl + T` | Go to symbol in workspace |
| `Cmd/Ctrl + G` | Go to line |

## Code Editing

| Shortcut | Action |
|----------|--------|
| `Cmd/Ctrl + Space` | Trigger IntelliSense/autocomplete |
| `Cmd/Ctrl + .` | Quick fix (show code actions) |
| `F2` | Rename symbol |
| `Cmd/Ctrl + K, Cmd/Ctrl + F` | Format selection |
| `Shift + Alt + F` | Format document |
| `Cmd/Ctrl + K, Cmd/Ctrl + X` | Trim trailing whitespace |

## Terminal

| Shortcut | Action |
|----------|--------|
| `Ctrl + `` (backtick) | Toggle integrated terminal |
| `Cmd/Ctrl + Shift + `` | Create new terminal |
| `Cmd/Ctrl + Shift + 5` | Split terminal |
| `Cmd/Ctrl + Shift + C` | Copy from terminal |
| `Cmd/Ctrl + Shift + V` | Paste to terminal |

## AI Assistant Shortcuts

### Claude Code
| Shortcut | Action |
|----------|--------|
| `Cmd/Ctrl + I` | Open inline chat |
| `Cmd/Ctrl + Shift + I` | Open chat panel |
| `Cmd/Ctrl + L` | Focus chat input |
| `/` | Access Claude skills |

### GitHub Copilot
| Shortcut | Action |
|----------|--------|
| `Tab` | Accept suggestion |
| `Esc` | Dismiss suggestion |
| `Alt + ]` | Next suggestion |
| `Alt + [` | Previous suggestion |
| `Cmd/Ctrl + Enter` | Open Copilot suggestions panel |
| `Cmd/Ctrl + I` | Inline chat |

## Panels & Views

| Shortcut | Action |
|----------|--------|
| `Cmd/Ctrl + B` | Toggle sidebar |
| `Cmd/Ctrl + J` | Toggle panel (terminal/output/problems) |
| `Cmd/Ctrl + Shift + E` | Explorer view |
| `Cmd/Ctrl + Shift + F` | Search view |
| `Cmd/Ctrl + Shift + G` | Source control view |
| `Cmd/Ctrl + Shift + D` | Debug view |
| `Cmd/Ctrl + Shift + X` | Extensions view |

## Debugging

| Shortcut | Action |
|----------|--------|
| `F5` | Start/Continue debugging |
| `F9` | Toggle breakpoint |
| `F10` | Step over |
| `F11` | Step into |
| `Shift + F11` | Step out |
| `Cmd/Ctrl + K, Cmd/Ctrl + I` | Show hover (inspect variable) |

## Git

| Shortcut | Action |
|----------|--------|
| `Cmd/Ctrl + Shift + G` | Open source control |
| `Cmd/Ctrl + Enter` | Commit (in SCM view) |
| `Cmd/Ctrl + K, Cmd/Ctrl + O` | Open repository |

## Customizing Shortcuts

### View/Edit Shortcuts
1. `Cmd/Ctrl + K, Cmd/Ctrl + S` - Open keyboard shortcuts
2. Search for the command
3. Click the pencil icon to edit
4. Press your desired key combination

### Common Customizations

**Duplicate Line** (like other IDEs):
```json
{
  "key": "cmd+d",
  "command": "editor.action.copyLinesDownAction"
}
```

**Quick AI Chat:**
```json
{
  "key": "cmd+shift+a",
  "command": "claude.openChat"
}
```

## Chord Shortcuts

Chord shortcuts are two-key combinations (e.g., `Cmd+K, Cmd+S`).

**How to use:**
1. Press first key combination
2. Release
3. Press second key combination within 1 second

**Examples:**
- `Cmd/Ctrl + K, Cmd/Ctrl + C` - Add line comment
- `Cmd/Ctrl + K, Cmd/Ctrl + U` - Remove line comment
- `Cmd/Ctrl + K, Z` - Toggle Zen mode

## Learning Strategy

### Week 1: Essential Navigation
- `Cmd/Ctrl + P` - Quick open
- `Cmd/Ctrl + Shift + P` - Command palette
- `Cmd/Ctrl + D` - Select next occurrence
- `Cmd/Ctrl + /` - Toggle comment

### Week 2: Editing Efficiency
- `Alt + Up/Down` - Move lines
- `Cmd/Ctrl + Enter` - Insert line below
- Multi-cursor with `Alt + Click`
- `F2` - Rename symbol

### Week 3: Code Navigation
- `F12` - Go to definition
- `Shift + F12` - Find references
- `Cmd/Ctrl + Shift + O` - Go to symbol
- `Alt + Left/Right` - Navigate history

### Week 4: Advanced Workflows
- Terminal shortcuts
- Debugging shortcuts
- Custom shortcuts for your workflow
- Zen mode for deep work

## Cheat Sheet Wallpaper

Download printable cheat sheets:
- [Windows](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf)
- [macOS](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-macos.pdf)
- [Linux](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-linux.pdf)

## Pro Tips

### 1. **Sticky Scroll**
Enable in settings: `"editor.stickyScroll.enabled": true`
Shows current scope at top of editor.

### 2. **Breadcrumbs**
`Cmd/Ctrl + Shift + .` - Focus breadcrumbs (shows current file path/symbol)

### 3. **Command Palette Search**
Type `@` for symbols, `#` for workspace symbols, `:` for line numbers

### 4. **Quick Open Tricks**
- `file.ts:20` - Open file at line 20
- `@symbolName` - Jump to symbol in current file
- `#symbolName` - Find symbol in workspace

### 5. **Fold/Unfold Code**
- `Cmd/Ctrl + Shift + [` - Fold region
- `Cmd/Ctrl + Shift + ]` - Unfold region
- `Cmd/Ctrl + K, Cmd/Ctrl + 0` - Fold all
- `Cmd/Ctrl + K, Cmd/Ctrl + J` - Unfold all

## Resources

- [VS Code Keyboard Shortcuts Reference](https://code.visualstudio.com/docs/getstarted/keybindings)
- [Keybindings Editor](https://code.visualstudio.com/docs/getstarted/keybindings#_keyboard-shortcuts-editor)

---

**Remember:** Don't try to memorize everything. Pick 2-3 new shortcuts per week based on actions you perform frequently. Muscle memory takes about 21 days to form.
