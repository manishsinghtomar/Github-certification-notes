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

```sh
git clone https://github.com/Pradeep-Pandey13/CheatSheets-HTML-CSS-JavaScript.git
cd Github-Examples
```

>You'll need to generate a Personal Access Token (PAT)
https://github.com/setting/token

You will use the PAT as your password when you login

- Give it access to Contents for Commits

### SSH

```ssh
git@github.com:andrew-wc-brown/Github-Examples.git
cd GitHib-Examples
```

we will need to create our own SSH

```sh
sshe-keygen -t rsa
```

We can test our connection here:

```
ssh -T git@github.com
```

For WSL users and if you create a non default key you might need to add it

```sh
eval `ssh-agent`
ssh-agent /home/andrew/ .ssh/alt-github_id_rsa
```

### Github CLI

Install the CLI

eg. Linux (ubuntu)
```sh
(type -p wget >/dev/null || (sudo apt update && sudo apt-get install wget -y)) \
	&& sudo mkdir -p -m 755 /etc/apt/keyrings \
        && out=$(mktemp) && wget -nv -O$out https://cli.github.com/packages/githubcli-archive-keyring.gpg \
        && cat $out | sudo tee /etc/apt/keyrings/githubcli-archive-keyring.gpg > /dev/null \
	&& sudo chmod go+r /etc/apt/keyrings/githubcli-archive-keyring.gpg \
	&& echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/githubcli-archive-keyring.gpg] https://cli.github.com/packages stable main" | sudo tee /etc/apt/sources.list.d/github-cli.list > /dev/null \
	&& sudo apt update \
	&& sudo apt install gh -y
```

```
gh auth login
gh repo clone andrew-wc-brown/Github-Examples
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

List of branches

```
git branch
```

Create a new branch
```
git branch branch-name
```

Checkout the branch

```
git checkout dev
```

## Remotes

we can add remote but often you will just add remote via upsteam when adding a branch

```sh
git remote add ...
git branch -u origin new-feature
```

## Stashing 

```
git stash list
git stash
git stash save my-name
git stash apply
git stash pop
```

## Merging

```
git checkout dev
git merge main
```

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