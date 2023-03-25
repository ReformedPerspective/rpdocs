# Git

- Repositories are in the root of the home folder in a folder called 'GitRepos'
- Repos are bare repos in a folder named after the URL of the site they contain
- Site folders are the folders with the actual code files

## initial setup of a site folder

> **NOTE**: Be careful to set this all up _before_ you start working. It will save a _lot_ of trouble later.

Set up the Git Repo for a site like this:

1. Copy the .gitignore file from the reformedperspective.ca site folder to the target site folder and edit as appropriate.
1. In the actual site folder run:

```bash
git init --separate-git-dir="../GitRepos/<folder>"
```

Now you can do your initial commit. Make sure to run `git status` first and be careful to add any files you don't want to track to the .gitignore file first before doing a commit.

## working on the site files

All work on the [PHP code](php.md) is done using the [staging site](staging.md), and is pushed to GitHub and, when complete, pulled to the main site. The process is pretty straightforward:

1. Make changes to the code inside `staging.reformedperspective.ca`.
2. Use `git add ...` to stage any changes, if necessary, and `git commit -m ...` (or `git commit -am ...` in the case of committing all changes).<br>
   Try to keep all the work on a certain thing to one or two commits.
3. Push the commits to GitHub using `git push` periodically.
4. Once the project is done and approved, `cd ../reformedperspective.ca` to switch to the main site folder and run `git pull` to fast-forward the main site files to be the same as the GitHub repo.

The easiest way to work on the staging site files on your local computer is to use [VSCode](vscode.md) with the [*SFTP* extension](vscode.md#SFTP). This allows you to sync the entire staging folder to your local computer (a little time-consuming) and then edit the files there as if they were on your computer.
