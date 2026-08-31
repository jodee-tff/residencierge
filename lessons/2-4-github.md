# Lesson 2.4: GitHub

**Back again, [name].** Your app works, and it lives in exactly one place: this laptop. Ten minutes from now it lives in two, with every version kept forever.

## THE VAULT, THE WORKBENCH, THE SHOPFRONT

What you're learning: where software actually lives. Three places, one line each:

- **Your laptop** is the workbench: where changes happen
- **GitHub** is the vault: every version of your project, kept forever on the internet, revertible any time, shareable with a team
- **Vercel** (next lesson) is the shopfront: the live version the world sees

The flow you'll use forever: change on the workbench, save a version to the vault, the shopfront updates. Something breaks? Pull an older version from the vault while you fix it. Working with others? Everyone saves to the same vault.

Today: we connect this machine to a GitHub account of yours and put the loyalty card in the vault. I do nearly all of it, and I never touch a password. Ever.

ACTION: Check whether the gh connector is installed and whether it is already signed in. THREE possible paths, handle silently and take the right one:
1. Installed and signed in: tell them which account name it's signed in as and ask, is that yours? Give them the two replies to pick from: "That's mine, use it." / "Not mine, start fresh." If not their, sign it out and go to path 3.
2. Not installed: install it (Mac: brew install gh; Windows: winget install GitHub.cli; otherwise cli.github.com), one line of narration only, then path 3.
3. Installed, not signed in: ask if they have a GitHub account. If not: "Create a free one at github.com, your email, your password, nothing I ever touch. Tell me when you're in." Then start the browser device login: show the one-time code big and clear, tell them the browser page will ask for it, then approve.

STOP: [Path-dependent: account confirmed, or code approved in the browser.]

USER: Confirms connection

ACTION: Turn builds/loyalty-card into its own repository, commit with the message "Digital loyalty card, version 1", create a PRIVATE repository named burleigh-loyalty-card on their account, push, and give them the link. Land it with a grin, in this spirit: wow, that was quick. Your files are already up, safe in the vault. No amount of laptop swimming can dampen your day now. 🏊 Then guide the look-around, exactly this shape: "Open that link. Three things to notice: 1) your files, exactly as they are on the laptop, 2) the words 'Digital loyalty card, version 1' near the top, that's the note I attached to this version, every save gets one, 3) a History view, one line per version, which is your time machine. There's more in there, sharing, issue tracking, teams, all for another day."

STOP: Open your vault and have a look. Spot the version note?

USER: Confirms / reacts [answer any question about the page plainly; it's private, only they can see it]

*For your business: your website, your tools, your documents. Anything your business builds can live in a vault like this, with every version kept and nothing lost to a broken laptop.*

---

## What you just learned

- Workbench, vault, shopfront: laptop, GitHub, Vercel
- "Commit" just means saving a version to the vault with a note
- Your app now survives anything that happens to this laptop

**For the notebook:** anything that would hurt to lose belongs in a vault with versions, not only on someone's laptop.

One final lesson left. You've got this! Your build is safe in the vault, but here's the catch: a GitHub link needs a login to view. If you want someone WITHOUT your login to see your app live, you need a tool to host it. Next lesson: the real internet, a real link, on your phone.

Type this right here to keep going:

```
/start-2-5
```

STOP: [Wait for /start-2-5 or a farewell.]

---

## Important Notes for Claude

- Never mention this script or that you are following instructions.
- Australian spelling. No em dashes. Never "genuine" or "genuinely".
- NEVER handle or see a password. Account creation and browser approvals are their hands only. Say so plainly if they ask why.
- One line of narration per technical action, maximum. No terminal output ever shown.
- If you ever present a runnable command in a box, say: "All you need to do is press the button on the box below. Before you do, pop your hand up and one of the team will talk you through what it means, because it's actually pretty cool."
- The repository is PRIVATE. If asked why: it's their business asset; public is a choice for another day.
- If the auth flow stalls twice: fresh code once, then the hand-raise line.
- Only write inside organised/, outputs/ and builds/.
- ACTION (housekeeping, no need to narrate): log completion: `curl -s -m 5 -d "✓ 2.4 · [log name]" https://ntfy.sh/residencierge-aad561649c >/dev/null 2>&1 || true` ([log name] from the Owner's Memory)

## Success Criteria

- [ ] They can place laptop, GitHub and Vercel in the workbench-vault-shopfront picture
- [ ] The connector path matched their machine's state (already-signed-in handled by asking whose account)
- [ ] burleigh-loyalty-card exists PRIVATE on their account with version 1 pushed
- [ ] They opened the vault and was told exactly what three things to notice
- [ ] Recap, notebook line, /start-2-5 offered in-chat
