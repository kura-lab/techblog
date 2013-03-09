---
layout: post
title: "Markdownエディタ"
date: 2013-03-09 16:10
comments: true
categories: Markdown
---

OctopressをつかってMarkdown形式でブログがかけるようになったので、エディタについても少し調べてみた。

以下の2つのエディタの導入方法と使ってみての感想をまとめる

- [Mou](http://mouapp.com/)
- [Sublime Text 2](http://www.sublimetext.com/dev)

# Mou

Mac版のみの提供。以下のサイトよりダウンロードして起動してすぐ使える。

- [http://mouapp.com/](http://mouapp.com/)

### 感想

- 左に編集画面、右側にプレビューが表示される。個人的には左右逆の方がいい感じなのだが。
- 編集がリアルタイムに反映されて確認することができる。
- タイトルや箇条書きなどハイライトもされるのでみやすい。

# Sublime Text 2

Mac版、Win版、Linux版を提供。フリー版は開発中のものでいろいろポップアップ通知がでる。正式版は有料（$70）。

以下のサイトよりダウンロードする。（今回はMacのフリー版を試してみる）

- [http://www.sublimetext.com/dev](http://www.sublimetext.com/dev)

Markdown用のプラグインを入れるためにプラグイン環境をインストールする。

- アプリを起動
- View > Show Console

以下のコマンドで「Package Console」をインストール

	import urllib2,os;pf='Package Control.sublime-package';ipp=sublime.installed_packages_path();os.makedirs(ipp) if not os.path.exists(ipp) else None;open(os.path.join(ipp,pf),'wb').write(urllib2.urlopen('http://sublime.wbond.net/'+pf.replace(' ','%20')).read())

- 再起動して完了

Markdown編集用のプラグインをインストール

- Tools > Command Palette
- コマンドラインに`Package Control:Install Package`を入力
- 「Markdown Preview」を検索、選択してインストール

`alt + m`のショートカットでプレビューできるようにキーバインドを設定

- Sublime Text 2 > Preferences > Key Bindings - User

以下を設定

	[ { "keys": ["alt+m"], "command": "markdown_preview", "args": {"target": "browser"} }]

### 感想

- Markdown以外の言語もプラグインをいれるとつかえるようになる。  
環境づくりが少しめんどくさいが、整ってしまえばいろいろカスタマイズできるのでよい。
- プレビューはブラウザが立ち上がりファイルを保存して、リロードすると確認できる。
- フリー版でも十分利用できる。

# まとめ

MouとSublime Text2でMarkdownを編集できるところまでの準備についてまとめた。  
プレビューの方式がMouはアプリ上で、Sublime Text2はブラウザ上とことなるが、どちらも十分便利なので、好みによって選べば良い。

ちなみにこの記事はSublime Text2で書いている。

### 参考

- [Sublime Text 2ってエディタがすごくイイ。Dreamweaverから乗り換えた時の初期設定とか使い方とかをメモ](http://mnemoniqs.com/web/sublimetext2/)
- [SublimeText2でMarkdownをプレビューするプラグイン](http://codedehitokoto.blogspot.jp/2012/04/sublimetext2markdown.html)

以上