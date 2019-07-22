# Code Review
All of our engineering work makes it to production by first passing through a
code review. No line of code is too small or inconsequential to bypass this part
of our product lifecycle.

## Opening a Pull Request
When opening a pull, a few things will help get quick and actionable feedback.
1. Use the PR template that is added by default
 - Reference the ticket
 - provide a test plan with relevant login info and environment
 - Use the `Status: Code Review` tag for the pull request once it is actually
   ready for review
2. Add at least two code reviewers
 - One engineer within your squad
 - One engineer from outside your squad
 - Additional folks if you want extra eyes
3. Give yourself a code review
 - Test your own test plan on the environment specified
 - Go through your diff, add some comments for the other reviewers if there is
   some noise they can "ignore"
 - If DB work, ensure its compatible across backend applications (Meteor and
   API). Changes to the API? Will this break support for iOS or Web?
4. Give it a second
 - People have other work they are probably finishing up, take the break you
   have to go give some rock solid code reviews. Earn some good will and
   bargaining chips!

## Giving a Code Review
A code review is our first line of defense when it comes to shipping high
quality software. It also ensures a ticket soars through UAT/QA and goes to
production faster. Reviewing code should be 50% of your "code related duties"
and you should feel a sense of accomplishment if you spend a whole afternoon
just reviewing pull requests.

1. Look at the ticket the work was for
 - Having an understanding of the goal of the ticket is the first step to making
   sure the work was done correctly
2. Go through the test plan in the ticket
 - Make sure it works! This is before you've even looked at any code at all
3. Review the code
 - Provide helpful comments on syntax, organization, and performance
 - We are still a small team, sometimes its ok to ask someone to answer a
   question in person instead of leaving a comment on their pull
4. If you are assigned, you need to review!
 - Please don't let 24 hours pass before completing the review
 - If you are unable for any reason to give the code review, let the person know
   as soon as possible

## How to get feedback
1. Give it a second
 - People have other work they are probably finishing up, take the break you
   have to go give some rock solid code reviews. Earn some good will and
   bargaining chips!
2. Use standup
 - Standup is the premium opportunity to tell people you will need code review.
   If your ticket is on the critical path, they should be more than happy to
   prioritize code review that day
3. Block time on calendars
 - When all else fails, put time on people's cals and complain to Cullen or your
   PM if people arent respecting it
