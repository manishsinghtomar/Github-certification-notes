# Github-certification-notes
A comprehensive guide to prepare for GitHub certification exams with detailed notes, study guides, and practice questions.

## Git Hidden Folder

There id a hidden folder called `.git` which tells you that our project is a git repo.

If we wanted to create a git repo in a new project we create the folder and the initalize that repo using `git init`

```
mkdir /workspaces/tmp/new-project
cd /workspaces/tmp/new-project
git init
touch Readme.md
open Readme.md
git status
git add Readme.md
# makes changes to readme.md
git commit -a -m "add readme file" 
```



## Cloning

We can clone three ways: HTTPS, SSH, Github CLI

Since we are using Github Codespaces we'll a create temporary directory in our workspace

```sh
mkdir /workspace/tmp
cd /workspace/tmp
```

### HTPPS

```md
git clone https://github.com/Pradeep-Pandey13/CheatSheets-HTML-CSS-JavaScript.git

```

## Commits

when we want to commit code we can write git commit which will open up the commit edit message in the editor of choice.

```sh
git commit
```

Set the global editor
```
git config --global core.editor emacs
```

Make a commit and commit message without opening an editor 
```sh
git commit -m "add another exclamation"
```

## Branches

## Remotes

## Stashing 

## Merging

## Add 

when we want to stage changes that will be included in the commit
we can use the . to add all possible files. 

```
git add Readme.md
git add .
```

## Reset

Reset allows you to move staged changes to be unstaged.
This is useful when you  to revert all files not to be commited

```
git add .
git reset
```

> git reset will revert a git add.

## Status 

Git status shows you what files will or will not be commited.

```
git status
```

## Gitconfig file

The gitconfig file is what stores your global configurations for git such as email, name, editor and more.

Showing the contents of our .gitconfig file
```
git config --list
```

When you first install Git on a machine you are suppose to set up your name and email

```sh
git config --global user.name "John Doe"
git config --global user.email johndoe@example.com
```

## Log

git log will show recent git commits to the git tree

## Push

When we want to push a repo to our remote origin

```
git push


```