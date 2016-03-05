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
To install [Deployer](http://deployer.org/) download the Deployer phar archive:

```bash
http://deployer.org/deployer.phar
```

Then install it globally:

```bash
mv deployer.phar /usr/local/bin/dep
chmod +x /usr/local/bin/dep
```

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
