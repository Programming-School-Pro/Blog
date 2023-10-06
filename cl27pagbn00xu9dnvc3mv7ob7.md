---
title: "Useful Git Commands"
datePublished: Wed Apr 20 2022 14:59:12 GMT+0000 (Coordinated Universal Time)
cuid: cl27pagbn00xu9dnvc3mv7ob7
slug: useful-git-commands
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1650465226428/Y_-BYEuML.png
tags: github, git, command-line, 2articles1week, programming-school

---

# Git

Git is a free and open-source distributed version control system that's responsible for everything GitHub related that happens locally on your system. 


# GitHub


GitHub is a web-based platform where you can share your work with other developers and showcase your learnings.

# Git Commands:

-> think of it as a Marriage(our git repository)->guests(working files)->photoshoots on stage->(commiting your repository)

**git config**

-> Configures user information used across all local repositories.
set a name that is identifiable for credit when review version history
-> git config --global user.name "username"

set an email address that will be associated with each history marker.
-> git config --global user.email "email"

**git init**

Initializes an existing directory as Git repository (.git directory).
-> git init

**git clone**

-> git clone [url]
retrieve an entire repository from a hosted location via URL.
-> git clone --branch[url]

**git add**

add a file to your next commit(stage).
-> git add [file]

**git rm**

Deletes the file from project and stages the removal for commit. -> git rm [file]

**git mv**


Changes an existing file path and stages the move.
-> git mv [existing-path][new-path]

**git commit**


Commits the staged contents as a new commit snapshot.
-> git commit -m "your commit message goes here"

**git branch**


List, Create or, Delete Branches(branches looks like a acyclic graph)
List branches
-> git branch
Create a new Branch at the current commit
-> git branch [branch-name]
Delete a Branch
-> git branch -d[branch-name]

**git status**


Shows the paths of modified files in working directory.
-> git status

**git diff**


Show changes between commits.
to see diff of what is changed, but not staged
-> git diff
to see diff of what is staged, but not commited
-> git diff --staged
to see diff between 2 branches
-> git diff BranchA...BranchB

**git log**


Shows the commit history for the currently active branch.
-> git log
Shows the commits on branch-A that are not on branch-B.
-> git log branchA..branchB

**git checkout**


Switch Branches.
Switch to another branch and, check it out into your working directory .
-> git checkout [branch-name]

Switch to another branch(create if does not exist)
-> git checkout -b [branch-name]

**git merge**


For joining two or more development histories together.
-> git merge [branch]

**git fetch**


Fetch branches and/or tags from one or more other repositories.
-> git fetch [alias]
you can use git fetch to know the changes done in the remote rep/branch since your last pull.

**git pull**


Fetch and merge any commits from tracking remote branch.
-> git pull

**git push**


For making changes in your repository
-> git push origin [branch-name]

Transmit local branch commits to the remote repository branch.
-> git push [alias]

**git rebase**


Applies any commits of current branch ahead of specified one.
It is used if you need to rewrite the history of a project.
-> git rebase [branch-name]

**git revert**


Reverts some existing commits.
-> git revert

**git reset**


If you want to delete the commits.
-> git reset [hashcodeId]
you can get "haschodeId" by running git log
(NOTE: the commits deleted will be in unstaged area)

Resets current HEAD to the specified state.
Unstages a file while retaining the changes in working directory.
-> git reset [file]
(NOTE: the commits deleted will be in unstaged area)

Clears staging area , rewrite working tree from specified commit.
-> git reset --hard[commit]

**git stash**


Temporarily stores modified, tracked files in order to change branches.
it's used when you don't want to commit your working files but want to store
temopararily.

Save modified and staged changes
-> git stash

List StackOrder of stashed file changes
-> git stash list

write working from top of stash stack or to bring your temporarily stored files.
-> git stash pop

Discard the changes from top
-> git stash drop

For deleting temporary stored, modified, tracked files.
-> git stash clear

**git remote**


For adding the URL of your repository to your project
-> git remote add origin [URL]
remote means you're working with URLs and origin is the name of the url.

Shows all the URLs attached with your project
-> git remote -v

# Things to keep in mind while working on other developer's open-source projects.

Always make a separate branch when you working with a new feature or fixing a bug in someone's else repository.
-> git branch [branch-name]

HEAD : It's just a pointer that means all the commits that you've made will be
added on the head(the new branch).

To check when someone else commits to main branch.
-> git checkout main

For merging your code with the main code .
-> git merge [branch-name]

for copying existing organization project
-> use fork for that
clone that project in your repository.
-> git clone [URL] (paste the URL of the forked project)

upstream URL -> it is the URL from where you've forked the project .
-> git remote add upstream [URL]

To make changes in the upstream (original project)
make a new branch
-> git branch [new-branch]
-> git checkout [new-branch] (this will change the header to new-branch)

For making changes in the original project of the organization we use
pull request.

NOTE: 1 Branch -> 1 pull request
we always make a new branch to make it easier to review our commit to the
original project.

To force push the changes
-> git push origin [branch-name] -f

To make changes that you've previously made in the original project to be shown in
your forked project too
-> git checkout main
-> git fetch -all --prune (prune means the deleted commits will also be fetched)

To reset the main branch of my origin to main branch of upstream
-> git reset --hard upstream/main
-> git push origin main

> NOTE: that's how you keep in sync with the main branch or you can directly fetch upstream in your GitHub. https://sonalirajput.hashnode.dev/usefull-git-commands