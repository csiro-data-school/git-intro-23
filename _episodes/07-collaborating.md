---
layout: episode
title: Collaborating with git repositories
teaching: 20
exercises: 25
questions:
  - How can I contribute to a shared repository?
  - How can I contribute to a public repository without write access?
objectives:
  - Understand how to share a repository collaboratively
  - Learn how to contribute a pull request.
keypoints:
  - "Sharing a repository needs good communication"
  - "Branches are _really_ necessary"
  - "Pull requests enable sensible merging of changes between branches and across repositories"
---

## Collaborating with git remotes

One of the major advantages of version control systems is the ability to collaborate, without having to email each other files, or bother about sharedrives. We'll consider two scenarios for collaboration:

- A remote repository where collaborators each have write acess
- A remote repository where you do not have write access

## A remote with write access

Remember that a git remote is simply a copy of the `.git` directory. It contains the instructions for how to recreate any state in the history that has been captured. If more than one person is contributing to a collaborative remote, there will be a shared history. That is, the copy on the remote will be a combination of the history between the collaborators.

> ## Discussion
>
> What do you think will happen if two collaborators make their own sequence of commits on `master` and try to push them to the same remote?
{: .discussion}
