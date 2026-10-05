# Cheatsheet: [Topic / Tool / CLI]

* **Tool / CLI Name**: [e.g., Docker CLI / Git / PostgreSQL psql / Linux Networking]
* **Version**: [e.g., 24.0+]
* **Last Updated**: [YYYY-MM-DD]
* **Official Ref**: [Link to CLI reference]

---

## 1. High-Frequency Commands & Idioms

| Command / Syntax | What It Does | Why / When to Use |
| :--- | :--- | :--- |
| `cmd --flag [arg]` | Concise explanation of behavior | Primary use case |
| `cmd subcmd -v` | Concise explanation of behavior | Diagnostic or verbose mode |

---

## 2. Common Workflows & Recipes

### Recipe 1: [Common Task Name]
```bash
# Step 1: Initialize
command init --flag

# Step 2: Execute operation
command run --option value
```

### Recipe 2: [Troubleshooting / Diagnostic Task]
```bash
# Inspect runtime status and logs
command logs --tail 100 -f
```

---

## 3. Dangerous Flags & Gotchas (CAUTION)

> [!CAUTION]
> The following commands alter state permanently or bypass safety checks:
> * `command --force`: Deletes without confirmation.
> * `command reset --hard`: Drops uncommitted working tree changes.

---

## 4. Key Configuration Flags Explained

* `--flag-a`: [Meaning, default value, and subtle consequences]
* `--flag-b`: [Meaning, default value, and subtle consequences]
