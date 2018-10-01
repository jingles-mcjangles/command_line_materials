
# Git Cheat Sheet
<!-- MarkdownTOC -->

1. [Quick Reference](#quick-reference)
	1. [General Commands](#general-commands)
	1. [Reading Files \(with Less\)](#reading-files-with-less)
	1. [Getting Help with Git](#getting-help-with-git)
	1. [Starting a Repository](#starting-a-repository)
	1. [Adding Files and Committing Changes](#adding-files-and-committing-changes)
	1. [Branches](#branches)
	1. [Showing Recent Work](#showing-recent-work)
	1. [Logging and History](#logging-and-history)
	1. [See Previous Commits](#see-previous-commits)
	1. [Changing History](#changing-history)
	1. [Remotes, clouds and GitHub](#remotes-clouds-and-github)
1. [Role Playing Git](#role-playing-git)
1. [Vocabulary](#vocabulary)
1. [General commands \(for UNIX\)](#general-commands-for-unix)
1. [Git commands](#git-commands)
	1. [Help](#help)
	1. [Using the Reader \(called less\)](#using-the-reader-called-less)
	1. [Setting up your local git program](#setting-up-your-local-git-program)
	1. [Starting a Git Repository](#starting-a-git-repository)
	1. [Adding files and Committing Changes](#adding-files-and-committing-changes-1)
	1. [Seeing your History](#seeing-your-history)
	1. [Advanced History Searching](#advanced-history-searching)
	1. [Using your History](#using-your-history)
		1. [Moving through Time](#moving-through-time)
		1. [Changing History](#changing-history-1)
	1. [Making and Using Branches](#making-and-using-branches)
	1. [Syncing with GitHub](#syncing-with-github)

<!-- /MarkdownTOC -->

## Quick Reference

### General Commands

Command                | Description
---                    | ---
`man [command]`        | **Manual:**	Read manual or help file for [command]
`ls`                   | **List** files and folders in current folder/directory
`cd [directory]`       | **Change** your current **Directory** to [directory]
`pwd`                  | **Print** the directory that you are currently in (**Working Directory**)
`mkdir [name]`         | **Make** a new folder or **Directory** with name [name]
`cp [file] [copy]`     | **C**o**p**y [file] to [copy]
`mv [file] [new_name]` | **M**o**v**e [file] to [new_name]
`rm [file]`            | **R**e**m**ove [file]. PERMANENT!

### Reading Files (with Less)

Command                | Description
---                    | ---
`less [file]`          | read [file]
`h`                    | read help file (once opened Less)
`j`                    | 1 line down
`k`                    | 1 line up
`d`                    | 1/2 window down
`u`                    | 1/2 window up
`G`                    | bottom of file
`g`                    | top of file
`/[text]`              | search for text in file (hit enter to search)
`n`                    | scroll to next hit
`N`                    | scroll to previous hit


### Getting Help with Git

Command                       | Description
---                           | ---
`git help [command]`          | Read help on the git sub-command [command]
`git help -a`                 | List all available sub-commands
`git help -g`                 | List all available guides / tutorials
`git help glossary`           | Read the built in glossary


### Starting a Repository

Command                       | Description
---                           | ---
`git init`                    | Start git repository in current folder
`git status`                  | Check current status of current repository

### Adding Files and Committing Changes

Command                       | Description
---                           | ---
`git add [file]`              | start tracking the file [file]
`git add [file]`              | add changes to [file] to staging area
`git commit -a -m "mess"`     | commit all changes with message "mess"
`git commit -m "mess"`        | commit all staged changes with message "mess"

### Branches

Command                       | Description
---                           | ---
`git branch`                  | List all branches and current branch
`git branch [name]`           | Make new branch with name [name]
`git checkout [name]`         | Move to branch [name]
`git merge [name]`            | Merge branch [name] into current branch


### Showing Recent Work

Command                       | Description
---                           | ---
`git diff`                    | Shows changes made since last commit
`git diff [file]`             | Shows changes for specific file only
`git diff [SHA] [SHA]`        | Shows differences between any two commits (identified by [SHA])

### Logging and History

Command                       | Description
---                           | ---
`git log`                     | Shows a log of your commit history
`git log --oneline`           | Shows abbreviated history
`git log --stat`              | shows changed files and number of changes


### See Previous Commits

Command                       | Description
---                           | ---
`git checkout [SHA]`          | Change current version to that of commit [SHA]
`git checkout [name]`         | Return to most recent commit of branch [name]


### Changing History

Command                       | Description
---                           | ---
`git checkout HEAD -- [file]` | Discard changes to file and return to most recent commit
`git reset HEAD [file]`       | Unstage changes but keep them in the files
`git revert [SHA]`            | Undo commit [SHA] with new cancelling commit
`git reset [SHA]`             | Reset repository to commit [SHA] (--hard, --mixed, --soft)

### Remotes, clouds and GitHub

Command                       | Description
---                           | ---
`git remote -v`               | List all remotes
`git remote add [name] [URL]` | Add remote at [URL] under name [name]
`git push [name] [branch]`    | Push branch [branch] to remote [name]
`git pull [name] [branch]`    | Pull branch [branch] from remote [name]
`git push -u [name] [branch]` | Push and set remote as upstream for branch (automatically used)




## Role Playing Git

**Dwarf**
  Mines away, on their own, stashes all their treasure, doesn't use it, but is happy with all that they have achieved.

  Simply log away your history.  You never have any crisis, but you feel good and safe with your history.

  * git plugin or desktop app.
  * A few command line commands just for practice: 

> git init, git add, git commit -a -m 'text'

**Human**

  Like a dwarf, but a bit more egotistical.

  You like to show off a little more, so you put your treasure up on github for everyone to see.  

  You're also a little selfish, like dwarves, so you aren't collaborating.

  * git plugin or desktop app.
  * Use GitHub


**Elf**

  More in touch with mystical powers and can talk to the animals (??!!??).

  Cloning other repos, collaborating, and sharing your work with others.

  * git plugin or desktop app
  * May have started using the command line for some of the magical features
  * Uses GitHub a lot as part of the workflow

**Wizard**

  Contributor to open source research software with git+gitHub

  * Uses command line exclusive.
  * For some reason, is completely hopeless at using the easier to use apps
  * Uses GitHub a lot
  * Bends time and space with git


## Vocabulary

**Repository**
A log book for a captain
A Diary for all of your work
A project containing all the files

*The records and information that git keeps to track your changes and versions*

**Commit**
How you put something in your diary - a single diary entry
*Tell git to log and record the changes made since the last entry*

**Master**
	The name for the default “universe”

**Hunk**
	A location in your code where Git has detected changes

**Branch**
	Parallel Universe

**Master Branch**
	Original version

**Merge**
	Put history of one branch into another

**Origin**
	Online parallel universe

**HEAD**
 	Is a reference to the last commit in the currently checked-out branch.
 	OR, a reference to wherever you are in your history

**Working Tree / Working Directory**
	The actual files, with all the changes you’ve made, whether you have committed them or not.
	Basically, the files on your hard drive, before git did anything

**Staging Area / Index**
	Intermediate collection of files and changes prepared to all be committed together.
	Useful for excluding some changes that you don’t want to commit just yet
	Ignore for now if you like.

**Repository**
	All the versions and changes and metadata git has recorded for you




## General commands (for UNIX)

**Help or Manual**

> man [command]

**List**

> ls 

_List what is here_

**Change Directory**

> cd [directory]

_Change to specified directory_

> cd ..

_Change to the directory above.  The double dots means 'directory above'_


**Where am I**
> pwd

_Print working directory ... the directory we are in now._


**Make A New Directory**
> mkdir [new directory name]

_Make a new directory in the directory that you are currently in._


**Copy**
> cp [original file] [new file]

_Copy the original file to a file named what you specify in "new file"_
_File specifications can include whole directories too: "/my_folder/file.txt"_

**Move**
> mv [original file] [new file]

_Much like cp, but doesn't copy the file into a new one, just moves it._


**Remove or Delete**
> rm [file]
> rm -r [directory]

_Remove (or delete) a file or directory._
_This is permanent!_
_Using the "-r" flag is necessary for directories_




## Git commands

### Help

**General Help**

> git help

**Help for specific command**

> git help [command]

> git help commit

**Look up General Help**

> git help -a

*list all subcommands.  Useful for when you can't quite remember which command you want to use.*

> git help -g

*list general guides including a tutorial and suggested workflows*

> git help glossary

*Search for a term by pressing "/" then your word, and enter.  Go to each find with "n" or "N" to go backwards.  See Using the Reader (less) for more.*

### Using the Reader (called less)

The above help commands automatically use a reading app for the terminal called `less`.  To navigate and search the file you've just opened, the following commands will be helpful.


**Getting Help**

key or command | action
---            | ---
h              | read help file

**Moving around**

key or command | action
---            | ---
j              | 1 line down
k              | 1 line up
d              | 1/2 window down
u              | 1/2 window up
G              | bottom of file
g              | top of file

**Searching**

key or command | action
---            | ---
/[text]        | search for text in file (hit enter to search)
n              | scroll to next hit
N              | scroll to previous hit


### Setting up your local git program

**Configure your user name**
> git config --global user.name [My Name] 

_Lets git know who you are_
_If you ever collaborate with others, this way people can know which commits are yours._

**Configure your email**

> git config --global user.email my.email@myEmailProvider.com 

_Tell Git your email address_
_Create a config file in your home directory_


**Change default text editor**

[Quick Guide](https://help.github.com/articles/associating-text-editors-with-git/)

> git config --global core.editor "atom --wait"

**Add Aliases**

Aliases are sub-commands of your own making which run a custom, and often long, git command that you define.

Useful for making short versions of common commands, or for saving long complicated commands on speed dial for quick recall.

> git config --global alias.quick_commit "commit -a -m "whatever, get it done!"

Now, `git quick_commit` will run the above command.

*Notice the lack of a git in the quotation marks*

**Listing All Configuration Options**

> git config --global -l

**Editing Config File**

> git config --global -e

**An Alias for listing all aliases**

> git config --global alias.alias "config --global --get-regexp alias"



### Starting a Git Repository

> git init 

_Create that hidden .git directory so Git is ready to start working with your project._


> git status 

_“Hey Git, what’s up right now?”_
_Displays general information about your current repository._


### Adding files and Committing Changes
_Your Captain's Log or Diary_

**Add a File**
> git add [file] 

_Tell git to now keep records on a file so you can commit changes you've made to it._

**Commit a Change**

> git commit -m “Commit message here” 

_Whatever changes you've made (and added to the staging area), commit them with the note or message provided after the "-m" flag._


**Commit ALL Changes without adding to the Staging Area**

> git commit -a -m 'Added first verse' 

_The "-a" flag means: git-add, then do commit_
_Only works for changes to files that have previously been added.  If you want to commit changes to a new file, you have to add as above, then you can use the above._


### Seeing your History

**See the log**

> git log

_shows captain’s log activity_


> git log --oneline 

_Show the git log in a more concise form._


**Seeing Differences between changes or commits**

> git diff

_Shows differences between current uncommitted changes and those of the most recent commit_


> git diff [path]

_Shows differences only for file specified by path_


>git diff [commit] [commit]

_Shows differences between two specified locations in your history (including branches etc)_


>git diff --word-diff


_Show differences in terms of changes words, not changed lines_


### Advanced History Searching

> git log --stat

> git log --shortstat

> git log --numstat

*numbers on what changes have been made*



> git blame [path]

*Shows only the commits that affect the file defined by path*

> git log -n x

*limit the number of commits you see from your history to x*

> git log [--after | --before] <date>

* Date:
	* 'YYYY-MM-DD HH:MM::SS +1000'
	* 'YYYY-MM-DD'
	* '7 years 5 months 3 days 2 hours ago'

*Specify a time period of your history to look at*

> git log --grep [pattern]

*pattern is in the message for the commit*

> git log -S [pattern]

*pattern has been added or deleted (in change log) in actual text*

> git log -G [pattern]

*Pattern occurs in change log in actual text*

> git log -L [start],[end]:file

*Shows commits that affected the specified line range of the specified file (with respect to present file line numbers)*

> git log --diff-filter [A,D,M, ...]

*See commits that affected files in a particular way (ie, added a file, modified, deleted, etc)*


### Using your History
_Time Travel_

#### Moving through Time

**Going back in time to a previous commit**

> git checkout [unique change id]

_Goes back to the state of your files at this commit_
_Lets you look at your files as they were at this time, and run code if you need to_


**Going back to the present**

> git checkout master

*Here, master is referring to the branch name.  If on another, you need to specify that branch*

#### Changing History

**Cancelling previous commits**

> git revert [unique change id]

_The "Unique Change ID" is what the commands "git log" give you for each commit_
_Cancels the changes made in a particular commit, and adds a new commit recording this reversal of changes_

**Undoing Work before its committed**

> git checkout HEAD -- [file]

*Any changes not committed will be discarded*


**Re-Writing History**

> git revert SHA

> git reset SHA

* soft (kind of default)
* hard
* all with possibility of specifying path


### Making and Using Branches
_Parallel Universes_

**List all Current Branches**
> git branch

**Make a new Branch**
> git branch [branch name]

**Go to a branch**
> git checkout [branch name]


**Merge the History of a branch into the current branch**
> git merge [branch name]

_Takes the history of "branch name" and merges that into the branch you are current in._
_Running "git branch" before, to confirm which branch you're in maybe helpful._
_If there are different changes in each branch that can't be merged, ie that conflict with each other, you will get a conflict that needs to be resolved._


### Syncing with GitHub
_Sharing your repositories online_

**List current Remotes**
> git remote -v

**Add your GitHub (or other) repository to your local repository**

> git remote add [name] [URL]

_Adds the URL of your online Repo to your local repo under the name you provide._
_Within Git, this is the name of the remote that you are using_


**Put your Local History onto your Online Repo**
> git push [remote name] [branch]

_Takes all of the history of the branch you specify and adds it to the remote you specify_
_This history is put into a branch of the same name as your local one, the one you specify._


**Bring changes that are on your online repo into your local Repo**
> git pull [remote name] [branch]

_Here, "branch" specifies the branch name in the GitHub account (which will generally be the same name as the one on your local computer, as it will have been created by you doing "git push" as above)_

_Will take the history of the "branch" on "remote name" and merge it into the branch you are currently in_
	

