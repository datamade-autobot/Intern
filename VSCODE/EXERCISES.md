# VS Code Power Hour - Hands-On Exercises

These exercises reinforce key concepts from the session. Complete them during or after the Power Hour.

---

## Exercise 1: Mastering Essential Shortcuts (10 mins)

### Setup
1. Create a new file: `practice.txt`
2. Copy this text into it:

```
Shopping List
- apples
- bananas
- oranges
- grapes
- strawberries

TODO: buy milk
TODO: buy bread
TODO: buy eggs

function calculate(a, b) {
  return a + b
}
```

### Tasks

#### Task 1.1: Multi-Cursor Editing
1. Select the word "TODO"
2. Press `Cmd/Ctrl + D` three times to select all three occurrences
3. Type "DONE" to replace them all at once

**Expected Result:**
```
DONE: buy milk
DONE: buy bread
DONE: buy eggs
```

#### Task 1.2: Line Manipulation
1. Put cursor on the "apples" line
2. Press `Alt + Down` three times to move it below "grapes"
3. Press `Cmd/Ctrl + Shift + K` to delete the line

**Expected Result:**
```
- bananas
- oranges
- grapes
- strawberries
```

#### Task 1.3: Copy Line Down
1. Put cursor on the "function calculate" line
2. Press `Shift + Alt + Down` twice to duplicate it
3. Use multi-cursor to change "calculate" to "multiply" and "divide"

**Expected Result:**
```
function calculate(a, b) {
  return a + b
}
function multiply(a, b) {
  return a + b
}
function divide(a, b) {
  return a + b
}
```

#### Task 1.4: Quick Open
1. Press `Cmd/Ctrl + P`
2. Type "AGENTS"
3. Press Enter to open AGENTS.md
4. Press `Cmd/Ctrl + P` again
5. Type `:10` to jump to line 10

#### Task 1.5: Command Palette
1. Press `Cmd/Ctrl + Shift + P`
2. Type "format"
3. Select "Format Document"
4. See your code formatted

### Bonus Challenge
Use only keyboard shortcuts to:
1. Open the Explorer view
2. Create a new file called `test.js`
3. Type: `console.log("Hello")`
4. Save the file
5. Close the file
6. Reopen it

<details>
<summary>Solution</summary>

1. `Cmd/Ctrl + Shift + E` - Explorer view
2. Right-click in Explorer, or use File menu
3. Type the code
4. `Cmd/Ctrl + S` - Save
5. `Cmd/Ctrl + W` - Close
6. `Cmd/Ctrl + P`, type "test.js", Enter

</details>

---

## Exercise 2: Creating Your First AGENTS.md (15 mins)

### Scenario
You're starting a new Python project: a weather CLI app that fetches weather data and displays it nicely in the terminal.

### Task
Create an `AGENTS.md` file for this project.

### Requirements
Your AGENTS.md should include:
1. Project context (what is it?)
2. Tech stack
3. Code style preferences
4. Common commands
5. At least one "gotcha" or important note

### Template

```markdown
# AI Agent Instructions

## Project Context
[What is this project? What does it do?]

## Stack
[List technologies, libraries, versions]

## Code Style
[Your preferences for how code should be written]

## Common Commands
[Commands AI might need to run]

## Important Notes
[Gotchas, conventions, things to know]
```

### Example Solution

<details>
<summary>Click to see example</summary>

```markdown
# AI Agent Instructions

## Project Context
This is a command-line weather app that fetches current weather data
from OpenWeatherMap API and displays it in a formatted way in the terminal.
Built as a learning project for Python CLI development.

## Stack
- Python 3.11
- requests (HTTP client)
- click (CLI framework)
- rich (terminal formatting)
- pytest (testing)
- python-dotenv (environment variables)

## Code Style
- Use type hints for all function parameters and returns
- Follow PEP 8 style guide
- Prefer f-strings over .format() or %
- Write docstrings in Google style
- Keep functions small (< 20 lines when possible)
- Use descriptive variable names (no single letters except in loops)

## Common Commands
```bash
# Install dependencies
pip install -r requirements.txt

# Run the app
python main.py --city "San Francisco"

# Run tests
pytest

# Run tests with coverage
pytest --cov=src

# Format code
black .

# Lint code
flake8 src/
```

## Important Notes
- API key must be in `.env` file (never commit .env!)
- API has rate limits: 60 calls per minute
- Temperature is returned in Kelvin by default, convert to Fahrenheit
- Error handling is important - API calls can fail
- City names with spaces need quotes: `"New York"`
```

</details>

### Validation
Use AI to review your AGENTS.md:

**Prompt:**
> "Review this AGENTS.md file. Is it clear and complete? What would you need to know to effectively help me code this project?"

---

## Exercise 3: AI-Assisted Coding (20 mins)

