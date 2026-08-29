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

## Build log: 26 August 2026, evening (Claude Code session with Jodee)

The build brief above is now DONE. What changed:

- **GitHub repo settled:** github.com/jodee-tff/residencierge (public). README, the website page 0.2 and all placeholders now carry the real URL.
- **Modules 1 and 2 built out:** lessons 1-4 (Commands and Navigation, plan-before-do on the council inspection), 1-5 (Agents, Deano's three unanswered questions in parallel), 1-6 (Project Memory, Owner's Memory section appended to CLAUDE.md, proof lands at the top of 2-1), 2-1 (Setup, memory greeting, builds/loyalty-card workspace, the "one thing"), 2-2 (Plan, four-question interview, when-then rules, three visual previews, PLAN.md as build contract), 2-3 (Build and Iterate, persistence beat, describe-what-you-see changes), 2-4 (GitHub, gh device flow, PRIVATE burleigh-loyalty-card repo, guest's hands only for all credentials), 2-5 (Go Live, Vercel via GitHub, the phone moment, the rope now ends here pointing at Module 3).
- **Module 2 project:** the digital loyalty card, per the brief. Never a personality quiz.
- **Write permissions widened:** CLAUDE.md now allows outputs/, organised/ and builds/, plus the single 1-6 exception for the Owner's Memory heading.
- **Pacing pass (Jodee's 26 Aug feedback):** pure "ready?" gates removed from 1-1, 1-2 and 1-3; every STOP in every lesson is now an action or a decision. New-lesson benchmark: three to five STOPs, each one earning its place.
- **Hidden words:** no new ones added. Jodee's rule, confirmed by Juz's instinct: the beat exists only where it teaches verification (WOMBAT in 1-2 stays). New lessons add no new data files, so no new words.
- **1-3's ending** now hands off to /start-1-4; the construction rope lives at the end of 2-5.
- **Companion website** updated the same evening: all Module 1 and 2 pages written and unlocked, rope moved to 2.5, prompt box label clipping bug fixed (overflow-x removed from .promptbox). Module 3 remains locked/proposal.

Open items that remain: Module 3 shape (with Justin), the per-guest repo control layer, the Carl Vellotti courtesy note, and Juz's full test run.

## Progress beacon: added 26 August 2026, later that evening

Every start command (and the BOOTSTRAP clone path) opens with a silent ping, and SCRIPT_INSTRUCTIONS rule 11 sends a completion ping when a lesson's success criteria are met. Channel: ntfy.sh topic `residencierge-f78fe9ea` (subscribe in the ntfy phone app or at https://ntfy.sh/residencierge-f78fe9ea). Format: "▶ N.N started · username" and "✓ N.N complete · username". Pings are best effort (5 second timeout, never block a lesson), disclosed in the README, and carry only the lesson number and the machine username. The topic string lives in a public repo, so treat it as demo-grade: rotate it, or retire it for the per-guest private repo layer, before the real cohort.

## Overnight rework: 27 August 2026, from Jodee and Erik's full test run (two Plaud recordings)

Every lesson rewritten against the recorded feedback. The standing law now lives in SCRIPT_INSTRUCTIONS (teaching pattern, pace rules, formatting, truth rules). Headlines:

- **Teaching pattern, every section:** say what's being learned and why FIRST, hand the exact copy-paste text for every guest input (never make them compose, choices are picks from given options), respond in one-line dot points, close with an italic "For your business:" transfer line. A new skill every turn. No empty "ready?" CTAs.
- **Scenario diet:** the previous owner is named at most twice per lesson, no backstory, "villain" banned. reviews-dump.md renamed inherited-chaos/customer-reviews.md; the word of the week now sits at the TOP of the handover notes (no hunting).
- **Chat flow fixed:** lessons chain in the SAME chat via typed /start commands. Fresh chats only after 1-1 (the folder move, now taught as an explicit two-step with the sidebar described) and after 1-6 (the memory proof). 2-1 chains automatically into 2-2. Chained lessons still send beacon pings; every lesson script now carries an explicit completion-ping ACTION.
- **1-4 rebuilt:** slash menu (spot, don't count), the screenshot-and-ask move (Jodee's request, taught as a first-class skill), plan-before-do on a DIGITAL job (organising inherited-chaos into organised/).
- **The design disaster, root-caused and fixed:** the old scripts specified rules but zero design direction, so preview and build quality depended on the guest session's model improvising, and the three previews were near-identical recolours. Now the repo ships templates/loyalty-previews.html (three deliberately distinct directions: A Burleigh Sunrise, B Midnight Gold, C The Point Pop) and templates/loyalty-card-base.html (a TESTED app base: tap-to-toggle stamps, add button, persistence, confetti and celebration at ten, head-start option, three themes via CONFIG). Lesson 2-2 opens the previews file; 2-3 builds by customising the base to the signed plan. Functionality verified by automated browser tests on 27 Aug (toggle, add, persist, complete, new card, all three themes).
- **2-5 hardened:** short project name (burleigh-loyalty) for a typeable URL, Vercel Deployment Protection handled as an explicit neutral choice with exact clicks, what-now FAQ, and the big ending: the what-you-actually-did list with technical names in brackets, the replicate-to-your-business map, both-outcomes reassurance.
- **/self-destruct built** (Jodee's request): typed DELETE EVERYTHING consent, Vercel project removal, manual GitHub deletion via the settings page (no scope elevation), folder to Trash never rm -rf, chats deleted by hand with instructions.
- Justin quotes rule: never attribute specific claims to Justin that he hasn't said; credit the method generally.

## 27 August 2026, morning: dynamic names and the Files panel

- **Names are dynamic now.** Scripts carry [name]; BOOTSTRAP and SCRIPT_INSTRUCTIONS rule 14 resolve it (Owner's Memory, then the computer account's display name, then ask warmly). Override: Justin Kabbani goes by Juz. Guest pronouns default to they/them. No more per-copy editing for the cohort.
- **The Files panel replaces the Finder split screen** as the primary way guests see files (Jodee's screenshot confirmed the Code tab's built-in panel, top right). Finder/Explorer stays as the scripted fallback. Rule 18 carries the details; lesson 1-2 teaches the panel.

## 30 August 2026: Justin's demo feedback, actioned

Justin's verdict on the demo run: extraordinary, keep the name, keep the quirk level. His feedback plus Jodee's decisions, now built:

- **See it empty first, everywhere:** organised/ before the owner's log (1.2), CLAUDE.md's empty card before the memory (1.6), outputs/ before the brief (1.3), builds/ before the app (2.3), organised/ before the tidy-up (1.4).
- **Owner's log reworked (1.2):** the concierge proposes an Owner's Log, the guest sees the empty folder, then two PERSONAL BEATS typed in their own words, never pasted: naming the cafe (a. Burleigh Heads Coffee Co. / b. The Bright & Burleigh Café / c. their own) and a day-one hunch about the loyalty problem. 1.3 now reads the hunch back after the flyer reveal and appends a verdict entry. [cafe name] flows through the whole course: the brief, the Owner's Memory, the previews copy and the built app all carry the guest's chosen name.
- **Models taught as 1.4 move four:** engines analogy, same prompt on Haiku then Opus picked from the bar below the message box (never /model), guest describes the difference, back to Sonnet. Experiential only, no benchmark claims in script. Room opens on Sonnet + Medium (Jodee's spoken line, see DELIVERY-NOTES.md).
- **Jodee leads the room:** 1.1 rule two names Jodee as presenter; SCRIPT_INSTRUCTIONS rule 11 and CLAUDE.md positioning updated. Never invent quotes from Jodee or Justin.
- **Files panel restored as the taught path** (Jodee's final call), Finder as fallback. Rule 18, 1.2, 1.6, 2.1, 2.3, plus the website.
- **builders/DELIVERY-NOTES.md** holds Jodee's spoken lines (safety line with the phone-home reveal, model line), timing plan, novice test protocol, reminders.
- **Working copy moved out of iCloud:** canonical local copy is now ~/residencierge (fresh clone; the old ~/Documents/residencierge copy is stale, Jodee to delete by hand). HANDOVER updated.
- **hub/** folder added to the repo: the standalone hub page plus a README for Justin to drop into the Exec Hub.
- Parked: localhost visual companion for visual learners (Justin's idea, post-residency). Pre-made GitHub/Vercel accounts: rejected, guests bring or create their own; GitHub signup goes in pre-event comms.
