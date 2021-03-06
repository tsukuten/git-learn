# Git資料

Gitはバージョン管理システムです．

間違った変更を取り消したり，
追加する機能ごとに"ブランチ"を分けて他の

学習に適したページ

* [サルでもわかるGit入門 - 入門編](http://www.backlog.jp/git-guide/intro/intro1_1.html)

サルになりましょう．


## リポジトリ

Gitで管理してるファイルの変更履歴を保存している場所  
ローカルとリモートの二種類ある

* ローカルリポジトリ
  * 作業者のPCにある
* リモートリポジトリ
  * 外部にある　いわゆるGitHubにあるリポジトリ

## 作業の流れ

1. リモートリポジトリの状態をローカルリポジトリに取り込む(pull)
1. 自分のファイルの変更をローカルリポジトリに登録(add -> commit)
1. 自分のファイルの変更をリモートリポジトリに取り込ませる(push)

## 使うコマンド

* git pull
  * リモートリポジトリの状態をローカルリポジトリに取り込む

* git add [ファイル名]
  * commitするファイルを指定する(ステージに上げる)
  * ファイル名で"."と指定すると現在のディレクトリ以下の変更のあったファイルを自動で指定してくれるので便利(その分扱いにも注意)
* git commit -m "[コミットメッセージ]"
  * addで指定した(ステージに上った)ファイルの変更をローカルリポジトリに反映させる．
  * コミットメッセージには変更した内容を記述(〇〇を直した，〇〇機能を追加した)
* git push origin master
  * ローカルリポジトリの変更内容をリモートリポジトリに取り込ませる


## リポジトリに取り込ませたくないファイルがある

パスワードやトークンが記述されたファイルやログなど，リポジトリに取り込ませたくないファイルがある場合．

リポジトリ直下に".gitignore"というファイルを作り，そこに取り込ませたくないファイルを列挙することでそのファイルがリポジトリに登録されないようにできる．

[サンプル](https://github.com/tsukuten/git-learn/blob/master/.gitignore)
