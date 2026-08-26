# The Residencierge

The AI concierge and tutor of the Exec AI Residency. An interactive "learn Claude Code inside Claude Code" course, built by Justin Kabbani and Jodee Bibaeff. Lessons 1-1 to 1-3 are built; the rest is under construction.

Format inspired by Carl Vellotti's CC for Everyone. All lesson content, scenario and data here are original.

## How to run it (the magic paste)

Open Claude Code (the Code tab in the Claude Desktop app, or `claude` in a terminal) and paste:

> Clone https://github.com/YOUR-USERNAME/residencierge into a new folder called residencierge, then read the file BOOTSTRAP.md inside it and follow its instructions exactly.

Replace YOUR-USERNAME with the GitHub account this repo lives under. The Residencierge takes it from there. After lesson 1-1, each lesson starts with a fresh chat pointed at the residencierge folder: `/start-1-2`, then `/start-1-3`.

## The scenario

The guest has just bought **Burleigh Heads Coffee Co.** from Deano, who ran it for 19 years and left one messy folder behind. The loyalty program is quietly failing, the clues are scattered across the files, and the answer is hiding in the small print of an unopened flyer image.

## What's inside

- `BOOTSTRAP.md`, what Claude follows on first run
- `CLAUDE.md`, standing house rules loaded whenever Claude Code runs in this folder
- `lessons/`, the teaching method plus the three lesson scripts
- `.claude/commands/`, the `/start-1-1` to `/start-1-3` shortcuts
- `company-context/`, `inherited-chaos/`, `attachments/`, `templates/`, the scenario data (verification words hidden inside: Deano's notes and the company file each carry one)
- `organised/` and `outputs/`, the only folders the concierge writes into

## Lesson map

- **1-1 Welcome.** The three rules (you talk I do, the misnomer, raise your hand for Jodee or Erik), the scenario, housekeeping.
- **1-2 The Inheritance.** Folder tour, what an .md file is, seeing files for real (Finder or File Explorer beside the Claude app), the hidden-word verification, Claude reads and summarises, first file created by conversation.
- **1-3 Working the Files.** The @ mention, patterns from messy reviews, cross-file contradiction (500 cards, 9 redemptions), the flyer image reveal (stamps expire in 14 days), quick live web research, and a board-ready insight brief built from the template. Ends at the construction rope.

## Personalising for other guests

This copy greets Justin Kabbani by name (see `BOOTSTRAP.md` and `lessons/1-1-welcome.md`). For the full version, each guest gets their own copy with their name and, eventually, their own business as the scenario.
