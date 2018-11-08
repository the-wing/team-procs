# Sprint Planner [Work In Progress]

The purpose of a sprint planner at The Wing is for a team of engineers, designers, and product managers to align on what, why, and how we are working on the things we are working on. As new information emerges and our goals change, the priority of various projects, features, and bugs shift around. As new work (design or tech) is produced, the relative difficulty of other work changes as well. Our sprint planner script allows us to account for relative effort and value of the things we have in the backlog. 

Our goal is never to "complete" sprint. We never set a "story points" minumum we must hit. The purpose of the sprint planning meeting is simply to make sure the priority order of planned work still makes sense given the new state of the world. As work is completed, new work proposals are introduced and ranked based on their relative value and effort.

We use Atlassian's Jira for managing tickets. Many of the steps below are specific to this tool, but they dont need to be.

For information on how work gets introduced, please read the [Grooming](/Ceremonies/Grooming.md) document. The important thing to know is that we group proposed work into Jira's "Epics" concept. Basically, a container for related tickets. 

1. **Mark the sprint as complete from the active sprints tab**

   By marking the sprint as completed, Jira will move all "Done" tickets off the backlog. This is crucial for the next steps, as it will be easy to determine if an Epic is fully shipped and it will force us to re-prioritizeany tickets that are carried over.

2. **On the backlog, we go through completed epics and mark them as done**
   
   This allows us to celebrate the wins. Over the span of two weeks, its very easy to forget all the small (and large) things we've shipped. Starting the sprint planning sesh off this way allows us to see the facts (vs feelings) of how the last sprint went. 

3. **Take stock of next two weeks**
   
   Are there any planned vacations coming up? Any weird changes to schedule due to a doctor's appointment or a national holiday? These things should already be on your calendar but its always good to remind people before planning.

4. **Go over queued epics**
   
   In this phase of the planner, the epic writer talks about the objectives of the proposed epic. We discuss acceptance criteria, rough technical design, and any actual designs that have been finished. 

   a. Read over the epic discussing the objectives, goals, plans etc. 
   b. Have a discussion chatting about the requirements and potential implementation methods
   c. Epic auther proposes the value estimate (t-shirt size). The group agrees or pushes back.
   d. The group proposes an effort estimate (t-shirt size). The group discusses ways to cut effort. If it results in a lower value as a result of cutting scope, the value estimate is updated.
   e. Once finished, move on to next epic
   
5. **Rank the epics**

   Once all proposed epics have been estimated, we rank them in order of lowest effor to highest value:
   - S-L
   - S-M
   - M-L
   - S-S
   - M-M
   - L-L
   
   We won't ever do an epic that is lower value than its effort requires. 
   
6. **Gut Check**
   
   The PM on the squad performs their "feelings" rank. There is always a valid reason that the value of something gets bumped up because of a random deadline or customer commitment.

7. **Ticket Writing Party**

   In this phase, we split up the work of writing the tickets. The engineers likely to work on an epic go through and figure out how to break up the work into tasks that one or more engineers can work on.

