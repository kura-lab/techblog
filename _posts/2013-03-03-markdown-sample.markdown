---
layout: post
title: "Markdown Sample"
date: 2013-03-03 21:56
comments: true
categories: [Markdown] 
---

タイトル
======================
行末にスペースを2つ入れると  
改行する。

空行を入れると段落がわかれる。

使い方
------
### コード ###

    <script type="text/javascript" src="jquery.min.js"></script>
    <script type="text/javascript">
    $(function() {
        alert($); /* 先頭に4文字のスペース、
                     もしくはタブを挿入します */
        });
    </script>

    def hoge(param, ...)

+   `param` :  
_パラメータ_ の説明

パラメータはバッククォートでくくる。

### 画像 ###
1. [example.com](http://example.com/ "example.com")
* ![octocat](http://github.com/github.png "画像")
2. [example.com][link]
- [![octocat][image]](https://github.com/)

[link]: http://example.com/ "インデックス型のリンク"
[image]: http://github.com/github.png "インデックス型の画像"

    1. [example.com](http://example.com/ "example.com")
    * ![octocat](http://github.com/github.png "画像")
    2. [example.com][link]
    - [![octocat][image]](https://github.com/)
  
    [link]: http://example.com/ "インデックス型リンク"
    [image]: http://github.com/github.png "インデックス型画像"

### 引用
> 引用です。
> 
> > スペースを挟んで `>` を重ねると、引用の中で引用ができますが、
> > GitHubの場合、1行前に空の引用が無いと、正しくマークアップされません。
