<!--
Title: Pype
Description: Pype stands for Personal Yii Page Engine and serves static markdown documents from a separate Git repository
Keywords: wiki, yii, pype, markdown, static, flat-file
-->
# Pype - Personal Yii Page Engine


![Pype](/images/pype.png "Pype")

This is a minimal wrapper application for the [yii2-mdpages-module](https://github.com/jacmoe/yii2-mdpages-module) which serves static markdown documents from a separate Git repository.

The goal is to create a small, fast and versatile flat-file engine that is suitable for serving blogs, wikis and personal websites.

The application should be easy to upgrade and manage.

[Deployer](http://deployer.org/) is used for deployment, and [Flywheel](https://github.com/jamesmoss/flywheel) is used for temporary storage of processed documents.

And, last - but not least: Pype is powered by the [Yii Framework](http://www.yiiframework.com/)

----------------------------------

Wikilink : [[section|The Section]]

Wikilink syntax (title is optional) :
~~~
[[link|Title]]
~~~

Non-existing wikilink : [[I-do-not-exist]]

Feed : [RSS](/rss)

~~~
<?= "code here"; ?>
~~~

Some more code:

```php
        foreach($crumbs as $crumb) {
            $page = $repo->query()->where('url', '==', $crumb)->execute();
            $result = $page->first();
            if($result != null) {
                if($result->url == $crumbs[count($page_parts)-1]) {
                    Yii::$app->view->params['breadcrumbs'][] = array('label' => $result->title);
                } else {
                    Yii::$app->view->params['breadcrumbs'][] = array('label' => $result->title, 'url' => Url::to(array('page/view', 'id' => $result->url)));
                }
            } else {
                Yii::$app->view->params['breadcrumbs'][] = array('label' => $crumb, 'class' => 'disabled');
            }
        }
```

This project is still in the early phase.

Check out the project at Github: [github.com/jacmoe/pype](https://github.com/jacmoe/pype)
