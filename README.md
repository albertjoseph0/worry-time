# Worry Time

A small web app for the "Worry Time" technique from Peter Hauri's *No More Sleepless Nights*: spend half an hour in the early evening writing each worry on its own index card, sorting the cards into a few piles, and writing a plan at the bottom of each one, so the worrying is done before bed instead of in it.

It's a single `index.html` with no build step and no server. Open it in a browser. Everything is stored in the browser's `localStorage` on your device; nothing is sent anywhere.

## What's in it

| Section | What it does | From the book |
|---|---|---|
| **Tonight** | Sets your worry time and bedtime, then guides a 30-minute session through five steps: settle in, write, sort, plan, put away. | "Schedule a half hour… long before you go to bed." |
| Write | One worry per card, as many as come. | "Whatever bothersome thought comes into your head gets a separate card." |
| Sort | Cards go into piles, one at a time. A starter *Little things* pile becomes the to-do list. Hover a pile button to show its ×, which deletes the pile and sends its cards back to be sorted. You can't have more than seven piles, and the app warns you if you have nearly one pile per card. | "From three to seven is usually about right. If you have a separate category for every worry, then you haven't accomplished anything." |
| Plan | Each card gets a plan type (next step, to-do, out of my control, about a person), a ruled area to write on, and an optional *Worst possible scenario* section. | Steps 3–5 and "The Worst Possible Scenario." |
| Put away | Cards with plans go to the morning list. Cards without one wait for the next session. | "Put the cards away to look at in the morning." |
| **Morning** | Shows the plans you wrote. Mark each one *Done*, or *Didn't work*, which sends the card back for tonight along with what you tried. After two failed plans, the card suggests talking to a counselor. | "If a suggested solution doesn't work, try something else or get advice." |
| **Bedside card** | A dim, warm screen for jotting a worry at night. It doesn't show your other cards. | "Keep a card near your bed in case a new worry pops up." |
| **Is it working?** | Log how long it took you to fall asleep, then compare nights with and without worry time. | "Test scientifically whether the technique is effective for you." |

## Design notes

- **Index cards drive the visual design.** Each worry is drawn as a 3×5 card with a red header line and blue ruled lines. The worry goes above the red line and the plan is handwritten on the ruled lines below it, matching the book's instruction to write the solution "at the bottom of each card."
- **The order of the steps is enforced loosely.** The stepper lets you go back to earlier steps. You can't start planning until every card is sorted, but you can put cards away without a plan.
- **Timing comes from your schedule.** If you open the app within an hour of bedtime, it suggests the bedside card instead of a full session, since the point is to worry while you're still thinking clearly.
- **Fonts:** Young Serif for headings, Atkinson Hyperlegible for interface text (it's designed for legibility, which helps when you're tired), and Kalam for anything written on a card.
- Supports light and dark themes, works on a phone, and respects reduced-motion settings.
