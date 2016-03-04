<!--
Title: Prerequisites
Description: What you need to install Pype
Keywords: pype, prerequisites
-->
PHP 5.4+, Git, ssh access to remote host.  
Node.js with Gulp and Browsersync installed globally, if using the provided Pype themes.

## Composer
Like Yii2: Composer with the Composer asset plugin globally installed.

## Deployer
[Deployer](http://deployer.org/)

## Github API token
You need to generate a Github API token.

You can do that from your Github profile settings menu:
(lightbox:Github API token source:prerequisites/githubtoken_mobile.png target:prerequisites/githubtoken.png)
(clearfix:)

## Docs repository
Create a repository on Github for your content - documents and images.

## Webhook
Add a webhook to your content repository:
(lightbox:Webhook source:prerequisites/hook_mobile.png target:prerequisites/hook.png)
(clearfix:)

## Pype template
Install Pype:
```bash
composer create-project --prefer-dist --stability=dev jacmoe/pype mypypesite
```
