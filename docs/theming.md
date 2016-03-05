<!--
Title: Theming
Description: How to theme your Pype
Keywords: pype, theme, theming
-->
A theme in Pype is a directory with the following structure:

    themename
      assets    ->  contains 'ThemeAsset' responsible for publishing
      dist      ->  generated files - symlinked into the web directory
        css
        js
        fonts
      js        ->  source js files
      scss      ->  source scss files - can also be Less or even css..
      views     ->  Layouts and page view files
        layouts
        page

Each theme goes into the `theme` directory at the Pype root.

It does not matter what Yii renderer you are using.  
Pype's default theme - 'Primer' - uses a Jade renderer, but you can use Smarty, Twig or even plain php.

Because the assets are symlinked into the `asset` directory in your `web` directory, they will update automatically whenever they are changed. Usually as a result of running `gulp build`.

## Details

### Asset bundle

```php
app\themes\primer\assets\ThemeAsset::register($this);
```
