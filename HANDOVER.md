# Handover: iterating on The Residencierge in Claude Code

For Jodee. Carry this into a Claude Code session when you want to test or extend the course.

**Building new lessons? Read `builders/PROJECT-MEMORY.md` FIRST.** It is the full project recap: people, event, legal rule, script format, writing rules, scenario canon, the build brief for Modules 1 and 2, and the companion website link. This file covers testing; that file covers building.

## To test it exactly as Juz will

1. Put this folder somewhere sensible, for example `~/Documents/residencierge` (or run the clone prompt from the README).
2. Open Claude Code IN that folder (Desktop app: point the Code tab at the folder; terminal: `cd` there, run `claude`).
3. Type `/start-1-1` and play the guest. Then fresh chats for `/start-1-2` and `/start-1-3`.
4. Test the failure paths on purpose: wander off script, claim you can't see a file, guess the flyer twist early, ask for lesson 1-4. Watch how it recovers.

## Prompt to paste into Claude Code when extending it

> Read HANDOVER.md, CLAUDE.md, lessons/SCRIPT_INSTRUCTIONS.md and all three lesson scripts in lessons/ in this folder. This is The Residencierge, a scripted in-tool course for the Exec AI Residency (non-technical CEO guests, 31 Aug to 3 Sept 2026, Mondrian Gold Coast; builders Justin and Jodee; in-room help Jodee and Erik). Keep the exact script format: STOP / USER / ACTION markers, Important Notes, Success Criteria, fourth wall never broken. Hard writing rules: Australian spelling, no em dashes ever, never the word "genuine" or "genuinely". UI references must match the Claude Desktop app Code tab as at August 2026: the left sidebar is chats and projects navigation, files are viewed in Finder or File Explorer beside the app, @ in the message box opens the file picker. Help me test the current lessons, then draft new ones when I describe them.

## Design decisions already made

- Format follows the CC for Everyone method; content is original (Carl Vellotti's repo has no open licence, so nothing is copied).
- Compressed pacing on purpose: bundle related concepts into one message, but only one guest action per turn (lesson 1-2 covers eight concepts in five stops).
- Verification words hidden in the data (WOMBAT in Deano's notes, MACADAMIA in the company file) so the tutor can confirm the guest truly opened the right file.
- The mystery arc in 1-3 reveals in strict order: reviews pattern, then 500 cards vs 9 redemptions, then the flyer's 14 day expiry. Scripts forbid spoiling early.
- Carl's "Full Stack PM account" plug is replaced by: progress saves itself in the folder, background materials live in the Exec AI Residency Hub, feedback is filed to outputs/feedback.md for Justin and Jodee.
- The wider curriculum plan, four work zones model, and the control/nightly-sync design (per-guest private repos, /pack-down, /start-day, hooks) live in the Cowork project doc `claude/cc4e-course-analysis.md`.

## Setup clinic checklist (run per machine, 8:30 Sunday)

The bootstrap now runs a silent pre-flight (write test, enclosing git repo and gitignore shadowing, cloud-sync path). The human clinic should additionally confirm: Claude Desktop installed and signed in, admin rights available, the residencierge folder cloned OUTSIDE any synced or git-managed parent (a plain `~/Documents/residencierge` is ideal), and the @ picker shows course files when typing @ in a chat pointed at the folder. Jodee's own machine is the known exception: her home folder is a git repo with an ignore-everything rule, so on her machine the picker hides the files by design.

## Next lessons on the roadmap (not yet built)

- 1-4 Commands and navigation (trimmed), then the vibe coding wing: plan, build, GitHub, go live on Vercel, on a small piece of the guest's own one-page brief.
- Swap the coffee shop for each guest's real business once the format is approved.
