# The Residencierge: Project Memory

Full recap for builders. Last updated 26 August 2026 from Jodee's Cowork session. Read this top to bottom before building anything. This folder (`builders/`) is for Justin and Jodee only; guest-facing lessons never mention it or draw attention to it.

## What this project is

The Residencierge is the AI concierge and tutor of the **Exec AI Residency** (execairesidency.com), a three day retreat for CEOs, 31 August to 3 September 2026, Mondrian Gold Coast. It teaches Claude Code INSIDE Claude Code: scripted interactive lessons the guest experiences as a conversation, no videos, no manuals. The guest pastes one prompt, the course lands on their laptop, and the concierge teaches by having them do the work.

## The people

- **Justin Kabbani ("Juz")**: host of the Residency, co-builder of this course, and its first test guest. The current demo greets him by name.
- **Jodee Bibaeff**: co-builder and operator. Based in Perth (AWST).
- **Erik Bibaeff**: in-room support alongside Jodee.
- **Guests**: eight curated CEOs, non-technical, mixed Mac and Windows laptops, arriving with admin rights and Claude Desktop per pre-event comms.

**Branding rule, hard:** everything says Exec AI Residency or Justin Kabbani. Never any other business name.

## The event context this must fit

From the 25 August planning call: Day 1 runs an 8:30 to 9:00 setup clinic (Jodee and Erik), then a one hour orientation, then just-in-time teaching. Guests pick a business problem and write a one page brief before lunch. Obsidian was removed from the curriculum. The conceptual model for the week is four work zones: private draft, team-shared work, source of truth, and live/public work. The Residency's Day 1 will use a roughly 90 minute cut of this course; the full course is self-paced homework and post-event material.

## Origin, and the one legal rule

Format inspired by Carl Vellotti's "CC for Everyone" (ccforeveryone.com, repo: github.com/carlvellotti/claude-code-everyone-course). **His repo has NO open licence. Never copy his wording, his scenario, his data files or his project builds. Ever.** The METHOD is fair to reimplement (scripted lessons, slash commands, STOP/USER/ACTION markers, success criteria, hidden verification words, learn-by-doing). Every word of Residencierge content must be original. Specific trap: Carl's Module 2 build is a Coffee Personality Quiz; ours must be something else (recommendation below).

## The name

"The Residencierge" (residency + concierge), chosen to sit in the family of Justin's named tools (Curious George, The Instructionator, Prompt Extractor Deluxe, The Smooth Promptenator).

## What exists right now

