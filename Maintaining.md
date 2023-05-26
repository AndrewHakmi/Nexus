🧙‍♀️ Here be wizards

TODO: flesh this all out
- our review/merge process
- what else?

## Maintainers' Responsibilities

**TL;DR:** Upkeep of the project.

* Promote progress of the project towards its goals
  * Ensure the project architecture serves the project's goals
  * Coordinate with catalysts, contributors, and external parties
* Gatekeep the codebase and ensure its quality
  * Reviewing and merging pull requests
* Publish releases

## Conventions

* GitHub
  * Assign PR to a milestone if appropriate
  * `nit:` if we're reviewing someone's code, but don't want to insist they take our suggestion
* Kanban
  * Assign yourself to a card in the "In Progress" col, so people can see what you're up to.

## Discord

* Each day, `#maintainer-updates` channel:  
  * Post a message when you clock in, with your TODOs.  
  * As you work, update this message, so that when you clock out it actually shows what you did (and things still to do)
    This way we can see what everyone's up to.

### Reactions  
Let's be creative:
- 👀 (looking at it) -- if someone presents an issue (e.g. a pull-request) we don't want everyone looking at it.
    So whoever is looking at it, react with 👀
- Ask for a 👍 to request acknowledgement (or react 👍 to acknowledge that you've read it)
- ✅ job done (merged, finished, etc)
- etc.

## Organizing meetings

- create a thread at the relevant place (e.g. ⁠💬・dev-contributors-chat )
- In it Hilight e.g. @Contributor @Catalyst @Maintainer, @Catalyst @Matintainer, or just @Maintainer
    - Propose time using https://r.3v.fi/discord-timestamps/ -- invite 👍 👎 responses
    - link a livedoc https://pad.bitlair.nl/ so stakeholders can put together an agenda, so meeting starts hot
        - seed the agenda
- during the meeting, can update further the livedoc like Nick did yesterday, marking out TODOs at bottom of doc
- After the meeting, summarize actionables in thread


## GitHub

GitHub has comprehensive tooling for collaborative projects, and WE ARE USING MOST OF IT. 

- [Kanban project board](https://github.com/orgs/Significant-Gravitas/projects/1)
    This is our main nexus for scheduling, figuring out what's going on, etc. 
    - Use filters, e.g.:
        - `label:challenges` to see what's in-progress regarding Challenges
        - `milestone:"v0.4.0 Release"` to see what's outstanding regarding the upcoming v0.4.0 milestone
        - `assignee:ntindle` to marvel at the insane number of cards to which Nick has self-assigned (and maybe help him out)

    - If you're keen to involve, this is a GREAT place to get a sense of what needs doing

    - By viewing the `In Progress` column you can see who's currently doing what!

    NOTE: Cards (issues/PRs) are NOT by default added to the kanban project. So if you're wondering why a card doesn't show up on the kanban, probably this is why. If you go to the issue/PR, on the right, you should see a `Projects` that lets you choose which projects to add this card to. Just select the kanban project, and it'll show up.

    NOTE: Also TODO is add milestone to certain issues / PRs. Either make a decision yourself, or float it on Discord.


- [Milestones](https://github.com/Significant-Gravitas/Auto-GPT/milestones)
    - Click the link to see current milestones.  

    - This is DIFFERENT from the [roadmap](https://github.com/orgs/Significant-Gravitas/projects/2)

    - Catalysts/Maintainers should be adding milestones to cards (issues/PRs) as appropriate

    - We should always have a few open milestones. Suppose for example we're on 0.3.1. We should have:
        - 0.3.1 -- current version being worked on
        - 0.3.2 -- next point-release
        - 0.4.0 -- next minor-version release
        - 1.0.0 -- next MAJOR-version release

    - We can shuffle these around when we need to, e.g.: 
    At time of writing we're about to release 0.3.1, as it contains a critical bugfix.  
    We've created a 0.3.2 milestone (and re-targeted all cards that were targeting this milestone to this 0.3.2 milestone)
    
    
## Release process

NOTE (21 May 2023): [Discord link](https://discord.com/channels/1092243196446249134/1097204317125091328/1109658983163244626) We will be releasing each Thursday at 21:00z

- Any cards milestoned for this release not cleared get pushed forward to next milestone

- Compile RELEASE-NOTES
    - On [Releases](https://github.com/Significant-Gravitas/Auto-GPT/releases) page, `Draft New Release`
    - `Choose a tag`: (e.g.) `v0.3.1` and click `Create new tag: v0.3.1 on publish`
    - Click `Previous tag: auto` pulldown, and select the tag of the last release
        NOTE: Yes it's annoying the `auto` sometimes selects the wrong tag, so yes we have to do this!
    - Click `Generate Release Notes`
    - Throw these thru GPT4 to get a bulleted list
    - Use common sense to reformulate/reorganize items

- Round of testing (1h before release)
    - in #testing (in `Development` section) on the Discord:
        - Hilight @Contributor @Catalyst @Maintainer and @Windows Tester  @Linux Tester  @MacOS Tester  @Docker Tester
        - Dump RELEASE-NOTES into message
        - Create a thread from the message
        - In the thread, ask for testers to ✅ ❌, and leave a comment if ❌

- Update BULLETIN.md to announce new version

- ⭐️ Make the release, dropping in the RELEASE-NOTES, and tag master (e.g. v0.3.1)

- Announce it using the main Discord #Announcements channel (which relays to 50k+ other discord users as well as our guild)

- Tweet from official AutoGPT Twitter ([Toran](https://twitter.com/siggravitas))

- Retire old milestone (GH-PR-page (any PR))!


## Tooling
Here are some tools to make the life of catalysts and maintainers easier!

- [Refined GitHub](https://github.com/refined-github/refined-github) Chrome Extension to improve GitHub Web{UI/UX}

- Create a livedoc: https://pad.bitlair.nl/

- Create a diagram: https://www.figma.com/figjam/

- [list-prs-for-path.sh](https://gist.github.com/Pwuts/0dda08968e2731388461d464bda97039)  
  pwuts' Tool to List pull requests that touch/change a specified file or path

- Toran's [git-aid](https://github.com/torantulino/git-aid)  
  This repository contains a collection of AI-assisted utilities to improve your experience with GitHub. These utilities include tools for finding duplicate issues, generating responses to issues, extracting information about repositories, and assisting with reviewing pull requests.