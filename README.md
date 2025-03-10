# 概要
Pull Requestの作成方法の説明するためのリポジトリです。

# ハンズオン

## 1. ブランチを作成
ローカルPCでブランチを作成する。
```
$ git checkout <ブランチ名>

e.g. 
$ git checkout print-hello-world
```

## 2. 変更を作成
適当にファイルを編集し、変更を作成する。

例
```main.go
package main

import "fmt"

func main() {
	fmt.Println("Hello World!")
}
```

## 3. 変更をcommit
変更をcommitする。
```
$ git add .
$ git commit -m "<コミットメッセージ>"

e.g.
$ git commit -m "feat: print hello world"
```

## 4. 変更をpush
ローカルからGitHubにブランチをpushする。
```
$ git push origin print-hello-world

e.g. 
$ git push origin print-hello-world
```


この時点で、GitHub上でbranchが確認できるようになる。

![github branches](/image/github_branches.png)

https://github.com/knut1027/pull-request-challenge/branches

## 5. Pull Requestの画面にジャンプ
どちらかの方法でPull Requestの作成画面に飛ぶ。

【1. リポジトリ直下から】  
GitHubのリポジトリに飛ぶと、以下のようにPull Requestをがサジェストされる。  
[Compare & pull request] のボタンを押し、Pull Requestの作成画面に飛ぶ。

![github repository](/image/github_repository_pull_request.png)

【2. ブランチ一覧ページから】  
1.が出てこない場合はブランチの一覧画面に飛び、ブランチから直接作成する。  
自分が作成したブランチの横にある[…] > [New pull request] を押し、Pull Requestの作成画面に飛ぶ。

![github branchs](/image/github_branches_pull_request.png)

## 6. Pull Requestの作成
5.のいづれかの方法でPull Requestの作成画面に飛ぶと、以下のようなページが現れる。

必要に応じて、以下の項目を編集する。
- タイトル(①)
- 説明文(②)

![github pull request](/image/github_pull_request.png)

項目が編集できたら、[Create pull request] (③)を押し、作成を完了する。

## 7. Pull Requestのmerge
変更が問題なければ [Merge pull request] を押し、Pull Requestをデフォルトのブランチに反映させる。

![github merge](/image/github_merge.png)

# Tips

## レビューのアサインの仕方
ロジックがあってるかや他に良い書き方がないか等、誰かに変更内容を見て欲しい時はPull Requestのレビュー機能を使いましょう。

レビューアーはPull Requestの右端にある [Reviewers] から指定できます。

![github reviewers](/image/github_reviewers.png)

参考
- [Pull Request レビューをリクエストする - GitHub Docs](https://docs.github.com/ja/pull-requests/collaborating-with-pull-requests/proposing-changes-to-your-work-with-pull-requests/requesting-a-pull-request-review)