**This folder (the course repo):**
- `BOOTSTRAP.md`: what Claude follows on the first paste. Includes a SILENT pre-flight: write test in outputs/, detection of an enclosing git repo whose gitignore shadows the course files (this is real, it happened on Jodee's machine, her home folder is a git repo with an ignore-everything rule that blinds the @ file picker), and cloud-sync path detection. If files are picker-hidden, the tutor teaches typed paths in 1-3 instead and never argues.
- `CLAUDE.md`: standing house rules for any session in this folder.
- `lessons/SCRIPT_INSTRUCTIONS.md`: the teaching method. Applies to every lesson, always.
- `lessons/1-1-welcome.md`, `1-2-the-inheritance.md`, `1-3-working-the-files.md`: the three built lessons.
- `.claude/commands/start-1-1.md` etc: the slash commands (template: silently read SCRIPT_INSTRUCTIONS, read the lesson script, begin immediately).
- Scenario data: `company-context/` (about file, menu and prices), `inherited-chaos/` (Deano's handover notes, customer-feedback/reviews-dump.md, loyalty-card-numbers.md), `attachments/loyalty-flyer.png`, `templates/insight-brief-template.md`.
- `organised/` and `outputs/`: the ONLY folders the tutor may write into.
- `HANDOVER.md`: test protocol and extension prompt.
- `README.md`: human-facing overview and the clone paste prompt (contains a YOUR-USERNAME placeholder until the GitHub repo URL is settled).

**The companion website** (reference pages in the style of Carl's site, Home + Module 0 + Module 1, full locked course map, jkweb dark and gold design, desk bell 🛎️ brand mark):
https://claude.ai/code/artifact/cc7683bf-007d-4bbd-a5aa-a96a84b7e5a3
Private to Jodee until shared from the page's share menu. The paste prompt on its page 0.2 also carries the YOUR-USERNAME placeholder; update it (via the Cowork session that published it) once the repo URL exists. Module 3 shown on the site ("Your Business": real files, connect your tools, weekly workflow) is a proposal, shape not yet agreed.

## The lesson script format (follow exactly when building new lessons)

- One file per lesson at `lessons/N-N-slug.md`, one command at `.claude/commands/start-N-N.md`.
- Markers: `STOP:` (wait for the guest), `USER:` (expected reply shape), `ACTION:` (the tutor actually does it), `[square brackets]` (conditional guidance).
- Each lesson ends with two blocks: **Important Notes for Claude** (lesson-specific coaching, fourth wall rule, writing rules, folder-write limits) and **Success Criteria** (a checklist the tutor mentally ticks).
- **Never break the fourth wall.** The guest never hears about scripts or instructions.
- **Compression rule** (Jodee's explicit requirement): bundle two or three related concepts per message, but only ONE guest action per turn. Benchmark: lesson 1-2 delivers eight concepts in five STOPs. Lessons should feel quick.
- End every lesson with the handoff: start a fresh chat pointed at this folder, then `/start-N-N` for the next lesson, plus the note that slash commands only appear in chats pointed at the folder.
- Durations so far: 1-1 about 5 minutes, 1-2 about 15, 1-3 about 20. Keep new lessons in that range.

## Writing rules (hard, non-negotiable, apply to every file and every tutor utterance)

- Australian English spelling, always.
- NO em dashes, ever. Commas or restructure.
- Never the words "genuine" or "genuinely". Also avoid "straightforward" and "honestly".
- Voice: warm, confident, lightly playful, concierge of a very good hotel. Plain English; any technical term arrives with a one line analogy. Short messages.
- **Positioning, non-negotiable: "Justin teaches, this guides."** Justin Kabbani is the teacher of the Residency and the source of the method; the Residencierge is the guide that walks guests through the doing between his sessions. Never write a lesson that positions the concierge as the expert, the instructor or the origin of the thinking. This replaced an earlier "you talk, I do" framing on 26 Aug; carry the new one into every lesson built from here.
- The help rule: whenever the guest is confused, unsure where to start, or not seeing what they should: try one simple fix, then "raise your hand and Jodee or Erik will come over and get you back on track" (remote testing: "message Jodee").

## UI reference rules (as at August 2026, Claude Desktop app)

Guests use the Code tab of the Claude Desktop app, NOT a code editor. The app's left sidebar is navigation for chats and projects, never the guest's files. Seeing files means Finder (Mac) or File Explorer (Windows) in a split screen beside the app; the tutor opens the folder with `open .` or `explorer .`. The `@` symbol in the message box opens a file picker; typed paths are the universal fallback. Every ACTION needs a Mac and a Windows path. If the guest's screen does not match expectations, believe the guest, ask what they see, adapt. Never insist on a pixel.

## Scenario canon (do not contradict any of this)

**Burleigh Heads Coffee Co.**, the little cafe on the point at Burleigh Heads QLD, bought this week by the guest from **Deano** (Dean Maloney), who ran it 19 years and retired to fish. Cast: **Priya** (head barista, runs the floor, pay rise due October, her nan's macadamia cookie recipe stays in her family), **Callum** (late Mondays, blames the surf report), **Tommo** (the roaster in Currumbin), **Big Al** (machine servicing). Facts in play: oat milk runs out every Saturday, the weekend queue from 8 to 10am is feral, wifi password flatwhite2007, council inspection in November, flat white $5.00 small and $5.80 large.

**Hidden verification words** (the tutor asks the guest to find one with their own eyes, proving they truly opened the file): WOMBAT in `inherited-chaos/deanos-handover-notes.md`, MACADAMIA in `company-context/about-burleigh-heads-coffee.md`. Convention: hide one per major new data file, and never reveal them unprompted.

**The Module 1 mystery, resolved in lesson 1-3:** reviews show customers love the cafe but complain their loyalty stamps "disappear"; Deano's numbers show about 500 cards handed out since March and only 9 free coffees ever redeemed; the unopened flyer image (`attachments/loyalty-flyer.png`) carries the villain in its small print: stamps expire 14 days after purchase and no digital records are kept, so nearly every card dies before reaching ten. Reveal order is strict: reviews pattern, then the 500 vs 9 contradiction, then the flyer. Never spoil the flyer early.

**Files the lessons create:** 1-2 creates `organised/owners-log.md`; 1-3 creates `outputs/loyalty-insight-brief.md` from the template, containing the guest's own decision. Feedback notes are appended to `outputs/feedback.md`.

## The account/plug replacement

Carl's course plugs a Full Stack PM account (progress, certificates, community). Ours instead: progress saves itself in the folder, background materials live in the guest's **Exec AI Residency Hub** (it exists, do not invent features for it), and feedback is filed to `outputs/feedback.md` for Justin and Jodee. No sign-ups anywhere.

## THE BUILD BRIEF: Modules 1 and 2, what to build next

**Module 1 completion** (Carl's module shape as the guide, all content original, cafe scenario continues):
- **1-4 Commands and Navigation.** The handful of moves worth knowing: `/resume` to pick up where you left off, plan-before-do for bigger asks, referencing files, keeping chats per task. Compressed hard; this is the shortest lesson.
- **1-5 Agents.** Parallel work: several Claudes at once. Natural cafe story: three questions Deano never answered (weekend staffing vs the queue, oat milk ordering, which menu items earn their place) investigated simultaneously, results compared. Optional taste of custom sub-agents as an advisory bench.
- **1-6 Project Memory.** CLAUDE.md as the business brain: the guest teaches the folder who they are and how the cafe works, then sees a fresh chat already know it. This lesson also plants the seed for the guests' own businesses. Fold a small celebration and a Module 2 preview into its ending (Carl gives this its own 1.8; we fold it in).

**Module 2, Vibe Coding** (five lessons, Carl's arc, original project):
- 2-1 Setup, 2-2 Plan, 2-3 Build and Iterate, 2-4 GitHub, 2-5 Go Live (Vercel).
- **Recommended build project: a digital loyalty card for Burleigh Heads Coffee Co.** It is the payoff of the whole story: Module 1 diagnosed the loyalty program (paper stamps that expire), Module 2 builds the fix, stamps that never vanish, live on the internet with a real link. Do NOT build a coffee personality quiz; that is Carl's exact project.
- 2-4 GitHub mechanics: the tutor installs the gh CLI (brew on Mac, cli.github.com otherwise) and drives the browser device-code login so the guest never types scary commands. Guests sign up to Vercel WITH GitHub so everything connects. 2-5 installs the Vercel CLI (`npm i -g vercel`) the same way.
- Every new lesson: fresh secret word in any new data file, Mac and Windows ACTION paths, Important Notes, Success Criteria, the compression rule, and the handoff footer.

**After building lessons:** create matching `.claude/commands/start-N-N.md` files, update `README.md`'s lesson map, and note that the companion website (artifact link above) will need its locked entries unlocked and reference pages written; that update happens in Jodee's Cowork session, which owns the artifact URL.

**The construction rope moves.** Whatever the last built lesson is, the rope line ("Justin and Jodee haven't finished building this wing yet") moves to its ending, and nothing is ever invented beyond it.

## Also agreed, build later (not now)

The control and nightly-sync layer for the Residency proper: per-guest private GitHub repos, auto-checkpoint hooks, `/pack-down` (end of day commit and push) and `/start-day` (morning pull and greeting) commands, the Mac mini as the nightly pull station, a consent line in the T&Cs, one repo per guest so nobody sees another's material. Full design lives in Jodee's Cowork project doc `claude/cc4e-course-analysis.md`.

## Open items

- GitHub repo URL not yet settled; README and the website's 0.2 page carry a YOUR-USERNAME placeholder.
- Module 3 ("Your Business") is a website proposal only, shape to be agreed with Justin.
- Whether to email Carl Vellotti for a friendly heads-up or blessing: suggested, not yet done.
- Juz's first test run of 1-1 to 1-3: scheduled for tonight, 26 August.
