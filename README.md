# Portfolio
Portfolioサイト。

Masterブランチにpushすることで、CircleCIにてHugoでビルドされて静的ファイルが生成します。さらに、それらのファイルをGoogle App Engine(GAE)にデプロイします。

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
