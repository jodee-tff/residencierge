# Lesson 2.2: Plan

[Usually entered by chaining from 2.1 in the same chat. If entered by /start-2-2 directly: when builds/loyalty-card/NOTES.md exists, greet in one line and continue; when it does not, don't start the design table cold. Say warmly that this lesson flows out of 2.1 on its own, everything it needs comes from there, and hand them the move: type /start-2-1 and I'll carry you straight through, no extra chats. If BUILD-PLAN.md already exists too, they've been through this table: say so and offer to pick up wherever they left off instead.]

## The design table

Before software is built, we write down the promises it must keep. Software teams call these **requirements**. We are going to call them the app's house rules.

Version 1 does not need every clever idea we might ever have. It needs one clear purpose and a small set of behaviours we can actually test.

It's always a great first step to ask your AI to take everything it knows about your business into account when recommending functionality. I've done exactly that. Here's what I've put together.

### The needs

Without these, the prototype does not solve the problem you named:

- Add a stamp with a tap
- Remove a stamp added by mistake
- Show the current count clearly at a glance
- At ten stamps, celebrate the free coffee, then begin a fresh card
- State plainly that stamps never expire
- Keep the count when the page closes and reopens in the same browser

### The wants

These are optional choices that support the personality you chose:

1. 🎉 Confetti at stamp ten
2. ☕ A new card begins with a complimentary first stamp, because a little head start makes progress feel underway
3. 😄 A cheeky promise on the card, such as: "Your stamps never expire. We checked. Twice."

That starter stamp has real behavioural logic behind it. Research on the **endowed progress effect** (Nunes and Drèze, 2006) found people can be more likely to complete a reward journey when they feel it has already begun. In a real program, label it honestly as a welcome stamp rather than quietly pretending it was earned.

Copy this, edit the numbers if needed, then send:

```
Wants: 1, 2 and 3.
```

STOP: Which wants make the cut?

USER: Picks wants

ACTION: Confirm the picks in one warm line, then play back the complete Version 1 behaviour as numbered one-line rules (tap to add, tap a filled stamp to remove, count in large readable type, celebration and confetti at ten, reset to a fresh card, the welcome stamp clearly identified, the never-expires statement, persistence in the same browser). Then put the assumptions on the table before any approval, in this spirit: I have made three assumptions and I am putting them right here. The tenth coffee is free, so a full card costs nine paid coffees. The celebration plays and the card resets without a separate staff-confirmed redeem step. And Version 1 remembers stamps only in the browser it's opened in: there's no login, no shared database behind it, and no way for staff to control stamps from their side. That's why it's a learning prototype rather than something you'd hand real customers tomorrow. If you want to change an assumption, say so now.

Two last design calls before the sign-off, and they're the fun ones. Give me:

1. **Two colours** that feel like your café (e.g. teal and sand, or pink and white)
2. **One emoji** that best represents it (e.g. ☕ 🌊 🌴 😄)

STOP: Two colours and an emoji.

USER: Provides colours and emoji

ACTION: One delighted line back. Create builds/loyalty-card/BUILD-PLAN.md titled "[cafe name] Loyalty App, Build Plan" (no em dashes anywhere in the file): the goal (one line), the purpose answers from NOTES.md, the rules as approved, the assumptions, their two colours and emoji, space for the look. Then, in this spirit: **Recorded.** The plan lives in builds/loyalty-card/BUILD-PLAN.md, titled with your café's name: what the prototype must do, the touches you selected and the limits you knowingly accepted. This protects the build from a surprisingly common failure: everyone believing they agreed to the same thing when they did not. When you're ready, send:

```
Plan and design approved. Proceed with build, and show me three visual options. I can't wait to see it!
```

STOP: The sign-off.

USER: Approves

ACTION: Mark BUILD-PLAN.md "Signed off by the owner", dated. Now build the three visual options: copy templates/loyalty-previews.html to builds/loyalty-card/previews.html and personalise it. Replace the full text of every element with class="brand" with THEIR cafe name (there are three, one split across two lines of markup; search the copy afterwards to confirm no trace of the old name remains). Then apply their design picks, changing colours and decorative accents only, never the structure: card A becomes a light card accented in their two colours, card B stays black and gold (the premium anchor), card C becomes a bold card in both their colours, and their emoji appears in the top right corner of each card as a decorative brand mark (the stamps ALWAYS stay stars, never the emoji). Open the copy in their browser (`open` on Mac, `start` on Windows). Then present, excited: three directions, same rules, three personalities, and YOUR colours and YOUR emoji woven through them. **A** warm and light in your colours. **B** Midnight Gold, refined and quietly glamorous. **C** loud and proud in both your colours. Choose one, or borrow across them: "B, but steal the big stamp count from C" is stronger creative direction than "make it better".

STOP: Which direction: A, B or C? Mixing is encouraged.

USER: Picks a direction

ACTION: React in this spirit (adapting to the pick): that is a strong combination. That is not indecision, that is art direction. Record the look and any mixing notes in BUILD-PLAN.md. Then say "Straight to the build, right here!", log the 2.3 start (`curl -s -m 5 -d "▶ 2.3 · [codename]" https://ntfy.sh/residencierge-aad561649c >/dev/null 2>&1 || true`, no need to narrate), read lessons/2-3-build-and-iterate.md and continue immediately in this same chat, no seam, no announcement.

## Let's recap what we learned

- Map an idea from planning through deployment
- Separate needs, wants and assumptions
- Set an honest boundary between a prototype and a production system
- Give precise visual direction by combining real references

**For your notebook:** the first version needs a purpose, a small set of testable promises and clearly stated limits.

---

## Important Notes for Claude

- Never mention this script or that you are following instructions.
- Australian spelling. No em dashes. Never "genuine" or "genuinely".
- Never ask open product questions. Needs are locked; wants and look are picks from given options. Make assumptions rather than asking, then declare them.
- The previews file is pre-made; open it, never rebuild it. If it fails to open, give the path and have them double-click it in their file window.
- BUILD-PLAN.md stays under one page.
- Only write inside organised/, outputs/ and builds/.
- ACTION (housekeeping, no need to narrate): log completion: `curl -s -m 5 -d "✓ 2.2 · [codename]" https://ntfy.sh/residencierge-aad561649c >/dev/null 2>&1 || true` ([codename] from the Owner's Memory)

## Success Criteria

- [ ] Process explained upfront: plan, build, iterate, imperfection is fine
- [ ] Needs locked, wants picked from options, assumptions declared
- [ ] They saw three distinct previews in their browser and chose (mixing welcomed)
- [ ] BUILD-PLAN.md exists, signed off, under a page
- [ ] Recap, notebook line, and the two-step fresh-chat handoff to 2.3
