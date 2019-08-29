# 🌱 THE LIFECYCLE 🌿 OF A TICKET 🌳 #
## or, HOW WE GET CODE MERGED TO PRODUCTION ##

### What to work on
#### Tickets 📝
We decide on what we'll work on each sprint in planner. Any work you do will be described in a ticket in Jira.

### How to work on them
#### On Deck 🔜
When something is on deck, it means no one has started working on it yet. Tickets are generally listed in order
of priority, so the top ticket in an epic is probably the next one you'll want to do.

Read the ticket! If it's unclear or something's missing, ask your PM. It might be marked as `blocked` if we know
there's something blocking it.

#### In progress
##### Points  1️⃣ 2️⃣ 3️⃣
When you move a ticket to `in progress`, you'll have to point it. Give it a 1 (simple, quick), 2 (involved but
not very complex) or a 3 (very complex, but can still be one ticket).

##### Your branch 🌾
Generally you'll want to create your branch off of staging. Get the latest from staging, then checkout your own
branch and have it start with your ticket number then a word or two about the ticket, i.e. `GROW-100-submit-application`.

##### Your work 💻
Code the ticket. Woo! Before you have anyone else review it, make sure you fulfill the ticket acceptance criteria.

### How to get your work reviewed
NOTE: Sometimes it makes sense to get a ticket code reviewed before it's UAT'd, but sometimes it makes sense
for UAT to come first. Use your judgment!

#### Create a PR [pull request] 📄
Instructions for this are (here)[https://github.com/the-wing/team-procs/blob/master/Eng/CodeReview.md].

#### In review 🔎
In review means you have assigned 2 engineer reviewers. More on this
(here)[https://github.com/the-wing/team-procs/blob/master/Eng/CodeReview.md], again.

#### UAT (user acceptance testing) 🚦
First, make sure your code is somewhere that it can be reviewed.

- For members-portal code, you can just use the generated Netlify link that is created on a PR.
- For api or meteor code, you will have to deploy the code to a preview environment. Ask a non-iOS engineer if you need help with this.
- For iOS code, you need an Alpha build through AppCenter. Ask an iOS engineer if you need help with this.

We UAT because the ticket needs to be tested by a non-engineer. This is most likely a product manager or a product designer,
but sometimes you'll have to use your best judgment on who should UAT a ticket.
If a ticket is rejected from UAT the tester will put it back to in review and let you know why it was rejected.

#### Approved ✅
NICE! This means 2 engineers and 1 product manager or product designer or non-engineer has approved your ticket!

### How to get them into production
#### Merged 💯
This ticket has been merged to staging. It will wait here until we do a release.

#### Done 🎉
This ticket has been deployed to production in a release. You did it!
