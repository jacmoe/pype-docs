<!--
Title: Installation
Description: How to install Pype
Keywords: pype, install
-->
## Configure
First, you need to generate the initial configuration by running the following command in a console:

```bash
dep local-config local
```

You can ignore the warning because the script will not find any file to overwrite since it is the first time.

The script generates `web.php` and `console.php` files in the `config` directory, the `index.php` and `deploy.php` script in `web` and `Gulpfile.js` and `yii` at the project root, using the values that you previously entered into your `servers.yml` configuration file.

## Deploy
Now, that we have generated the necessary code, we are ready to deploy:

```bash
dep deploy production
```

(lightbox:Deploy source:install/deploy_mobile.png target:install/deploy.png)
(clearfix:)
