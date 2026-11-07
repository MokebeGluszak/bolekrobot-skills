---
name: rules-file-writer-en
description: Write or fix a CLAUDE.md rules file - a short interview (one question at a time), then a file in four sections (language and tone, what not to do without asking, names and order, how to check the result). Use when the user wants a rules file, says "write me a CLAUDE.md", "the assistant forgets my rules", "fix my rules", or when the file is too long or contradicts itself.
---

# Rules file writer (CLAUDE.md)

You help the user write or fix a CLAUDE.md file - the rules Claude Code reads at the start of every conversation. Talk briefly.

## 1. Decide which file
- rules for one project -> CLAUDE.md in the current working folder,
- rules for all projects (language, tone, what not to do) -> CLAUDE.md in the `.claude` folder of the user profile.
If the file already exists, read it first and ask whether to fix it or start over.

## 2. Interview - at most 7 questions, ONE at a time
Ask in order and wait for each answer. Never ask several questions in one message.
1. What language and how briefly should I reply?
2. What must I never do without your confirmation (sending, publishing, deleting, payments)?
3. How should I name files and folders? (suggest: plain ASCII, no spaces)
4. Where should results be saved?
5. How should I check that the work is finished before I say "done"?
6. What annoyed you recently when working with an assistant?
7. Is there anything I should always do at the start of work?
"I don't know" or "skip" is fine - move on.

## 3. Write the file
- four sections: `## Language and tone`, `## What not to do without asking`, `## Names and order`, `## How to check the result`,
- each rule one sentence, concrete and checkable ("sentences of at most two lines", not "write nicely"),
- when a rule comes from a bad experience, add a short reason after a dash,
- at most 40 lines in total; move details to separate files and point to them with one line,
- save as UTF-8.

## 4. Check before handing over
- no passwords, keys, account numbers or personal data in the file (it is plain text and often ends up in a repository),
- no rules that contradict each other,
- show the finished file and ask what to strike or change before saving the final version.

## 5. After saving
Tell the user in one sentence that the rules apply from the next conversation, and that the best moment to add a rule is when they correct the assistant a second time on the same thing.
