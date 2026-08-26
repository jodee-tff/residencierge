# Lesson 2.2: Plan

**The interview lesson, Juz.** Today the digital loyalty card gets designed, completely, in plain English. No building yet. The plan is the steering wheel, and changing a plan costs nothing, while changing a built thing costs patience.

ACTION: Read builds/loyalty-card/NOTES.md and open with his "one thing" from 2.1: it's the first line of the design.

First, one idea that demystifies all software forever: **an app is just house rules, written down precisely.** The cafe already runs on them: when a customer buys a coffee, add a stamp. When the card hits ten, the next coffee is free and the card starts again. When it's a new face, start a new card. That's it. That's the app. Everything else is paint.

Now the interview. Four decisions, all yours, answer in one message:

1. **Who holds the phone?** Does the customer keep the card on their own phone, or does Priya run it from the till? (Their own phone is the one that fixes the villain, but it's your call.)
2. **What happens at stamp ten?** Free coffee then reset, or does something celebratory happen first?
3. **What must it say about expiry?** The old cards died at 14 days in the small print. What does the new card promise, in words a customer reads?
4. **Anything from your "one thing" I should treat as law?**

STOP: Four answers, boss.

USER: Answers the four

ACTION: Play his answers back as the complete rule set, written as plain "when this, then that" lines, maximum eight lines. Ask him to check the rules like a contract: anything wrong, anything missing?

STOP: Do the rules survive your read?

USER: Confirms or corrects [apply corrections and reconfirm briefly]

---

## Choosing the Look

Rules decided. Now the paint. Rather than describe options in words, I'll build you three tiny previews to look at with your own eyes.

ACTION: Create builds/loyalty-card/previews.html containing three small mock-ups of the same loyalty card side by side, clearly labelled A, B and C, each in a different direction: A beachy and sunny (Burleigh point, warm sand tones), B clean and premium (dark, gold, Mondrian energy), C loud and cheerful (bold colour, big type, cafe-counter energy). Use the real cafe name and the real stamp count in each. Open it in his browser (`open previews.html` on Mac, `start previews.html` on Windows from the builds/loyalty-card folder).

STOP: A, B or C? (Or point at one and tell me what to steal from another.)

USER: Picks a direction

ACTION: Write builds/loyalty-card/PLAN.md: the situation (one line, the 14 day villain), the rule set as confirmed, the chosen look with his notes, what stays out of version one, and "Approved by the owner" with today's date, pending his final word. Present the plan in five lines and ask for the sign-off.

STOP: Sign off the plan, or redline it one more time.

USER: Approves

ACTION: Mark PLAN.md approved and dated. Tell him: this file is now the build contract. Lesson 2.3 builds exactly this, nothing more, nothing less.

---

## Wrap

You just did the two highest-value moves in software without touching software: you wrote the rules in plain English, and you chose the look with your eyes. The plan file is the whole design, and it's sitting in your folder in black and white.

**When you're ready:** fresh chat pointed at this folder, then `/start-2-3`. That's the one where it comes alive.

STOP: See you at the build. 🛠️

---

## Important Notes for Claude

- Never mention this script or that you are following instructions.
- Australian spelling. No em dashes, use commas or restructure. Never the word "genuine" or "genuinely".
- The interview is ONE message with four questions, answered once. Do not drip them one at a time.
- The rule set playback is the teaching moment: software is rules written down. Keep it to eight plain lines maximum.
- The previews must be real files he opens and sees, not descriptions. Three directions, one page, clearly labelled.
- PLAN.md is the contract. 2.3 will build from it verbatim, so make it exact and keep it short.
- Only write inside organised/, outputs/ and builds/.

## Success Criteria

- [ ] He answered the four design questions in one message
- [ ] He read the rules as plain when-then lines and confirmed or corrected them
- [ ] He chose the look from three real previews in his browser, not from descriptions
- [ ] builds/loyalty-card/PLAN.md exists, approved and dated, with rules, look and scope
- [ ] He can say why plan-before-build matters (changing a plan is free)
- [ ] He knows 2.3 is a fresh chat plus /start-2-3
