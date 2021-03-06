<!--
Title: Configuration
Description: How to configure Pype
Keywords: pype, configuration
-->

```yaml
# Pype Configuration
# -------------
prod_1:
    host: hostname
    user: username
    password: password
    stage: production
    repository: https://github.com/user/repository.git
    deploy_path: /var/www
    app:
        debug: false
        stage: 'prod'

        github:
            token: secretstuff
            owner: user
            repo: repo
            branch: master

        webhook:
            secret: secrethash
            php: /usr/bin/php
            yii: /path/to/yii

dev_1:
    local: true
    host: localhost
    user: username
    password: password
    stage: local
    repository: https://github.com/user/repository.git
    deploy_path: /home/user/www
    app:
        debug: true
        stage: 'dev'

        github:
            token: secretstuff
            owner: user
            repo: repo
            branch: master

        webhook:
            secret: secrethash
            php: /usr/bin/php
            yii: /path/to/yii
```

Example of the config file in use:
```php
    'modules' => [
        'wiki' => [
            'class' => 'jacmoe\mdpages\Module',
            'repository_url' => 'https://github.com/{{app.github.owner}}/{{app.github.repo}}.git',
            'github_token' => '{{app.github.token}}',
            'github_owner' => '{{app.github.owner}}',
            'github_repo' => '{{app.github.repo}}',
            'github_branch' => '{{app.github.branch}}',
            'absolute_wikilinks' => true,
            'generate_page_toc' => true,
            'snippets' => $snippets,
        ],
    ],
```
