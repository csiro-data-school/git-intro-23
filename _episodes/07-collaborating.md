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

To make sure that you don't end up with a mess of conflicting commits, it's essential to have an agreed strategy for how to manage your contributions.

There are different models that can work, and depending on the complexity of each situation might be appropriate.

There's a good discussion of different models, including git-flow [here](https://www.gitkraken.com/learn/git/git-flow).

To be absolutely sure your local work won't conflict with someone else's, always work on your own branch. Don't commit directly to `master`, but only merge your branch onto `master` after discussion with your collaborators, or through a pull request (discussed below).

> ## Challenge
>
> Go to https://github.com/csiro-mlai/git-practice/ and clone the repository. Create a new branch (give it a meaningful name!) on your local copy and make a change to the readme (whatever you like). Push your changes to the remote.
> Once other collaborators have pushed changes, see if you can pull their contributions to your local repo.
{: .challenge}

## A remote without write access

Lots of open source projects welcome contributions from the community, but clearly don't want to give write access to just anyone. Instead, a very commonly used approach is to accept pull requests from _forked_ versions of the repository.

### Forking a repo
Forking a repository is making your own copy of a remote. For example, the pytorch repo is hosted at `github.com/pytorch/pytorch`. By forking that repository, you can have your own copy of the complete history of the project at `github.com/[your_username]/pytorch`. To fork a repository on github, click on the Fork button at the top right of the page.

<img src="{{ site.baseurl }}/fig/github-fork.jpeg" width="60%">

### Submitting a pull request

To contribute a change to a repository that you don't have write access to, you first of all need to make your own copy (fork the repo) which you do have write access to.

You can then make your changes to the repo, and push them to your own fork.

To get them into the original repo (if that's what you want), you need to ask the maintainers of that repository to accept them, through a _pull request_.

Github has really good support for this process, and gives helpful prompts if you push a commit that is likely to be a pull request candidate.

> ## Challenge
>
> Go to https://github.com/csiro-mlai/pull-request-practice - a repo that you do not have write access to.
> 1. Fork the repo to your personal account
> 2. Clone your forked repo
> 3. Make a change in your local repo and push it to your forked copy
> 4. Submit a pull request to the original repo
{: .challenge}
