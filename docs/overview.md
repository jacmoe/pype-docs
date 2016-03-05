<!--
Title: Overview
Description: Highlevel overview of Pype
Keywords: pype, overview
-->

## Motivation
Because there is no flat-file management systems (FMS?) built on Yii.

Because database and WYSIWYG editors and user management is overkill for projects which only purpose is to render fairly static documents, like blogs, documentation and wikis.

## Design decisions
Optimize the heck of out of it: when a page has been changed and pushed to the repository, Pype processes the page and updates the database according to the *frontmatter*, grabs the contributor data (name, login name, profile url, etc.) makes a local thumbnail of the contributor's avatar, calculates breadcrumbs and even image dimensions (with and height) which is then used to process and cache the markdown.

The more can be done before the page is rendered, the better.

## Main features


## Performance
Since Pype is not using a database, and because the content it manages is generated beforehand and then cached, it is quite speedy.
(inimage:Performance source:overview/gtmetrix_mobile.png)
(clearfix:)
The performance rating is actually a bit misleading, because without the Gitter chat and the Poser button linked to Packagist, Pagespeed would give a rating of 99%!  
So, it has more to do with the theme than the actual 'engine'.

In addition to caching, care has been taken to ensure as high a rating as possible.

That means that Pype will calculate the height and width of all images, and create a thumbnail from the Github user avatar and store it locally, to point out some of the things that goes on under the hood.
