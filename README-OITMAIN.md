Syncing a fork
===============================

https://help.github.com/articles/syncing-a-fork/

1. Add upstream to sync fork
git remote add upstream https://github.com/yiisoft/yii2-app-advanced

git fetch upstream

git checkout master

git merge upstream/master


Install and initialize Yii 2
===============================

composer global require "fxp/composer-asset-plugin v1.2.1" --no-plugins

composer update

php /path/to/yii-application/init

php /path/to/yii-application/yii migrate

Token : c8bd9e956c283747fc72adbaff9edf0df43109a7