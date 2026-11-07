---
name: windows-shell-rules-en
description: Working rules for Claude Code on Windows - plain ASCII file names, UTF-8 when saving text, quoted paths with spaces, check which shell will run a command (PowerShell vs Git Bash), one task per conversation. Use whenever you create files or folders, save non-English text, or run commands on a Windows machine.
---

# Windows shell rules

You are working on a Windows computer. Reply briefly. These rules prevent the five mistakes that happen most often on Windows.

## 1. Plain ASCII in file and folder names
File contents can be in any language. File names, folder names and variable names use ASCII letters only.
- write `report_september.txt`, not a name with accented letters,
- write `meeting_notes`, not `Meeting notes (final)`.

## 2. Save text as UTF-8
Older Windows PowerShell (5.1) writes files in an encoding that loses non-English letters unless told otherwise.
- always add `-Encoding utf8` to `Set-Content`, `Add-Content` and `Out-File`,
- after saving, read back a fragment and check that accented letters look right.

## 3. Quote paths with spaces
A folder called `My Documents` without quotes is two separate words to a command.
- quote every path in a command: `"My Documents\plan.txt"`,
- create new working folders without spaces.

## 4. Check the shell first
On Windows a command may run in PowerShell or in the Git Bash shell. The syntax differs.
- before writing a command, find out which shell will run it,
- PowerShell: `$env:NAME`, `Get-ChildItem`, `;` between commands (version 5.1 has no `&&`),
- Git Bash: `$NAME`, `ls`, forward slashes in paths,
- when a command fails for no clear reason, first check whether it went to the wrong shell.

## 5. One task, one conversation
When the user starts a new, unrelated topic, suggest a new conversation. Whatever must survive (decisions, rules) goes into the project rules file (CLAUDE.md), not only into the conversation.
