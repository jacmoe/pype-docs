<!--
Title: Workflow
Description: An example of Pype in use
Keywords: pype, workflow
-->
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
