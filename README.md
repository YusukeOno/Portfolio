# Portfolio
Portfolioサイト。

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

- [ ] Githubのmasterブランチにpushしたら、CI側でhugoしてGAEにdeployする。
- [ ] 結果をslackに通知する。

### GTM導入

- [x] Google Tag Managerを導入する。
