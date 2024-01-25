# Using Git in Terminal (on MacOS X)

## Note: Git/GitHub dcoumentation and this tutorial https://guides.codepath.com/ios/Using-Git-with-Terminal#add-files-and-directories-to-gitignore were used to learn how to interface between GitHub and Terminal.

# Install Git Credential Manager

brew install --cask git-credential-manager

## Update by running:

brew upgrade --cask git-credential-manager

## The first time you perform an action that requires GitHub authorization, it will prompt a login in via a browser window. Once successfully authenticated, credentials are stored and will not need to be retyped unless credentials are changed (e.g., update password, etc.)


# Install GitHub CLI (GitHub command-line tool)

brew install gh

## Follow prompts for authentication



## Creating a Local Git Repository

## Local Git repositories are created and managed locally on your computer

## Navigate to a project folder with existing code (i.e., the local, root directory of your project)

cd [filepath]

## OR make a new directory where your project will live

mkdir [filepath]

## Assign the directory as a Git repository (i.e., Initialize the local directory as a Git repository)

git init -b main 

## By default the initial branch is main, but you can sent the name of the default branch using the flag -b

## Add the files in your new local repository

git add .

## Adds the files in the local repository and stages them for commit.

## To unstage a file, use:

git reset HEAD [YOUR-FILE]

# Create a .gitignore file

## The purpose of a .gitignore file is to tell Git which files and directories to ignore when you make a commit. Commit the .gitignore file to the repository to share the rules with others

touch .gitignore

open .gitignore

## Add files or directories that should not be commited to the GitHub repository

## For more, see: https://docs.github.com/en/get-started/getting-started-with-git/ignoring-files

## It may be useful to also create a .gitattributes file. This file allows you to specify merge strategies for individual files or directories in your project. For example, how to read and show changes to .docx (Word) files.

## To learn more about .gitattributes, see here: https://git-scm.com/book/en/v2/Customizing-Git-Git-Attributes#:~:text=Using%20attributes%2C%20you%20can%20do,into%20or%20out%20of%20Git.

# Add a README

touch README.md

open README.md


# Import a Git repository from local with GitHub CLI

## See here: https://docs.github.com/en/migrations/importing-source-code/using-the-command-line-to-import-source-code/adding-locally-hosted-code-to-github#adding-a-local-repository-to-github-using-git

gh repo create

## When prompted select "Push an exisiting local repository to GitHub" and follow additional prompts

## Prompts can be skipped by adding flags



# Adding and Committing Changes to Local Repository 

## Check file status in repository

git status

## Stage files for commit

git add [filepath] # Adds individual file

git add . # Adds all files with changes

## Commit changes to local repository

git commit -m "Note about the commit"

## Push changes to remote repository

git push

## Pull changes that have been added to the remote repository / update local repository

git pull

# Cloning a Repository using Terminal

gh clone <repository> [<directory>]

## See more details here: https://cli.github.com/manual/gh_repo_clone







