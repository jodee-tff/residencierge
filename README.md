# The Residencierge

The AI concierge and tutor of the Exec AI Residency. An interactive "learn Claude Code inside Claude Code" course, built by Justin Kabbani and Jodee Bibaeff. Modules 1 and 2 are built (lessons 1-1 to 2-5); Module 3 is under construction.

Format inspired by Carl Vellotti's CC for Everyone. All lesson content, scenario and data here are original.

## How to run it (the magic paste)

Open Claude Code (the Code tab in the Claude Desktop app, or `claude` in a terminal) and paste:

> Clone https://github.com/jodee-tff/residencierge into a new folder called residencierge, then read the file BOOTSTRAP.md inside it and follow its instructions exactly.

The Residencierge takes it from there.

A note on visibility: lessons quietly send the crew a one line ping when a lesson starts and finishes (the lesson number and your computer's username), so in-room help can find whoever needs it. Nothing else leaves your machine. After lesson 1-1, each lesson starts with a fresh chat pointed at the residencierge folder: `/start-1-2` through `/start-2-5`.

## The scenario

The guest has just bought **Burleigh Heads Coffee Co.** from Deano, who ran it for 19 years and left one messy folder behind. The loyalty program is quietly failing, the clues are scattered across the files, and the answer is hiding in the small print of an unopened flyer image.

## What's inside

- `BOOTSTRAP.md`, what Claude follows on first run
- `CLAUDE.md`, standing house rules loaded whenever Claude Code runs in this folder
- `lessons/`, the teaching method plus the three lesson scripts
- `.claude/commands/`, the `/start-1-1` to `/start-2-5` shortcuts
- `company-context/`, `inherited-chaos/`, `attachments/`, `templates/`, the scenario data (verification words hidden inside: Deano's notes and the company file each carry one)
- `organised/`, `outputs/` and `builds/` (the Module 2 workspace), the only folders the concierge writes into

## Lesson map

- **1-1 Welcome.** The three rules (you talk I do, the misnomer, raise your hand for Jodee or Erik), the scenario, housekeeping.
- **1-2 The Inheritance.** Folder tour, what an .md file is, seeing files for real (Finder or File Explorer beside the Claude app), the hidden-word verification, Claude reads and summarises, first file created by conversation.
- **1-3 Working the Files.** The @ mention, patterns from messy reviews, cross-file contradiction (500 cards, 9 redemptions), the flyer image reveal (stamps expire in 14 days), quick live web research, and a board-ready insight brief built from the template.
- **1-4 Commands and Navigation.** Slash commands as saved instructions, one job per chat, and plan-before-do, practised on the November council inspection.
- **1-5 Agents.** Three parallel investigators answer Deano's three never-answered questions at once; the owner picks the first move.
- **1-6 Project Memory.** CLAUDE.md as the business brain: the owner's details go on the card, verified with his own eyes, then proven in a fresh chat. Closes Module 1.
- **2-1 Setup.** The memory proof, what vibe coding is, the build workspace, and the mission: a digital loyalty card that fixes the 14 day villain.
- **2-2 Plan.** The design interview, rules as plain when-then lines, three visual previews to choose from, and PLAN.md signed off as the build contract.
- **2-3 Build and Iterate.** The card is built from the plan, tested (stamps survive a closed page), then changed by describing what you see.
- **2-4 GitHub.** The off-site safe: browser handshake, private repository, version 1 committed and pushed.
- **2-5 Go Live.** Vercel via GitHub, a real production URL, and the phone moment. Ends at the construction rope (Module 3, Your Business).

## Personalising for other guests

This copy greets Justin Kabbani by name (see `BOOTSTRAP.md` and `lessons/1-1-welcome.md`). For the full version, each guest gets their own copy with their name and, eventually, their own business as the scenario.
