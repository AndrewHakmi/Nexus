*Nobody likes meetings.* They take up time and energy, which can feel like a hassle, and for some people it is hard to sit still and pay attention for an hour or even longer. Unfortunately, running an organization without any meetings is near impossible.

This guide attempts to take away some of the pain associated with organizing and attending meetings by giving concrete guidelines to make meetings more effective.

## Organizing a meeting
Setting up a meeting consists of 4 parts:
1. The objective of the meeting
2. Choosing a date, time and place ("space-time coordinates")
3. Drafting a useful agenda
4. Communicating the invitation

Guidelines:

* If there is no clear objective, don't organize a meeting.

* An agenda should contain enough information for anyone to lead the meeting. Every non-trivial agendapoint must have a short description of the objective and the context of the agenda point. See also the [example agenda](#example-agenda).

* Smaller meetings are often more effective meetings. Make sure that the selection of invitees matches the objective of the meeting.
  * Inviting observers is generally not a problem, as long as they are aware of their role in the meeting.

Tips:
* Finding a suitable date+time can be challenging. In such cases, you can take inventory of everyones availability with [Lettucemeet] to more easily find a time slot.
* Use [Discord timestamps] to communicate timezone-agnostic date/timestamps over Discord.
* To keep meeting-related communication together, you can create a dedicated thread in a Discord channnel for which the meeting is most relevant.

## During the meeting
During the meeting, there are two major challenges:
1. Keeping the conversation on track, ensuring its time-efficiency and its effectiveness towards the meeting objective
2. Taking notes for reference at a later time and for people who couldn't attend

### Guide to chairing a meeting
A very effective effective way to streamline a meeting is to have a chair who keeps it on track. This takes practice, but knowing what to look out for makes it a lot easier to begin with.

* It must be abundantly clear who is chairing the meeting. Needless to say, you should take the lead by kicking off the meeting.

* First order of business is arranging for notes to be taken; see [Meeting notes](#meeting-notes).

* For each agenda item:
  1. announce the item;
  2. give the floor to whoever is best equipped to kick off the discussion, usually the item's speaker (submitter);
  3. observe the allocated time and the scope of the item;
  4. summarize the resulting conclusions and action points before moving on to the next item.

* For discussion items that are beyond your understanding, ask the speaker who submitted the item to observe the scope of the conversation when giving them the floor.

* When the conversation veers off course, let the "offender" finish their sentence &ndash; if not too long &ndash; and interrupt them. Point out that the ongoing conversation is out of scope / a side track / off-topic and push to move on.
  * As seductive as it can be to go into related interesting topics, try to keep this to a minimum for time's sake. Going off topic also increases the risk of losing the attention of other attendees.
  * If you are not sure whether the ongoing conversation is out of scope for the current item, you should still state this but as a suggestion or question.
  * If a side-track is important enough to discuss separately and during the meeting, park it to be discussed as Any Other Business at the end of the meeting.

### Meeting notes
To limit decay of the meeting's effects, meeting notes are essential. These notes should follow the same structure as the agenda, must include any conclusions and action points, and the considerations from which they resulted.

Tips:
  * Take down action points *including their assignees* in a dedicated section of the notes, preferably at the end of the document.
  * Note-taking can be a collaborative effort, or it can be assigned to one person who is good at it. Keep in mind that people usually can't type and speak at the same time.
  See also [Tools](#tools).

[Lettucemeet]: https://lettucemeet.com/
[Discord timestamps]: https://lettucemeet.com/

## After the meeting
* Tidy up the meeting notes and ask all attendees to check & complete the notes for items that they participated in.
* Make sure someone keeps an eye on the action points to ensure they are picked up within a reasonable period after the meeting.

## Example agenda
1. **Announcements**  
   _For logistical announcements regarding (ones attendance to) this meeting._
2. **Agenda review & confirmation**
3. **Updates** (10 min)
    1. Self-organization / Operations (pi)
    2. Team expansion (@lead-catalyst)
    3. Development
        1. State of `master` (*unassigned*)
        2. Re-arch (James)
        3. Memory (Pwuts)
        4. Contribution stats
    4. Outside interest / PR
4. **Releasing v0.4.0** (5 min, Rich)  
   Are we ready to release v0.4.0? Any remaining todo's?
5. **R&D organization** (5 min, James)  
   To tackle hard, non-trivial architecture problems and decisions, we need a solid evidence-based approach. We also need an information system for curating SotA research with a view to fast-implementing (e.g. ToT, Voyager).
   How do we set this up (rough outline), and who will take the lead?
6. **A.O.B.** - Any Other Business: points that came up after the agenda was fixed
7. **Next meeting**  
   Next thursday, 8 June at 20:00 UTC (same time)?
8. **Question round**

## Tools

**Planning**
* Lettucemeet &ndash;
  https://lettucemeet.com/
* Discord timestamp generator &ndash;
  https://r.3v.fi/discord-timestamps/

**Meeting online**
* Auto-GPT guild on Discord &ndash;
  https://discord.gg/autogpt

**Collaborative writing, note-taking/sharing**
* Notion &ndash;
  https://notion.so
* Etherpad &ndash;
  e.g. https://pad.bitlair.nl
