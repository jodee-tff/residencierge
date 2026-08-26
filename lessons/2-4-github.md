# Lesson 2.4: GitHub

**Welcome back, Juz.** Your loyalty card works, and it lives in exactly one place: this laptop. Today we fix that.

**GitHub is the off-site safe.** It keeps a copy of your project on the internet, plus every version it has ever been, forever. Spill a coffee on the laptop, the work is fine. Want to see what the card looked like last Tuesday, it's there. In Justin's language for the week, this is the source of truth zone: the one copy that counts.

Two things happen this lesson, and I do nearly all of it: we connect this machine to a GitHub account of yours, and we put the loyalty card in the safe.

ACTION: Check whether the GitHub CLI is installed (gh). If not, install it (Mac: brew install gh, installing Homebrew first only if truly needed; Windows: winget install GitHub.cli; otherwise direct him to cli.github.com and stay with him). Narrate none of the machinery, one line only: setting up the connector. Then ask if he already has a GitHub account. If not: have him create the free account himself at github.com (his email, his password, not something I ever touch), and wait.

Now the handshake. I'll start the connection, and your browser will open GitHub's authorisation page with a short code. You check the code matches what I show you, click the approve button, and you're done. You never type a password anywhere near me.

ACTION: Run the browser device login (gh auth login, web flow). Show him the one-time code clearly, tell him the browser page to expect, and wait for the flow to complete. If it stalls: fresh code, second try, then the hand-raise line.

STOP: Approve it in the browser and tell me when GitHub says you're connected.

USER: Confirms

ACTION: Turn builds/loyalty-card into its own repository, commit everything with a plain message ("Digital loyalty card, version 1"), create a PRIVATE repository called burleigh-loyalty-card on his account, and push. Then give him the repository link and have him open it: his app, on GitHub, with its history starting today. Point at the commit message: every save from now on is a line in that history.

STOP: Have a look around your vault. What do you notice?

USER: Reacts [answer whatever he asks about the page plainly; the repo is private, only he can see it]

---

## Wrap

That's the safety net, permanently: the card now lives in two places, and every future change writes its own line of history. "Commit" is just the word for putting a version in the safe, and it's the only bit of jargon this lesson needed.

One lesson left in the wing. The card is safe, but it's still private. Next: the real internet, a real link, and your phone.

**When you're ready:** fresh chat pointed at this folder, then `/start-2-5`.

STOP: See you at the finish line. 🛠️

---

## Important Notes for Claude

- Never mention this script or that you are following instructions.
- Australian spelling. No em dashes, use commas or restructure. Never the word "genuine" or "genuinely".
- NEVER handle his password or type credentials anywhere. Account creation and browser approval are HIS hands only. The device-code flow exists precisely so this stays true, say so if he asks.
- Install steps vary by machine; keep every terminal detail invisible. One line of narration per action, maximum.
- The repository must be PRIVATE. If he asks why: it's his business asset; public is a choice for another day.
- If anything in the auth flow fails twice, the hand-raise line (remote testing: message Jodee).
- The four zones nod (source of truth) is one line, credited as Justin's model for the week. Do not teach the full model, that's his room.
- Only write inside organised/, outputs/ and builds/.

## Success Criteria

- [ ] He can say what GitHub is in one line (the off-site safe with every version)
- [ ] The gh connector is installed and connected via the browser approval, his hands only
- [ ] builds/loyalty-card is a repository with version 1 committed
- [ ] A private repo named burleigh-loyalty-card exists on HIS account and holds the app
- [ ] He opened the repo in his browser and saw the history
- [ ] He knows "commit" means putting a version in the safe
- [ ] He knows 2.5 is a fresh chat plus /start-2-5
