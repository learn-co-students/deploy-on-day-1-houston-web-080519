# Deploy on Day One

## Contents

|Section                            |
|-----------------------------------|
|[History](#history)                |
|[Assignment](#assignment)          |
|[Requirements](#requirements)      |
|[File Structure](#structure)       |
|[Getting Started](#getting-started)|
|[Next Steps](#next-steps)          |
|[Resources](#resources)            |
|[Issues](#issues)                  |

## History

Welcome to Flatiron! One of the first tasks we do together as a cohort is create
student info pages to help in the process of getting to know each other. You and
your peers will be filling in these pages, which will be linked together through
an index page displaying all students.

An index page looks something like [this][index]. Links from this page go to
individual profiles, which look like [this][profile]. You will be making and
deploying an index page that contains info for all of the people at your current
table.  

Your assignment is to create a student profile for someone sitting at your table. By the end of this project, every student should have a profile for themselves that was created by someone else and every student should have created a profile for someone else. It might be easiest to create the profile of the student clockwise to you. 

You'll have about an hour and a half to complete this lab. Use that time to get to know your table, get familiar with git workflows, and re-familiarizing yourself with HTML. If you feel stuck, ask any instructor for help. **Keep in mind everyone in your table will be pushing to the same repository.**  Think about using a workflow with your teammates that will minimize conflicts.

## Requirements

Please collect the following content from your assigned student for their
profile. This content doesn't have to be finalized, but you need something to
get started. They'll be using this content as the project evolves for their
resume and other profiles online.

* Name
* Github Username
* Short Bio
* Favorite Food

## Structure

The structure of this project looks something like this:

```text
├── README.md
├── css
│   ├── css style sheets
│   └── fonts
│       └── font files
├── img
│   ├── lots of images here
├── index.html
├── js
    └── javascipt files
```

### Files You Will Need to Alter

The only file you'll alter is `index.html`.

### Files You Will Need to Add

While working on this project, you will need to add the following files:

## Getting Started

### Group Logistics

* Figure out who is going to write whose profile.

* ![fork](http://ironboard-curriculum-content.s3.amazonaws.com/web-development/deploy-on-day-1/fork.png)
* Have one person at your table [fork](https://help.github.com/articles/fork-a-repo) this repo.
* Git clone the forked repo to that person's machine. Ensure that your index.html file has the same amount of ```<li></li>``` elements (surrounded by the 'begin student' and 'end student' comments) as you have persons on your team. We have provided four by default, but you should either remove these or copy/paste to reflect the correct amount of people on your team. Assign individuals to specific ```<li></li>``` elements (order matters!).
* Once the count is accurate, the person who forked the repo must git [add](http://git-scm.com/book/en/Git-Basics-Recording-Changes-to-the-Repository#Staging-Modified-Files), [commit](http://git-scm.com/book/en/Git-Basics-Recording-Changes-to-the-Repository#Committing-Your-Changes), and [push](http://git-scm.com/book/en/Git-Basics-Working-with-Remotes#Pushing-to-Your-Remotes) to your remote master.

* Next, this person should then send the link to their fork to everyone sitting at their table.

  ![clone](http://ironboard-curriculum-content.s3.amazonaws.com/web-development/deploy-on-day-1/clone.png)

* Everyone at the table should [clone][] the repo from this fork using this link. Do not clone directly from learn-co-curriculum.

### Individual Instructions

Now that you have the repo, you'll want to get into it. Remember [cd](http://linux.about.com/od/commands/a/Example-Uses-Of-The-Command-Cd.htm)? **NOTE In all the hypothetical examples, we're writing a profile for Zoe Perez.**

Take a look at `index.html` in the browser. You can do this many ways but one is by opening finder and right clicking on index.html. Then click on "Open with" then the name of your favorite browser.

#### Make a New Branch

* From the root directory, [checkout a new branch][]. This new branch's name
  should be the name of the student whose profile you're going to create.  
  * For instance, the branch would be titled `zoe-perez`.
  * Note: The `master` branch of a project is NEVER a place to do any work. `master` is considered the build and you never break the build. So make sure you are not working or committing to the `master` branch.

* If you haven't already, switch to the branch you created. To make sure you're where you need to be, type `git branch` in your terminal. It should return the name of your assigned student emphazised with an asterisk and master.
  * For instance, typing `git branch -v` in the terminal would return:

```text
  master
* zoe-perez
```

[checkout a new branch]: http://git-scm.com/book/en/Git-Branching-Basic-Branching-and-Merging#Basic-Branching

#### Add Profile

* Open up `index.html`. Use the assigned ```<li></li>``` element as a template and fill it out for your fellow classmate.

#### Stage and Commit Changes

* Once you're happy with the profile you've created and the changes you've
  made to the index page, type [git status][]. The file you've altered,
  index.html, should appear in the "Tracked Files" section and the files
  you've created should appear in the "Untracked Files" section.

* You'll want to [add][] then [commit][] these changes with a message.

* If you type `git status`, you should see "nothing to commit, working
  directory clean". If you type `git remote -v`, it should display something
  like:

|remote | URL                                                               |         |
|-------|-------------------------------------------------------------------|---------|
|origin |https://github.com/table-member's-github-name/deploy-on-day-1...git| (fetch) |
|origin |https://github.com/table-member's-github-name/deploy-on-day-1...git| (push)  |

[git status]: (http://git-scm.com/book/en/Git-Basics-Recording-Changes-to-the-Repository#Checking-the-Status-of-Your-Files)

#### Push Up Your Branch

* Now it's time to [push][] to a remote branch. This remote branch doesn't
    exist yet, you're going to create it by pushing.

  * **NOTE: Do not push to master. Do not type anything that contains the word master!**
  * You're going to push to a branch that is the same name as your local branch.
    * For instance, if we're on the branch zoe-perez, we're going to push to zoe-perez.

* To confirm this push worked you can do two things:
  * Type `git branch -a` which will show the remote branch on github.com you
    just created when you pushed.
  * You could also go to the URL of the forked repo. Notice the section that
    looks like
  
  ![branches][]
  
You should be able to click on that arrow and to see a dropdown. From this
dropdown, select the name of the branch you've been working on.

[branches]: http://ironboard-curriculum-content.s3.amazonaws.com/web-development/deploy-on-day-1/branches.png

## Next Steps

### Additional Group Logistics

Since your table is going to be deploying a single web page with all of your
tables profiles, you'll need to merge every branch that your table created
into a single branch. This branch will contain every profile from your table.
The process of merging these branches may result in merge conflicts in
`index.html` and possibly elsewhere. That's totally okay and expected!

Think about the best way to merge all the branches together. Should one person
do it? Should everyone do it in order? Should you merge into a pre-existing
branch, like `master`, or create a totally new branch? You might be wondering
what the best answer is but there isn't a "best answer", just decide on a
strategy and go for it!

### Merge Conflicts

When [merging][], [merge conflicts][] can happen. Generally they look like:

```text
> git branch
  └── master
> git merge zoe-perez
  └── Auto-merging index.html
  └── CONFLICT (content): Merge conflict in index.html
  └── Automatic merge failed; fix conflicts and then commit the result.
```

This just means that you will have to open the files where there are merge
conflicts, in this case, `index.html`, and find the part that looks like:

```text
other content here
```

Just decide which one you want to keep or if you want to keep both. Then delete
the parts you don't want and delete the `<<<<HEAD`, `======`, and `>>>>>` parts.
In the process of trying to merge two files, you may notice that chunks of html
end up in the wrong place on the page, and there is a chance you may need to
move things around to be in the proper order again.  If you'd like a visual
reference of what your index page looks like, you can also run `open index.html`
from your command line, in order to view the current state of your page in the
browser.  

Remember, if you have multiple files with merge conflicts, you'll have to repeat
this process with each file. Once you're done selecting which code to retain,
`git add` and `git commit` these changes. Now when you type `git status`, your
terminal should not display "You have unmerged paths."


Congratulations, you've completed your first assignment!

Note: From now on, most assignments will be completed in a group but submitted
individually. This means that instead of having a **table** fork an assignment,
**each student** will fork the assignment, minimizing the merge conflicts you'll
encounter in the future.

## Resources

* Git Step Resources
  * [Forking a Repo](https://help.github.com/articles/fork-a-repo)
  * [Cloning a Repo](http://git-scm.com/book/en/Git-Basics-Getting-a-Git-Repository#Cloning-an-Existing-Repository)
  * [Branching](http://git-scm.com/book/en/Git-Branching-Basic-Branching-and-Merging#Basic-Branching)
  * [Adding](http://git-scm.com/book/en/Git-Basics-Recording-Changes-to-the-Repository#Staging-Modified-Files)
  * [Committing Changes](http://git-scm.com/book/en/Git-Basics-Recording-Changes-to-the-Repository#Committing-Your-Changes)
  * [Pushing to Remote Branches](http://git-scm.com/book/en/Git-Basics-Working-with-Remotes#Pushing-to-Your-Remotes)
  * [Merging Branches](http://git-scm.com/book/en/Git-Branching-Basic-Branching-and-Merging#Basic-Merging)
  * [Submitting a Pull Request](https://help.github.com/articles/using-pull-requests#sending-the-pull-request)
* Git Workflow Resources
  * [GitHub Flow](http://scottchacon.com/2011/08/31/github-flow.html)
  * [Git Workflow](https://github.com/diaspora/diaspora/wiki/Git-Workflow)
  * [Git Rebase Workflow Explained](http://mettadore.com/analysis/a-simple-git-rebase-workflow-explained/)
  * [How GitHub uses GitHub to Build GitHub](http://zachholman.com/talk/how-github-uses-github-to-build-github)
  * [GitHub Workflow for Submitting Pull Requests](https://openshift.redhat.com/community/wiki/github-workflow-for-submitting-pull-requests)
* Deploying to GitHub Pages
  * [Documentation for how to deploy to GitHub Pages (choose "Project Site" rather than "User or Organization Site")](https://pages.github.com/)

## Issues

A common issue is not being able to authenticate with GitHub. You need to use HTTPS/SSH correctly when cloning the repository in order to be authenticated with GitHub. Checkout and follow:

* [Setting Up Git](https://help.github.com/articles/set-up-git)
* [HTTPS Cloning Errors](https://help.github.com/articles/https-cloning-errors)
* [Setting Up SSH](https://help.github.com/articles/generating-ssh-keys)

[add]: http://git-scm.com/book/en/Git-Basics-Recording-Changes-to-the-Repository#Staging-Modified-Files
[fork]: https://help.github.com/articles/fork-a-repo

[commit]: http://git-scm.com/book/en/Git-Basics-Recording-Changes-to-the-Repository#Committing-Your-Changes
[push]: http://git-scm.com/book/en/Git-Basics-Working-with-Remotes#Pushing-to-Your-Remotes
[here]: https://help.github.com/articles/adding-collaborators-to-a-personal-repository/
[clone]: http://git-scm.com/book/en/Git-Basics-Getting-a-Git-Repository#Cloning-an-Existing-Repository
[merging]: http://git-scm.com/book/en/Git-Branching-Basic-Branching-and-Merging#Basic-Merging
[merge conflict]: http://git-scm.com/book/en/Git-Branching-Basic-Branching-and-Merging#Basic-Merge-Conflicts

<p data-visibility='hidden'>View <a href='https://learn.co/lessons/deploy-on-day-1' title='Deploy on Day One'>Deploy on Day One</a> on Learn.co and start learning to code for free.</p>
