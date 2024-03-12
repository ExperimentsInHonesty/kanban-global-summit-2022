![image](https://user-images.githubusercontent.com/37763229/184605261-3e87d1df-9a7b-4d99-a7a2-1a91636d831c.png)


### Description
Checks the in-progress column from the project board. Goes through each issue, and if there is an assignee, checks the timeline for the issue. If it is outdated, posts a comment to update the issue and ensures the label is changed to 'to update.' Else, change the label so it is 'updated'

### Location of message in the repo
https://github.com/hackforla/website/blob/gh-pages/github-actions/trigger-schedule/add-update-label-weekly/update-instructions-template.md ([permalink](https://github.com/hackforla/website/blob/85a08700e88739cb387684465c857fedb935d421/github-actions/trigger-schedule/add-update-label-weekly/update-instructions-template.md))


### Technical Workflow
https://github.com/hackforla/website/blob/gh-pages/.github/workflows/schedule-fri-0700.yml ([permalink](https://github.com/hackforla/website/blob/85a08700e88739cb387684465c857fedb935d421/.github/workflows/schedule-fri-0700.yml), formerly `add-update-label-weekly.yml`)

### Text used in the message
```
${assignees}

Please add update using the below template (even if you have a pull request). Afterwards, remove the 'To Update !' label and add the 'Status: Updated' label.

Progress: "What is the current status of your project? What have you completed and what is left to do?"
Blockers: "Difficulties or errors encountered."
Availability: "How much time will you have this week to work on this issue?"
ETA: "When do you expect this issue to be completed?"
Pictures (optional): "Add any pictures of the visual changes made to the site so far."
If you need help, be sure to either: 1) place your issue in the developer meeting discussion column and ask for help at your next meeting, 2) put a "Status: Help Wanted" label on your issue and pull request, or 3) put up a request for assistance on the #hfla-site channel.

You are receiving this comment because your last comment was before ${cutoffTime} PST.
```
---
- Content sourced from https://github.com/hackforla/website/wiki/GHA:-add-update-label-weekly
- License at the source: https://github.com/hackforla/website/blob/gh-pages/LICENSE.txt
