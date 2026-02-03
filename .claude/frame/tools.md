# Claude Code Tools Reference

Framework-specific guide to using Claude Code's tools effectively.

## Tool Categories

Claude Code provides specialized tools for different operations. Always prefer specialized tools over bash commands.

### File Operations

#### Read
**Use for:** Reading file contents
```text
Use Read tool to read /path/to/file.md
```

**Don't use:** `bash cat /path/to/file.md`

**When to use Read:**
- Reading configuration files
- Examining source code
- Checking file contents before editing
- Viewing documentation

**Examples:**
```text
- Read the README to understand the project
- Read package.json to check dependencies
- Read the component file before modifying it
```

---

#### Edit
**Use for:** Making exact string replacements in files
```text
Use Edit tool to replace "old string" with "new string" in /path/to/file.md
```

**Don't use:** `bash sed`, `bash awk`

**Critical requirement:** MUST read file first before editing

**When to use Edit:**
- Fixing typos or bugs
- Updating function implementations
- Changing configuration values
- Refactoring code

**Examples:**
```text
- Replace the function signature in Button.tsx
- Update the version number in package.json
- Fix the import statement in utils/date.ts
```

---

#### Write
**Use for:** Creating new files or completely replacing existing files

**Critical requirement:** MUST read existing file first (if it exists)

**Don't use:** `bash echo`, `bash cat > file`

**When to use Write:**
- Creating new files
- Completely rewriting a file
- Creating configuration files
- Writing documentation

**WARNING:** Prefer Edit over Write for existing files when possible

---

### Search Operations

#### Glob
**Use for:** Finding files by pattern
```text
Use Glob to find all TypeScript files: **/*.ts
```

**Don't use:** `bash find`, `bash ls`

**When to use Glob:**
- Finding all files of a certain type
- Locating files in specific directories
- Discovering project structure
- Checking for file existence

**Examples:**
```text
- Find all React components: **/*.tsx
- Find all markdown files: **/*.md
- Find all test files: **/*.test.ts
```

---

#### Grep
**Use for:** Searching file contents
```text
Use Grep to search for "functionName" in all TypeScript files
```

**Don't use:** `bash grep`, `bash rg`

**When to use Grep:**
- Finding where functions are defined
- Searching for specific text patterns
- Finding all occurrences of a variable
- Searching across multiple files

**Examples:**
```text
- Search for "TODO" comments in all files
- Find where Button component is imported
- Search for error handling patterns
```

---

### System Operations

#### Bash
**Use for:** Terminal operations that cannot use specialized tools

**When to use Bash:**
- Git operations (status, commit, push)
- Running npm/yarn/pnpm commands
- Docker operations
- System commands (ps, top, kill)
- Installing dependencies

**Don't use Bash for:**
- File reading (use Read)
- File editing (use Edit/Write)
- File searching (use Glob/Grep)
- File writing (use Write)

**Examples:**
```text
- Check git status
- Run tests: npm test
- Install dependencies: npm install
- Build project: npm run build
```

---

### Task Operations

#### Task
**Use for:** Launching specialized agents for complex, multi-step tasks

**When to use Task:**
- Exploring codebases (use `subagent_type=Explore`)
- Planning implementations (use `subagent_type=Plan`)
- Running tests (use `subagent_type=Bash`)
- Searching code extensively

**Examples:**
```text
- Use Task tool with Explore agent to find all API endpoints
- Use Task tool with Plan agent to design a new feature
- Use Task tool with Bash agent to run the test suite
```

---

## Tool Selection Decision Tree

```
Need to read a file?
├─ Yes → Use Read tool
└─ No → Continue

Need to change file content?
├─ Yes → Have you read the file?
│   ├─ Yes → Use Edit tool (preferred) or Write tool
│   └─ No → Read the file first!
└─ No → Continue

Need to find files?
├─ Yes → Use Glob tool with pattern
└─ No → Continue

Need to search content?
├─ Yes → Use Grep tool with search pattern
└─ No → Continue

Need terminal command?
├─ Yes → Can it be done with specialized tools?
│   ├─ Yes → Use specialized tool instead
│   └─ No → Use Bash tool
└─ No → Continue

Complex multi-step task?
├─ Yes → Use Task tool with appropriate subagent
└─ No → Continue
```

## Common Mistakes

### Mistake 1: Using bash cat to read files
❌ `bash cat /path/to/file.md`
✅ `Use Read tool to read /path/to/file.md`

### Mistake 2: Using bash grep to search content
❌ `bash grep "pattern" **/*.ts`
✅ `Use Grep to search for "pattern" in TypeScript files`

### Mistake 3: Using bash find to locate files
❌ `bash find . -name "*.tsx"`
✅ `Use Glob to find all TSX files: **/*.tsx`

### Mistake 4: Editing files without reading first
❌ `Use Edit tool to replace "..." in /path/to/file.md` (without reading)
✅ `Use Read tool to read /path/to/file.md, then use Edit tool...`

### Mistake 5: Using bash sed for replacements
❌ `bash sed -i 's/old/new/g' /path/to/file.md`
✅ `Use Edit tool to replace "old" with "new" in /path/to/file.md`

## Performance Tips

1. **Parallel tool calls:** Call multiple independent tools in a single message
   ```text
   Use Glob to find *.tsx files AND Use Grep to search for "Button"
   ```

2. **Prefer specialized tools:** They're faster and provide better error handling

3. **Read before editing:** Always read files to get exact content for Edit tool

4. **Use Task for exploration:** For complex searches, use Task with Explore agent

## Tool Permissions

Some tools require permissions in `.claude/settings.local.json`:

```json
{
  "permissions": {
    "allow": [
      "Bash(git:*)",          // Allow git commands
      "Bash(npm:*)",          // Allow npm commands
      "WebSearch",            // Allow web searches
      "Skill(*)"              // Allow invoking any skill
    ]
  }
}
```

## Related Documentation

- `/frame/skill-development.md` - Building skills with tools
- `/rules/skills.md` - Skill development rules
