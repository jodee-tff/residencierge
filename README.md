# The Residencierge

The AI concierge and tutor of the Exec AI Residency. An interactive "learn Claude Code inside Claude Code" course, built by Justin Kabbani and Jodee Bibaeff. Modules 1 and 2 are built (lessons 1-1 to 2-5); Module 3 is under construction.

Format inspired by Carl Vellotti's CC for Everyone. All lesson content, scenario and data here are original.

## How to run it (the magic paste)

Open Claude Code (the Code tab in the Claude Desktop app, or `claude` in a terminal) and paste:

> Clone https://github.com/jodee-tff/residencierge into a new folder called residencierge, then read the file BOOTSTRAP.md inside it and follow its instructions exactly.

The Residencierge takes it from there. Point that first chat at your home folder (the one with your name on it), not an iCloud-synced folder like Documents on a Mac. The course then teaches the guest to move into the folder it creates, and the whole course flows in a handful of chats, with the lessons saying exactly when to open a new one.

A note on visibility: lessons quietly send the crew a one line ping when a lesson starts and finishes (the lesson number and your computer's username), so in-room help can find whoever needs it. Nothing else leaves your machine. After lesson 1-1, lessons chain inside the same chat with `/start-1-2` through `/start-2-5`; the scripts call for a fresh chat only twice (after 1-1 and after 1-6).

## The scenario

The guest has just bought **Burleigh Heads Coffee Co.** from Deano, who ran it for 19 years and left one messy folder behind. The loyalty program is quietly failing, the clues are scattered across the files, and the answer is hiding in the small print of an unopened flyer image.

## What's inside

- `BOOTSTRAP.md`, what Claude follows on first run
- `CLAUDE.md`, standing house rules loaded whenever Claude Code runs in this folder
- `lessons/`, the teaching method plus the three lesson scripts
- `.claude/commands/`, the `/start-1-1` to `/start-2-5` shortcuts
- `company-context/`, `inherited-chaos/`, `attachments/`, the scenario data (verification words: the handover notes and the company file each carry one, sitting near the top)
- `templates/`, the brief template plus the design studio: three ready-made loyalty card directions and the tested app base that lesson 2-3 builds from
- `organised/`, `outputs/` and `builds/` (the Module 2 workspace), the only folders the concierge writes into

## Lesson map

- **1-1 Welcome.** The three rules (you talk I do, the misnomer, raise your hand for Jodee or Erik), the scenario, housekeeping.
- **1-2 The Inheritance.** Folder tour, what an .md file is, seeing files for real (Finder or File Explorer beside the Claude app), the hidden-word verification, Claude reads and summarises, first file created by conversation.
- **1-3 Working the Files.** The @ mention, patterns from messy reviews, cross-file contradiction (500 cards, 9 redemptions), the flyer image reveal (stamps expire in 14 days), quick live web research, and a board-ready insight brief built from the template.
- **1-4 Commands and Navigation.** Slash commands as saved instructions, the screenshot-and-ask move, and plan-before-do, practised by organising the inherited files.
- **1-5 Agents.** Three parallel investigators answer the three never-answered questions at once; the owner picks the first move.
- **1-6 Project Memory.** CLAUDE.md as the business brain: the owner's details go on the card, verified with his own eyes, then proven in a fresh chat. Closes Module 1.
- **2-1 Setup.** The memory proof, the module map, the build workspace and a personality pick, flowing straight into 2-2 in the same chat.
- **2-2 Plan.** Needs, wants and declared assumptions become BUILD-PLAN.md; the look is chosen from three ready-made design directions.
- **2-3 Build and Iterate.** The card is built from the plan on the tested design base, test-driven, then iterated with the how-to-ask-for-changes list.
- **2-4 GitHub.** The off-site safe: browser handshake, private repository, version 1 committed and pushed.
- **2-5 Go Live.** Vercel via GitHub, a short production URL, the locked-door choice, the phone moment and the what-you-actually-did list. Ends at the construction rope (Module 3, Your Business).

## Personalising for other guests

This copy greets Justin Kabbani by name (see `BOOTSTRAP.md` and `lessons/1-1-welcome.md`). For the full version, each guest gets their own copy with their name and, eventually, their own business as the scenario.
