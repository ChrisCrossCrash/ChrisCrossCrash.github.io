---
layout: page
title: Version Control (Git)
---

Git is used for version control in all projects. Here are some of the key practices followed:

- **Make Small and Focused Commits**: Commits are kept as small as possible. Even when several changes have been made before committing, each change is staged and committed individually. This approach facilitates understanding the purpose of each commit and tracking changes over time.

- **Use Main and Dev Branches for Minor Changes**: For minor changes, commits are usually made directly to the main branch or the dev branch if it serves as the main development branch.

- **Use Feature Branches for Significant Changes**: For significant or experimental changes, a new feature branch is created. This strategy ensures that unfinished features do not interfere with the deployment of minor changes, such as dependency updates or quick fixes.

- **Tag New Versions**: If a project is versioned with semantic versioning, each new version is tagged. This practice provides a clear history of changes and facilitates tracking the progress of the project.

- **Rebase Changes from a Major Branch to Feature Branches**: To incorporate changes from a major branch into a feature branch, the feature branch is rebased on top of the major branch. This keeps the commit history clean and linear.

- **Merge Changes on Feature Branches to Major Branches**: To incorporate changes from a feature branch into a major branch, the feature branch is merged into the major branch. Fast-forward merging is used when possible.

- **Avoid Committing Sensitive Information**: Care is taken not to commit sensitive information, such as API credentials, into version control. If sensitive information is accidentally committed, a tool called BFG is used to remove it. Additionally, any exposed credentials are invalidated to prevent misuse.

- **Ignore Formatting Commits**: To maintain a relevant and meaningful commit history, formatting commits are ignored using the command:
  ```
  git config blame.ignoreRevsFile .git-blame-ignore-revs
  ```
  This command ignores commits with hashes listed in the `.git-blame-ignore-revs` file at the root of the project. Here's an example of a `.git-blame-ignore-revs` file:
  ```
  # This file contains a list of commits to be ignored while using `git blame`.
  # To add this to the project's Git config, execute the following:
  # git config blame.ignoreRevsFile .git-blame-ignore-revs
  # https://git-scm.com/docs/git-blame#Documentation/git-blame.txt---ignore-revs-fileltfilegt

  a28afe1facf1591b18ead8c159b25204cfb94b39
  1de62c659ba985d639b6a7cf904693889a0dc41e
  ```