### Task
Use AI to help you write a simple Python function with tests.

### Step-by-Step

#### Step 1: Set Up File
1. Create `temperature.py`
2. Open AI chat (`Cmd/Ctrl + Shift + I`)

#### Step 2: Generate Function
Use this prompt:

```
Write a Python function called `kelvin_to_fahrenheit` that:
- Takes a temperature in Kelvin (float)
- Returns temperature in Fahrenheit (float)
- Includes type hints
- Includes a docstring explaining the function
- Handles negative Kelvin values by raising ValueError

Formula: F = (K - 273.15) * 9/5 + 32
```

#### Step 3: Review Generated Code
Check:
- [ ] Type hints present?
- [ ] Docstring clear?
- [ ] Error handling included?
- [ ] Formula correct?

#### Step 4: Generate Tests
New prompt:

```
Write pytest tests for the kelvin_to_fahrenheit function. Include tests for:
- Normal values (e.g., 273.15K = 32F)
- Absolute zero (0K = -459.67F)
- High temperatures
- Negative Kelvin (should raise ValueError)
```

#### Step 5: Iterate
Ask AI:

```
Can you add another function `fahrenheit_to_kelvin` that does
the reverse conversion? Update the tests to cover the new function.
```

#### Step 6: Run Tests
1. Make sure pytest is installed: `pip install pytest`
2. Run: `pytest temperature.py -v`
3. All tests should pass

### Bonus Challenges

**Challenge 1: Add Celsius**
Ask AI to add Celsius conversion functions and tests.

**Challenge 2: Input Validation**
Ask AI to add more robust input validation (e.g., type checking).

**Challenge 3: CLI Integration**
Ask AI to create a Click CLI command that uses these functions.

---

## Exercise 4: Git Workflow in VS Code (10 mins)

### Setup
1. Make sure you're in a git repository
2. If not, run: `git init`

### Tasks

#### Task 4.1: Making Changes
1. Edit one of the markdown files in VSCODE folder
2. Add a new section or fix a typo
3. Save the file

#### Task 4.2: Viewing Changes
1. Open Source Control view (`Cmd/Ctrl + Shift + G`)
2. Click on the file to see diff
3. Understand what changed

#### Task 4.3: Staging Changes
1. Click the `+` icon next to the file to stage it
2. Or right-click → Stage Changes

#### Task 4.4: Writing Commit Message
Open AI chat and prompt:

```
I modified [filename] to [what you did].
Suggest a good commit message following conventional commits format.
```

#### Task 4.5: Committing
1. Type the commit message in the text box
2. Click the checkmark icon or `Cmd/Ctrl + Enter`
3. Commit created!

#### Task 4.6: View History
1. If you have GitLens installed, click on a file
2. See "Git Blame" information
3. Explore file history

### Bonus: AI-Powered Git Messages

Next time you commit, try:

```
Prompt to AI:
"I've made the following changes:
[Paste your git diff here]

Suggest a commit message following conventional commits:
- feat: new feature
- fix: bug fix
- docs: documentation
- style: formatting
- refactor: code restructuring
- test: adding tests
```

---

## Exercise 5: Terminal Mastery (10 mins)

