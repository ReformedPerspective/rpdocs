# RP "Staging" Website

The staging website, found at staging.reformedperspective.ca is protected by a password using the .htacccess file. This site is the testing/staging site, mainly for changes to the PHP code for the main website. Changes made here are 'pushed' to GitHub and then 'pulled' to the main site.

## Staging Workflow

Here is the workflow for working on the PHP code of the rp.ca website:

1. ssh into the rp.ca Dreamhost server.
2. Make changes to the code files inside the *benchpress* folder inside the `staging.reformedperspective.ca` folder.
3. `commit` the changes and `push` them to GitHub
4. When the changes are ready to go live, go to the `reformedperspective.ca` folder on the server and `pull` the changes from GitHub.

It's important to note that only the *benchpress* folder is tracked by git. Everything else, with only a few exceptions, is excluded by the `.gitignore` file for the git repository. Things like images, plugins, Wordpress files, and especially the MySQL database are not synched between the staging and main sites and will need to be synched in another way.
