## Maintainers' Responsibilities

**TL;DR:** Upkeep of the project.

* Promote progress of the project towards its goals
  * Ensure the project architecture serves the project's goals
  * Coordinate with catalysts, contributors, and external parties
* Gatekeep the codebase and ensure its quality
  * Process and encourage valuable external contributions
    * Perform final review and merge good pull requests
* Publish releases

## Maintainer Guide 🧙🏼

### Processing incoming contributions 📥
Handling pull requests and other types of contributions is not the sole responsibility of Maintainers, but rather a synergy between Catalysts and Maintainers. This workflow is described in [Processing Contributions](Processing-Contributions).

### Publishing releases 🚀

<details>
<summary><strong>Checklist to copy to the release PR 📋</strong></summary>

[Example usage: Release v0.4.0](https://github.com/Significant-Gravitas/Auto-GPT/pull/4539)

```markdown
1. [ ] Prepare 🏗️
    1. [ ] Create release branch (`release-v0.x.x`)
    2. [ ] Create release pull request, with this checklist in the description
    3. [ ] Resolve conflicts with `stable`
    4. [ ] Identify doc changes needed, create tasks for this release or next, depending on severity 
    5. [ ] Test release branch
    6. [ ] Update version numbers
    7. [ ] Draft PR materials for release
        * Release notes - Github generates pretty good ones but requires drafting an alpha or pre-release so others can see them and comment
        * Discord announcement
        * Bulletin - create a pull request
        * Twitter thread 
        * Instagram post
        * Reddit post
        * Developer newsletter (@ major releases)
        * YouTube video (@ major releases)
        * Blog post (@ major releases)
    8. [ ] Update bulletin in the release branch 
    9. [ ] Create a pre-release for peer review. You need to publish it otherwise peers won't see it
2. [ ] Publish 🚀
    1. [ ] Merge release branch into `stable`
    2. [ ] Tag & publish release v0.x.x
    3. [ ] Post announcement on Discord (@Ferg)
    4. [ ] Post announcement on Twitter (@Ferg)
    5. [ ] Post announcement on Instagram (@Ferg)
    6. [ ] Post announcement on [Reddit](https://www.reddit.com/r/AutoGPT)
    7. [ ] Send developer newsletter
    8. [ ] Post video on YouTube (@ major releases)
    9. [ ] Blog post (@ major releases)
3. [ ] Post-process 🎀
    1. [ ] merge release branch into `master`
    2. [ ] close the release's milestone
    3. [ ] evaluate this release process
    4. [ ] set next release (scope + target date)
```
</details>

#### Conventions
* We [strive to] release each Thursday at 21:00 UTC – [21 May 2023](https://discord.com/channels/1092243196446249134/1097204317125091328/1109658983163244626)

#### Further instructions
- While preparing for release:
  - Any non-urgent cards milestoned for the release-in-progress which are not cleared yet should be moved to the next milestone.

- 8-24 hours before release:
  - Compile Release Notes
    - On [Releases](https://github.com/Significant-Gravitas/Auto-GPT/releases) page, `Draft New Release`
    - `Choose a tag`: (e.g.) `v0.3.1` and click `Create new tag: v0.3.1 on publish`
    - Click `Previous tag: auto` pulldown, and select the tag of the last release
        NOTE: Yes it's annoying the `auto` sometimes selects the wrong tag, so yes we have to do this!
    - Click `Generate Release Notes`
    - Use common sense to pick out user-oriented highlights
    - Combine write-up about highlights etc. and the generated release notes and create a draft release
      - If you want others to review the release, you need to publish it, so append "-pre" or "-alpha" and mark it as a pre-release
    - Update BULLETIN.md with the most important *user-oriented* highlights and changes since the last major version

  - Coordinate community testing in [*#🧪 • testing*](https://discord.com/channels/1092243196446249134/1098217450425827468):
    - Write a message inviting to test the release branch
      - Include a list of most important features to test, based on the changes since the last release
      - Highlight `@Catalyst`, `@Maintainer`, and `@Windows Tester`, `@Linux Tester`, `@MacOS Tester`, `@Docker Tester`
    - Create a thread from the message
    - In the thread, ask testers to react with ✅ or ❌, and to leave a comment if ❌


## Challenges with Maintaining

### Distribution of Time/Effort
The properties, skills, and in-depth knowledge of the project that maintainers are required to have make them prone to picking up subprojects or other tasks that take up a lot of time. This can be of great value to the project, but also takes away from the available reviewing/merging power. The organization-level challenge this presents is to strike a balance between working on internal plans and processing external contributions.

Even if we can coordinate better just working among ourselves, there are a lot of valuable pull requests out there: improvements handed to us on a silver platter. Reviewing PRs can also help us find valuable contributors or potential catalysts/maintainers.

### Moving Forwards or Upwards?
Maintainers are charged with ensuring the quality of the codebase, but also with promoting the overall progress of the project. These two are often at odds: we get many medium-quality contributions which would introduce an improvement while also incurring technical debt or diverging from conventions or standards.

As of June 2023, we are pushing hard to make progress on two different fronts: performance and architecture. Performance improvements drive us forwards, closer to our goal of building an efficacious AI Agent. Architecture improvements move us upwards: a good architecture can make it easier to build and test performance improvements, just like an airplane can more easily move through the air at high altitude.

Since we are striving for both, neither can be called more important than the other. In daily reviewing though, we have to be practical. So: **it is acceptable to merge a performance improvement which doesn't exactly follow our highest standards if its added value is significantly greater than the incurred technical debt.** This way, the net added value is still positive, and the details can be perfected in a later pull request if it's really that important.

> **Note**  
> This is not a carte blanche to merge mediocre pull requests. They should still be of reasonable quality. And in the future, if the volume of PRs decreases or our capacity to process them increases, we may raise the bar.

## Conventions

### Reactions 😀
Let's be creative:
- 👀 (looking at it) -- if someone presents an issue (e.g. a pull-request) we don't want everyone looking at it.
    So whoever is looking at it, react with 👀
- Ask for a 👍 to request acknowledgement (or react 👍 to acknowledge that you've read it)
- ✅ job done (merged, finished, etc)
- etc.

## Tooling 🛠️

### GitHub

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

### Other tooling
Here are some tools to make the life of catalysts and maintainers easier!

- [Refined GitHub](https://github.com/refined-github/refined-github) Chrome Extension to improve GitHub Web{UI/UX}

- Create a livedoc: https://pad.bitlair.nl/

- Create a diagram: https://www.figma.com/figjam/

- [list-prs-for-path.sh](https://gist.github.com/Pwuts/0dda08968e2731388461d464bda97039)  
  pwuts' Tool to List pull requests that touch/change a specified file or path

- Toran's [git-aid](https://github.com/torantulino/git-aid)  
  This repository contains a collection of AI-assisted utilities to improve your experience with GitHub. These utilities include tools for finding duplicate issues, generating responses to issues, extracting information about repositories, and assisting with reviewing pull requests.
