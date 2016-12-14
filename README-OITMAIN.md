Install and initialize Yii 2
===============================

```sh
# Download Project
PROJECT_NAME=new-project-name
git clone --depth=1 --branch=master https://github.com/oitmain/yii2-app-advanced $PROJECT_NAME
cd $PROJECT_NAME
rm -rf .git

# Install Yii
composer global require "fxp/composer-asset-plugin v1.2.1" --no-plugins
composer update
php init
#php yii migrate
```

Deploy to Github
===============================
### 1. Initialize git project
```sh
git init .
git add -A
git commit -m 'Initial commit'
```
### 2. Create repository
```sh
API_TOKEN=github_token
REPO_NAME=some_repo
curl -H "Authorization: token $API_TOKEN" https://api.github.com/orgs/oitmain/repos -d '{"private":true,"name":"'"$REPO_NAME"'"}'
```
### 3. Push
```sh
REPO_NAME=some_repo
git remote add origin https://github.com/oitmain/$REPO_NAME
git push -u origin master
```

C9 Apache 2 configuration for Yii2 Advanced App
=============================== 
https://github.com/oitmain/c9-yii2-advanced-apache2-conf

Syncing the fork
===============================
https://help.github.com/articles/syncing-a-fork/

### 1. Add upstream to sync fork
```sh
git remote add upstream https://github.com/yiisoft/yii2-app-advanced
```

### 2. Fetch and merge
```sh
git fetch upstream
git checkout master
git merge upstream/master
```



