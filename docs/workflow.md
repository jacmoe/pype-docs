<!--
Title: Workflow
Description: An example of Pype in use
Keywords: pype, workflow
-->

## General workflow

When you have written a new document, it needs to be committed and pushed to the doc repository before the changes will show up in your local copy of your Pype-powered website.

In order to make it easier to manage, one way of semi-automating that process is to create a small Bash script that you can run after committing your changes.

```
#! /bin/bash
git push origin master && /path/to/local/pype/yii mdpages/pages/update
```
With that script put into the root of your docs repository, the workflow becomes:

```
git commit -a -m "Commit message"
```
followed by a call to your newly added Bash script:
```
./push_it.sh
```

## Command-line interface
```
./yii help mdpages/pages
```

(lightbox:Console Commands source:workflow/commands_mobile.png target:workflow/commands.png)
(clearfix:)

To clone the docs repository and build the pages database:
```
./yii mdpages/pages/init
```

This command checks if there are changes in the remote and if there are it will pull the changes and update the page database:
```
./yii mdpages/pages/update
```
The update command is also what is called automatically by the Github webhook.

The *rebuild* command will trigger a full rebuild of the page database, without modifying the *modified* page field:
```
./yii mdpages/pages/rebuild
```
The *rebuild* command does not check for remote changes nor does it pull anything.

If you want to delete both the content repository and the page database, run this command:
```
./yii mdpages/pages/clear-all
```

Utility command to symlink the `images` directory from the *content* repository in the `web` directory:
```
./yii mdpages/pages/symlink
```
The deploy script calls that command at it's completion, because a new deployment means that the old symlink will break.
