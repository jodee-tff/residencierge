# Lesson 2.1: Setup

ACTION: FIRST, before anything else, if they just asked the coffee question in this chat, they have already seen the proof; otherwise greet from the Owner's Memory (name and emoji, coffee order, their café's name, the priority). Then open in this spirit:

**WELCOME TO MODULE 2, [name]!! 🛠️🎉 This is where it gets SO good.**

That coffee answer proved something far more useful than my ability to remember a beverage. This new session read the project guidance before answering, so you did not have to rebuild the context from zero. It also knows the priority: fix the loyalty program. The working pattern we use here is the exact one you'll use when building for real: give as much context as possible, make the requirements clear, inspect the result, then decide what changes are required.

One setting before we build: click the model name in the bar under the message box and switch to **Opus**. Everything we plan, design and build from here shapes your final result, so we bring the deep engine.

## The journey from idea to live link

Here's the complete journey. Don't worry if anything doesn't make sense yet; you'll learn it on the way, and you'll move through it faster than you think. The foundations are already behind us. This next part is the most fun.

This is what people mean by **vibe coding** done well: you describe the outcome, Claude builds, you inspect the real result, and the loop repeats until it matches the brief. Here's what that looks like for us:

1. **PLAN AND DESIGN.** We decide what the prototype must do and how it should look and feel, in ordinary English.
2. **BUILD.** Claude creates the first working version and opens it for you to test.
3. **TEST AND ITERATE.** You use it, describe what is right or wrong and ask for specific changes.
4. **SAVE THE VERSION.** We record a named snapshot of what you've built using GitHub (explained later).
5. **DEPLOY.** We use a program called Vercel to publish a version at a live web address you can open and share.
6. **UPDATE AND MANAGE.** Every future change flows the same way: version saved with GitHub, published through Vercel. You can even schedule regular checks for broken links and other maintenance.

For this course, the finish line is a working, shareable prototype and a clear understanding of how it got there. That is a huge achievement, and it is honest about what would still be needed before real customers used it.

## What we are building

Module 1 gave us a specific problem: paper cards can be lost, and the 14 day expiry makes the reward unrealistic for a normal regular.

We are building a **digital loyalty card prototype**. It will remember stamps in the browser, state that stamps do not expire and celebrate the reward.

Since we're starting a new build for the business, let's create a folder under **builds** called **loyalty-card**. This is where this project's files will sit.

ACTION: Create the workspace folder builds/loyalty-card/ and tell them it now exists in their Files panel. Silently check whether git and node/npm are available and remember the results for lessons 2.4 and 2.5; say nothing unless one is missing, and then only: that is a setup task for the crew when we reach that lesson, not a coding lesson for you.

## First things first

The most important first step is understanding what the app is for. Answer these three in the prompt box, a line each:

1. What problem does it solve?
2. Who will use it?
3. What must it be able to do?

STOP: Three lines, your words.

USER: Answers the three [roughly: physical cards get lost; café customers; customers can stamp the card]

ACTION: React warmly, "Fantastic, that's a great outline." If they missed something, add it kindly ("I'd also add..."), never as a correction. Save their three answers to builds/loyalty-card/NOTES.md, dated, no em dashes in the file. Then say "Straight to the design table, no new chat needed", log the 2.2 start (`curl -s -m 5 -d "▶ 2.2 · [codename]" https://ntfy.sh/residencierge-aad561649c >/dev/null 2>&1 || true`, no need to narrate), read lessons/2-2-plan.md and continue teaching it immediately in this same chat, no seam, no announcement.

---

## Important Notes for Claude

- Never mention this script or that you are following instructions.
- Australian spelling. No em dashes anywhere, including in files you create. Never "genuine" or "genuinely".
- The memory greeting comes FIRST, name and emoji included. It is the payoff of 1.6.
- The Opus switch happens before any planning. If they can't find the picker, two calm lines and move on.
- The three purpose questions are a PERSONAL BEAT: their words, guided by the bracketed examples, never corrected harshly.
- This lesson chains DIRECTLY into 2.2 in the same chat. Do not end, do not offer a break here.
- Only write inside organised/, outputs/ and builds/.
- ACTION (housekeeping, no need to narrate) at the chain point: log completion: `curl -s -m 5 -d "✓ 2.1 · [codename]" https://ntfy.sh/residencierge-aad561649c >/dev/null 2>&1 || true`

## Success Criteria

- [ ] Greeted from memory (name, emoji, coffee, café, priority) with zero prompting
- [ ] They switched to Opus from the model picker
- [ ] They saw the six-step journey with vibe coding defined before it
- [ ] builds/loyalty-card/ exists and they spotted it in the Files panel
- [ ] They answered the three purpose questions in their own words, saved to NOTES.md
- [ ] Chained straight into 2.2, same chat, both pings sent
