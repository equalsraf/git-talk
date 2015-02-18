
class: bottom, right
background-image: url(git.png)

@equalsraf

---
class: middle, center
# about.me
---
class: middle, center
# about.you
---

# Outline

- Version Control
- Git
- Github
- Other stuff
- Q&A

---

# Why version control

- Duh, lots of people working on the same code
- Stores your code: history of **Who** did **What** and **When**!
- Fine grained control of changes
  - Messed up? **revert**
  - **merge** code from different people
- Prevents heart attacks. Developer safety net.
- Back in the 80s we used ...

---
class: inverse, middle

# rule**#1** 

don't spend more time managing code than coding


---

# Work is a flow of changes (aka commits)

![](flow-1.png)

sometimes we make mistakes!

---
# Work in multiple things at the same time


![](flow-2.png)

Now imagine this with 5, 10, 20 people

---
class: middle, center, inverse

# Git

---

# git history in one slide

1. In 2005 Linus Torvalds needed a version control system for the kernel
2. Someone wanted git to support a workflow for [RANDOM WORKFLOW HERE]
3. Repeat step 2. for ~10 years

Result: git supports lots of workflows

---
class: bottom, right
background-image: url(scared.jpg)
## scary for new users
---

# Keep calm and Don't be a wuss

- git has 125 commands (or 38 depending how you count)
- **I know** 26 well
- I never use them all in the same project
- New users can survive with <12

---

# Why maintainers want git?

- disk space efficiency
- weird workflows, git over email, or carrier pidgin
- awesome tools for merge and migration
- security - commits hashed and signed, if the code is tampered
  with you can tell
- Anyone tried deploying SVN over HTTP? PITA!

---

# Why developers want git?

- there are some awesome tools around it, Github, gitstats
- **local patch management** local commits/branches
- i.e. you don't pollute the remote repo with code that is not ready
- Karma - don't commit 3k lines of code with a comment 'Does stuff'

---

# Git is not SVN

- SVN offers a subset of Git
- SVN+Quilt+(??) == Git

## Extra confusion because

- git commit != svn commit
- idem, git checkout
- git pull ...

---
# git pull is the devil

- pull = fetch + merge
- fetch is harmless, merge is not
- In projects where I am the maintainer, git-pull
  is forbidden, use rebase instead

---
class: middle, center, inverse
# git intro


---

# Terminology

**Commit**: is a change in one or more files, with a helpful message

**Branch**: A sequence of commits. Usually each .branch[branch] matches a flow of work (e.g. bugfix, or new feature)

**Remote**: Remote git .remote[server]

Convention: .branch[master] is the main development branch and .remote[origin] is the default server
where you push/fetch

---
class: middle, center

# less talk, show me the real deal!

---
background-image: url(git-flows.png)

---

# Getting started

Create a new repo

```
git init
```

Clone an existing repo

```
git clone https://github.com/equalsraf/git-talk-2015.git
```

---

# Commit changes

Add files to the index

```
git add file.js
```

see what you are doing before committing

```
git status
```

Save index as new commit

```
git commit
```

---

# Branches

Create branch fix from master

```
git branch fix master
```

Switch to branch .branch[fix]

```
git checkout master
```

---

# Push our code to a remote server

Create a new remote called .remote[origin] (git clone does this)
```
git remote add origin https://equalsraf@github.com/equalsraf/git-talk-demo
```

Push the .branch[master] branch into the remote .remote[origin]
```
git push origin master
```

By default the remote branch will show up as .remote[origin/master]


---

# git merge

Turns this

![](rebase-1.png)

into this

![](merge-1.png)

---

# git merge **can fail**

- e.g. two people write in the same file
- git will try to be smart about it
- in 1% of the cases really weird things can happen

---
# git rebase

Turn this

![](rebase-1.png)

into this

![](rebase-2.png)

the result is similar to merge, **but maybe not**


---
class: bottom, left
background-image: url(cherry.jpg)
background-size: contain
# git cherry-pick
---
# git cherry-pick

Apply **individual** commits from other branches

![](pick-1.png)

![](pick-2.png)

---
class: middle, center
# for magic call **git rebase -i**

---
class: inverse, middle
# rule#2
Don't rewrite history, for changes you already pushed into a remote public branch

---
class: bottom, left
background-image: url(revert.jpg)
# git revert

---
# git add: patch mode

Changed a file but only want to commit some parts

```
git add -p file
```

---
class: bottom, left, inverse
background-image: url(blame.png)
background-size: contain
# git blame

---
class: bottom, right, inverse
background-image: url(reflog.jpg)
background-size: contain
# git reflog

---

class: bottom, right
background-image: url(github.jpg)

---

# Why github

1. home to lots of open source projects
2. self promotion
3. find what you need and DRY

---
# Why github: Yay free tools

- Git
- Issue Tracker
- Wiki
- Code review
- Static webpages

---

# Pull requests

- In github you can't push to other repositories
- You fork other repos, and send [pull requests](https://github.com/neovim/neovim/pull/1927)

---
class: inverse, middle

# rule#3
ALWAYS create a separate branch for a new PR

---

# Third-party tool integration

Collaboration tools
- Mail/IRC
- Gitter/Slack
- Waffle.io

Automatic testing/deployment
- [Travis-ci](https://travis-ci.org/neovim/neovim) (Linux/Mac)
- [Appveyor](https://ci.appveyor.com/project/equalsraf/neovim) (Windows)
- [Coveralls.io](https://coveralls.io/r/equalsraf/chan42)
- [Scrutinizer](https://scrutinizer-ci.com/)

or code your own ...

---

# Other stuff

- there is also Bitbucket
  - less people
  - unlimited private repos (for small teams)
- github student accounts
- gitorious, gitlab
- or the competition (Mercurial)

---

# Things you should check out

- [http://www.git-scm.com/book/en/v2](http://www.git-scm.com/book/en/v2)
- [http://nvie.com/posts/a-successful-git-branching-model/](http://nvie.com/posts/a-successful-git-branching-model/)
---

# Free advice

- Stay away from crappy IDE integration
- Disable automatic code reformatting
- There are good Git GUIs (gitk is not!)
- When doing cross platform development, Google for CRLF git issues

---
class: dark, middle, right
background-image: url(guiness.jpg)

# Q&A


