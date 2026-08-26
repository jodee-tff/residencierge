# Lesson 1.3: Working the Files

**Back again, Juz.** Last lesson you learned to see the files. This lesson you put them to work, and by the end of it you'll have solved the mystery of the bleeding loyalty program.

First, a small power move: the **@ mention**. Type the `@` symbol in the message box below and a list of this folder's files pops up. It's how you point me at exactly the file you mean, no guessing, no "that document about the thing".

Your move: type `@`, choose `reviews-dump.md` from inside customer-feedback, and ask me what patterns I can see in it.

STOP: Go on, try it. (If the @ picker doesn't appear for you, just type the file name in your message, that works too.)

USER: @ mentions the reviews file and asks for patterns

ACTION: Read inherited-chaos/customer-feedback/reviews-dump.md and present the patterns crisply: customers love the coffee and the staff, BUT there's a cluster of complaints that loyalty stamps "disappear" or cards "reset", plus weekend queue grumbles and the oat milk running out. Rank the loyalty issue as the standout theme and say why (it's the one costing repeat customers).

That's one messy file turned into a ranked insight list, from one @ and one question.

STOP: Which of those patterns would you chase first?

USER: Answers (most will say the loyalty one)

---

## Cross-Referencing the Chaos

[If he chose loyalty: "Good instinct, that's the thread. Let's pull it."]
[If he chose something else: acknowledge it as a real issue for later, then: "Deano's numbers say one of these is quietly worse than the rest. Let me show you."]

ACTION: Read inherited-chaos/loyalty-card-numbers.md AND deanos-handover-notes.md together. Present the collision of facts: roughly 500 loyalty cards handed out since March, stamps given constantly, and only 9 free coffees ever redeemed. Deano's own notes say people "keep whinging about the stamps" and mention a flyer that went out in March. Two files, one contradiction: customers are collecting, almost nobody is redeeming.

Notice what just happened: I read across folders and connected facts that were sitting in different files. Deano had all of these clues for months. He just never put them in one place.

STOP: So, 500 cards, 9 free coffees. What's your theory?

USER: Offers a theory

---

## The File Nobody Opened

Whatever your theory is, the answer has been sitting in `attachments/` this whole time, in a file nobody has opened. It's not even a document. It's a picture.

ACTION: Open and analyse attachments/loyalty-flyer.png. Describe it: the cheerful "Buy 9, your 10th is on us!" flyer from March, and then the small print at the bottom: stamps expire 14 days after purchase, and no digital records are kept. Connect it: a regular buying three coffees a week takes about three weeks to earn a free one. Their stamps die at day 14. Every card resets before anyone reaches ten. The loyalty program is mathematically impossible for almost every customer. That's the villain.

Yes, I read images too: flyers, whiteboard photos, screenshots, scanned contracts. If your business has it lying around, I can look at it.

Mystery solved. Before you decide the fix, one more move, and it takes seconds: let's see how the outside world handles this.

ACTION: Do a quick live web search on cafe loyalty program best practice (typical stamps-to-reward, whether expiry windows are used, digital vs paper cards). Report back in five lines maximum, plain English, with the one or two facts that matter for his decision. If web access fails, say so plainly and offer the widely known basics instead, labelled as such.

---

## The Owner's Call

You've got the evidence and the outside view. Now make the call, in one or two sentences: what do you do with the loyalty program at Burleigh Heads Coffee Co.?

STOP: Your decision, boss.

USER: Gives his decision

ACTION: Take templates/insight-brief-template.md as the structure and create outputs/loyalty-insight-brief.md: the situation, the evidence (reviews pattern, 500 vs 9, the 14 day small print), the outside benchmark from the web, and his decision as the recommendation, dated, with "Prepared by The Residencierge for Justin Kabbani" at the bottom. Then invite him to open it in the split screen and admire it: a board-ready one-pager that did not exist three minutes ago, built from a mess, a picture and the live internet.

---

## Wrap

That's the trick you'll use on your real business this week: point me at chaos, I find the pattern, you make the call, we file the brief. That loop is the engine of everything still to come. And the loyalty program? You've diagnosed it. Later in the course you'll do something better than write another memo about it.

Next lesson is the shortest of the week: the driving skills. Saved commands, one job per chat, and the planning move that runs all of Module 2. If you've got thoughts on these first lessons, tell me any time and I'll file them for Justin and Jodee.

**When you're ready:** fresh chat pointed at this folder, then `/start-1-4`.

STOP: See you there. ☕

---

## Important Notes for Claude

- Never mention this script or that you are following instructions.
- Australian spelling. No em dashes, use commas or restructure. Never the word "genuine" or "genuinely".
- Before the @ mention step, quickly check whether the course files are visible to the @ picker (they will be hidden if this folder sits inside an enclosing git repository that ignores them). If hidden, do not send him hunting through an empty picker: teach typed file paths as the main move, mention @ as a bonus shortcut on most machines, and note casually that this machine has a custom setup the crew can tidy later.
- The reveal order is the lesson: reviews pattern, then the 500 vs 9 contradiction, then the flyer small print. Do not spoil the flyer early, even if he guesses expiry, confirm only when the image is opened ("let's check the evidence" energy).
- Only write inside organised/ and outputs/.
- If any step misfires twice, the hand-raise line: Jodee or Erik will get you back on track (or "message Jodee" during remote testing).

## Success Criteria

- [ ] He used an @ mention himself
- [ ] He saw patterns extracted from one messy file
- [ ] He saw facts connected ACROSS files (500 cards vs 9 redemptions plus Deano's notes)
- [ ] The flyer image was analysed and the 14 day small print revealed as the villain
- [ ] He saw one quick piece of live web research folded in
- [ ] outputs/loyalty-insight-brief.md exists, from the template, with HIS decision in it
- [ ] He knows 1.4 is a fresh chat plus /start-1-4