### Setup
Open integrated terminal (`` Ctrl + ` ``)

### Tasks

#### Task 5.1: Navigation
```bash
# Print current directory
pwd

# List files
ls -la

# Create a directory
mkdir temp_folder

# Navigate into it
cd temp_folder

# Create a file
touch hello.txt

# Navigate back
cd ..

# Remove the directory
rm -rf temp_folder
```

#### Task 5.2: Running Code
Create a simple Python script:

**hello.py:**
```python
def greet(name):
    print(f"Hello, {name}!")

if __name__ == "__main__":
    greet("Nate")
```

In terminal:
```bash
python hello.py
```

#### Task 5.3: Multiple Terminals
1. Open a second terminal (`Cmd/Ctrl + Shift + `` `)
2. In terminal 1: `python hello.py`
3. In terminal 2: `ls -la`
4. Switch between them

#### Task 5.4: Terminal Split
1. Click split icon in terminal panel
2. Run different commands in each split
3. Practice terminal workflow

---

## Exercise 6: Extension Exploration (15 mins)

### Task
Find and install extensions for your preferred language.

### Steps

#### Step 6.1: Open Extensions
1. Press `Cmd/Ctrl + Shift + X`
2. Browse installed extensions
3. Check what each does

#### Step 6.2: Language-Specific Extensions

**If you use Python:**
- Search "Python"
- Install "Python" by Microsoft
- Install "Pylance"

**If you use JavaScript/TypeScript:**
- Install "ESLint"
- Install "Prettier"

**If you use Go:**
- Install "Go"

**If you use Rust:**
- Install "rust-analyzer"

#### Step 6.3: Productivity Extensions
Install these:
1. **Error Lens** - See errors inline
2. **GitLens** - Git supercharged
3. **Path Intellisense** - Autocomplete paths
4. **Auto Rename Tag** - Rename HTML tags

#### Step 6.4: Theme (Optional Fun!)
1. Search "theme"
2. Try: "One Dark Pro", "Dracula", "Night Owl"
3. Find one you like
4. Apply it

#### Step 6.5: Settings Sync
1. Press `Cmd/Ctrl + Shift + P`
2. Type "Settings Sync: Turn On"
3. Sign in with GitHub
4. Your settings will sync across devices!

---

## Exercise 7: Prompt Engineering Practice (20 mins)

### Goal
Learn to write effective prompts for AI assistants.

### Bad vs Good Prompts

Practice rewriting these bad prompts:

#### Example 1
❌ **Bad:** "fix this code"

✅ **Good:** "This function returns undefined instead of the user object. Can you debug why the database query isn't returning results?"

#### Example 2
❌ **Bad:** "make it faster"

✅ **Good:** "This function processes a 10,000 item array and takes 5 seconds. Can you optimize it using more efficient algorithms or data structures?"

#### Your Turn

Rewrite these prompts:

1. ❌ "add error handling"
   ✅ [Your answer]

2. ❌ "write tests"
   ✅ [Your answer]

3. ❌ "refactor this"
   ✅ [Your answer]

<details>
<summary>Suggested Answers</summary>

1. ✅ "Add try-catch error handling to this API call. If the request fails, log the error and return a user-friendly error message instead of crashing."

2. ✅ "Write Jest unit tests for the `calculateTotal` function. Cover these cases: valid input, zero values, negative numbers, and non-numeric input."

3. ✅ "Refactor this function to reduce nested if statements. Consider using early returns or extracting helper functions to improve readability."

</details>

### Practice Exercise

Open AI chat and try these prompts:

**Prompt 1: Context-Rich Request**
```
I'm building a REST API endpoint for user registration.
Stack: Node.js, Express, PostgreSQL.
Requirements:
- Accept email and password
- Validate email format
- Hash password with bcrypt
- Check if email already exists
- Return JWT token on success
- Return 400 for validation errors, 409 for existing email

Can you write the endpoint handler with error handling?
```

**Prompt 2: Iterative Refinement**
```
[After receiving code]
"Can you add input sanitization to prevent SQL injection?"

[After update]
"Now add rate limiting to prevent abuse"

[After update]
"Add logging for security events (registration attempts, failures)"
```

### Key Takeaways
- Specific > Vague
- Context helps AI understand your needs
- Iterate, don't expect perfection first try
- Explain the "why" behind your request

---

## Exercise 8: Custom Workspace Setup (Optional Advanced)

### Task
Create a custom VS Code settings file for your project.

### Steps

#### Step 8.1: Create Workspace Settings
1. In your project root, create `.vscode/settings.json`
2. Add custom settings:

```json
{
  "editor.tabSize": 2,
  "editor.formatOnSave": true,
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true
  },
  "files.exclude": {
    "**/.git": true,
    "**/__pycache__": true,
    "**/*.pyc": true,
    "**/node_modules": true
  },
  "python.linting.enabled": true,
  "python.linting.pylintEnabled": true,
  "python.formatting.provider": "black"
}
```

#### Step 8.2: Create Tasks
Create `.vscode/tasks.json`:

```json
{
  "version": "2.0.0",
  "tasks": [
    {
      "label": "Run Python Tests",
      "type": "shell",
      "command": "pytest",
      "group": {
        "kind": "test",
        "isDefault": true
      }
    },
    {
      "label": "Format Code",
      "type": "shell",
      "command": "black ."
    }
  ]
}
```

Run tasks: `Cmd/Ctrl + Shift + P` → "Tasks: Run Task"

---

## Completion Checklist

After finishing these exercises, you should be comfortable with:

- [ ] Essential keyboard shortcuts
- [ ] Multi-cursor editing
- [ ] Creating configuration files (AGENTS.md)
- [ ] Using AI assistants effectively
- [ ] Writing good prompts
- [ ] Git workflow in VS Code
- [ ] Terminal usage
- [ ] Installing and configuring extensions

## Next Steps

1. **Daily Practice:** Use 3 new shortcuts each day
2. **AI Integration:** Use AI for one task per day
3. **Customize:** Adjust settings to your preference
4. **Explore:** Try new extensions from [EXTENSIONS.md](EXTENSIONS.md)
5. **Advanced:** When ready, explore [MCP-GUIDE.md](MCP-GUIDE.md)

---

**Remember:** Learning is iterative. Don't try to master everything at once. Build muscle memory through consistent practice!
