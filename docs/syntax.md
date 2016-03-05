<!--
Title: Syntax
Description: The Pype Markdown flavour
Keywords: pype, markdown, syntax
-->
## Markdown
Pype uses Github flavoured Markdown.

If you know how to write Markdown, and used it before, then you don't have to learn a new markup language.

If you need a refresher course, see []()

### Extensions
Pype comes with a *wikilink* tag that is borrowed from WikiCreole:

```
[[link|optional title]]
```
It will link to a wiki page, relative to the root directory - `content` - so if you wanted to link to the document called *install* that lies in the *docs* folder, you would write:
```
[[docs/install]]
```
If you don't supply a title, then the Markdown parser will use the page title meta tag.


## Pypetext
In addition to regular markdown, Pype features *Pypetext* that enables you to extend the syntax.

For instance, this wiki uses this special tag for producing a Lightbox:

```
(lightbox:Console Commands source:workflow/commands_mobile.png target:workflow/commands.png)
```

Another utility tag is a clearfix tag:
```
(clearfix:)
```

Pypetext is inspired by [Kirbytext](https://getkirby.com/docs/advanced/kirbytext)

What is really cool about Pypetext is that you can add your own, bespoke tags.  
For instance, you could code an extension that automatically generates an image gallery using a collection of images in a directory, and write a Pypetext function that looked like this:
```
(autogallery:My Gallery source:somedirectory)
```

It doesn't have to be limited to writing your own functions, you can use third-party widgets, etc.  
Use your imagination.
