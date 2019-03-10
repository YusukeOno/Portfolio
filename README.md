# Portfolio
Portfolioサイト。

Masterブランチにpushすることで、CircleCIにてHugoでビルドされて静的ファイルが生成します。さらに、それらのファイルをGoogle App Engine(GAE)にデプロイします。

## CircleCI

[![CircleCI](https://circleci.com/gh/YusukeOno/Portfolio/tree/master.svg?style=svg)](https://circleci.com/gh/YusukeOno/Portfolio/tree/master)

#### Note to self:

CLIで .circleci/config.yml の構文チェックができます。

`$ brew install circleci`

`$ brew update`

`$ circleci config validate -c .circleci/config.yml`

### Environment Variables for CircleCI

- GOOGLE_AUTH
- GOOGLE_PROJECT_ID
- HUGO_VERSION

## Hugo

プレビューする。

`$ hugo server`

静的ファイルをbuildする。

`$ hugo`

## GAE

GAEに反映するコマンド。

`$ gcloud app deploy app.yaml`

## TODO

### CI導入

- [x] Githubのmasterブランチにpushしたら、CircleCI側でhugoして静的コンテンツをビルドしてGAEにdeployする。
- [x] 結果をslackに通知する。
- [ ] カナリアリリースする。

### GTM導入

- [x] Google Tag Managerを導入する。
