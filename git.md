
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

- Some history and early warnings
- Git
- Github
- Other stuff
- Q&A

---

# Why version control

- Duh, lots of people working on the same code
- Stores your code
- Keeps history of **Who** did **What** and **When**!
- Prevents heart attacks. Developer safety net.

---

# Work is a flow of changes over time


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
2. Someone wanted git to suport a workflow for [RANDOM WORKFLOW HERE]
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
- Anyone tried deployed SVN over HTTP? PITA!

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
background-image: url(git-flows.png)

---
# patch mode

changed a file but only want to commit some parts

- git add -p

---
class: bottom, left
background-image: url(cherry.jpg)
background-size: contain
# git cherry-pick
---
# git rebase

Turn this

![](rebase-1.png)

into this

![](rebase-2.png)

---

# git merge

Similar to rebase, turns this

![](rebase-1.png)

into this

![](merge-1.png)

---
class: middle, center
# for magic call **git rebase -i**

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

## Yay free tools

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

# Third-party tools

Collaboration tools
- Mail/IRC
- Gitter/Slack

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

---

# Things you should check out

- [http://www.git-scm.com/book/en/v2](http://www.git-scm.com/book/en/v2)
---

# Free advice

- Stay away from crappy IDE integration
- Disable automatic code reformating
- There are good Git GUIs (gitk is not!)


