# Portfolio

## Overview

Masterブランチにpushすることで、CircleCIにてHugoでビルドされて静的ファイルが生成します。さらに、それらのファイルをGoogle App Engine(GAE)にデプロイします。

## Screen Shot

![PC](https://raw.githubusercontent.com/YusukeOno/Portfolio/images-1/pc_image.png "PCサイト")
![SP](https://raw.githubusercontent.com/YusukeOno/Portfolio/images-1/sp_image.png "SPサイト")

## CircleCI

[![CircleCI](https://circleci.com/gh/YusukeOno/Portfolio/tree/master.svg?style=svg)](https://circleci.com/gh/YusukeOno/Portfolio/tree/master)

#### Note to self:

CLIで .circleci/config.ymlの構文チェックができます。

`$ brew install circleci`

`$ brew update`

`$ circleci config validate -c .circleci/config.yml`

### Environment Variables for CircleCI

- GOOGLE_AUTH
- GOOGLE_PROJECT_ID
- HUGO_VERSION

## Hugo

インストールする。

`$ brew install hugo`

プレビューする。

`$ hugo server`

submoduleのcloneし忘れた事に気がついた場合

`$ git submodule init`  
`$ git submodule update`

静的ファイルをbuildする。

`$ hugo`

## GAE

GAEに反映するコマンド。

`$ gcloud app deploy app.yaml`

## TODO

### CI/CD導入

- [x] GitHubのmasterブランチにpushしたら、CircleCI側でhugoして静的コンテンツをビルドしてGAEにdeployする。
- [x] GitHubへのpush結果をslackに通知する。

### GTM導入

- [x] Google Tag Managerを導入する。
