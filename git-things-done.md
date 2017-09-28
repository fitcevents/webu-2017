Git Things Done
--------------------------------
*with Anne Thomas*

"Work hard and git up early, it's the best part of the day."

#Overview
Git is a version control system for tracking code changes.

#Pros of Git
- decentralized code (unlike subversion), meaning a whole copy of the repo is stored locally
- super popular, huge community
- allows use of a feature branch workflow

#Cons of Git
- ummmm....none?
- can be intimidating for new devs to grasp the mental model
- extremely powerful (people feeling like they aren't using that power)
- a git hosting service can be an extra cost
- projects with large binary files (Editor: use Git LFS)

#Alternatives to Git
- Mercurial - uses a local repo system, similar to Git
- Subversion - uses a centralized repo, no local copy
- Perforce - commercial version control, used by larger companies like Ubisoft

#How are you using Git? Questions to ask yourself.
- how often are we deploying to production?
- do we tag code releases?
- do you have a QA team?
- how large is your dev team?
- is this an open source project?
- do we use command line or GUI?
- is this a short term project or a long term project that requires maintenance?

#Git Hosting Services
- Github
- Bitbucket
- GitLab
- Lots more!

#Options for Git workflow

##None/Basic/Central
- push and pull directly from the master branch
- used by individuals
- easiest to understand
- prone to issues cropping up / unstable master
- don't recommend this!

##Developer Branch
- Each developer has their own branch that they work on
- Use pull requests to merge into master
- Not feature specific
- Not as popular a workflow as others

##Feature Branch
- New branch created based on feature that needs to be added
- Use pull requests to merge into master
- One of the more popular workflows

##Git-flow
- uses master, develop, feature-branches, release-branches, hotfix
- branches are specifically named
- Git extensions available through command-line
- [cheatsheet](https://danielkummer.github.io/git-flow-cheatsheet/)
- it's popular because it's strict, not used as much because it's designed around the idea of releases

###Ideas behind Git-flow
- uses master and develop to record history of project
- feature branches are created off develop and merged into develop
- release branch is forked off develop - only used for fixes, docs (no new features)
- release gets merged into master and tagged (also merged back into develop)
- hotfix branches are for patch fixes and are forked/merged directly into master

##Custom
- most people had a specific workflow, but it was custom to each developer
- combination of the feature branch workflow and development branch is popular (no release branches)
- we use a master, development, feature-branch, bug-fixes and hot-fix method
- QA/design review is done directly on the feature-branch before merging into master

#Branch Management
##To rebase or not to rebase?
- rebasing is controversial
- [breakdown of pros and cons](https://git-scm.com/book/en/v2/Git-Branching-Rebasing)

##Commit Messages
- small commits - use git add -p, which allows you to stage partials
- effed up your commit message? 

##Merge Conflicts
- make sure that you aren't ignoring other branches that may have been merged development branch while you have been working on your feature
- do a git pull before any new work starts
- use a diff tool to compare
- ask your fellow dev! Sometimes a quick Slack message can avoid problems

##Labels in Github
- design and QA specific labels
- Emoji in labels - create empathy
- Make sure your labels are consistent across projects/repos
- group similar labels by colour (ie. use labels with similar colours to represent the urgency of an issue)

##Github Projects
- boards (like Trello)
- To-do lists
- Looping in QA/Design (using labels)

##Github Releases
- limit the permissions of who can actually push to Master
- user the checklist feature to give QA one last go - all feature branches have been merged together - does everything still work?

#Pull Requests
- be nice!
- commit messages MUST reference issue number (keywords: closes, fixes, close, fix)
- reference development style guides
- branch should be QA-approved before the PR
- use comments to point out specific problems

#Tools
- CLI / iTerm
- VSCode
- [GitKraken](https://www.gitkraken.com/pro)
- Tower
- [Git town](http://www.git-town.com/) - automate your branching model

#Final Thoughts
- regardless of how you manage your repos make sure you fully document these processes for on-boarding
- regularly checkin with your team

[@AlfalfaAnne](https://twitter.com/AlfalfaAnne)

