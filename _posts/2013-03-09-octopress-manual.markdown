---
layout: post
title: "Octopress運用マニュアル"
date: 2013-03-09 03:15
comments: true
categories: [Octopress]
---

Ruby+Octopressの環境を整えたので、記事の追加とデプロイまでをまとめておく。  

### 環境構築

詳しい設定については以下を参照。

- [Octopressのインストールから運用管理まで](http://tokkonopapa.github.com/blog/2011/12/30/octopress-on-github-and-bitbucket/)
- [Octopressをためしてみる](http://ktsugita.github.com/blog/2013/02/17/octopress1/)
- [octopressでgithubにブログ開設](http://hnakamur.github.com/blog/2012/03/03/how-to-setup-octopress/)

### 記事を新規作成

octopressディレクトリで以下のコマンドを実行。

	rake new_post['post title']

source/_post/以下に.markdownファイルが出来るので記事を書く

### HTML生成

記事が書き終わったらHTMLを以下のコマンドで生成。

	rake generate

### 記事をリリース

以下のコマンドでリリース（入稿）

	rake deploy

HTML生成とリリースを同時にするには`rake gen_deploy`を実行。

リリースができて内容の確認ができたらgithubへpushするのを忘れないように！

以上
