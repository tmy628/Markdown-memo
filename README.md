# Markdown記法 チートシート

## 見出し

文頭にハッシュ`#`と挿入すると見出しになります。  
レベルの数だけ`#`を記述します。   

**記述例**

```
# 見出し1
## 見出し2
### 見出し3
#### 見出し4
##### 見出し5
###### 見出し6
```

**結果**

# 見出し1
## 見出し2
### 見出し3
#### 見出し4
##### 見出し5
###### 見出し6

## 水平線

アスタリスク`*`、ハイフン`-`、またはアンダースコア`_`を3つ以上並べると水平線になります。

**記述例**

```
***
* * *
***************************************
---
- - -
---------------------------------------
___
_ _ _ 
_______________________________________

```

**結果**

***
* * *
***************************************
---
- - -
---------------------------------------
___
_ _ _ 
_______________________________________

## イタリック体

アスタリスク`*`1つ、またはアンダースコア`_`1つで囲むとイタリック体になります。

**記述例**

```
*イタリック体*
_イタリック体_
```

**結果**

*イタリック体*  
_イタリック体_

## 太字

アスタリスク`*`2つ、またはアンダースコア`_`2つで囲むと太字になります。

**記述例**

```
**太字**
__太字__
```

**結果**

**太字**  
__太字__

## イタリック体&太字

アスタリスク`*`3つ、またはアンダースコア`_`3つで囲むとイタリック体&太字になります。

**記述例**

```
***イタリック体&太字***
___イタリック体&太字___
```

**結果**

***イタリック体&太字***  
___イタリック体&太字___

## 打ち消し線

チルダ`~`で囲むことで打ち消し線を使うことができます。

**記述例**

```
~~打ち消し線~~
```

**結果**

~~打ち消し線~~

## 段落
行間に空行を入れることで段落になります。

**記述例**

```
段落1
(空行)
段落2
```

**結果**

段落1

段落2

## 改行
文末にスペース` `を2つ入れる、または`<br>`タグを使うと改行されます。

**記述例**

```
改行__(スペース2つ)
改行<br>
改行
```
**結果**

改行  
改行<br>
改行

## リスト（箇条書き）

文頭にアスタリスク`*`、ハイフン`-`またはプラス`+`を挿入すると箇条書きのリストになります。  
リストの上下には空行を挿入しないと正しく表示されません。  
また、`*`、`-`、`+`の後にはスペース` `が必要です。

**記述例**

```
（空行）
* リスト
+ リスト
- リスト
（空行）
```

**結果**

* リスト
+ リスト
- リスト

## リスト（番号付き）

文頭に番号`1`とピリオド`.`、スペースを` `挿入すると番号付きのリストになります。  
番号は自動的に採番されるため、すべての行を`1. リスト`と記述すると変更がしやすくなります。  
リストの上下には空行を挿入しないと正しく表示されません。  
また、`1.`の後にはスペース` `が必要です。


**記述例**

```
（空行）
1. リスト
1. リスト
1. リスト
   1. リスト
    1. リスト
       1. リスト
（空行）
```

**結果**

1. リスト
1. リスト
1. リスト
   1. リスト
    1. リスト
       1. リスト

## リスト（チェックボックス）

リスト（箇条書き）の記述の後ろに角括弧`[]`を記述するとチェックボックスになります。  
`[]`の中に`x`を入力するとチェックが入った状態のボックスになります。  
リストの上下には空行を挿入しないと正しく表示されません。  
また、`*`、`-`、`+`、`[]`の後にはスペース` `が必要です。

**記述例**

```
（空行）
* [ ] タスク1
+ [x] タスク2
- [ ] タスク3
（空行）
```

**結果**

* [ ] タスク1
+ [x] タスク2
- [ ] タスク3

## コードの表示(インライン)

バッククォート<code>`</code>で囲むとコードをインライン表示することができます。

**記述例**

>
> \`コードの表示(インライン)`

> \` puts "Hello World"`

**結果**

`コードの表示(インライン)`

` puts "Hello World"`

## コードの表示(ブロック)

バッククォート<code>`</code>3つ、またはチルダ<code>~</code>3つで囲むとコードブロックを表示することができます。  
コードブロックの上下に空行を挿入しないと正しく表示されないことがあります。

**記述例**

>
> (空行)  
> \`\`\`言語:ファイル名  
>  コードの表示(ブロック)  
> \`\`\`  
> (空行)
>
> (空行)  
> \~\~\~ruby:hello.rb  
>  puts "Hello World"  
> \~\~\~  
> (空行)

**結果**

```言語:ファイル名
 コードの表示(ブロック)
```

~~~ruby:hello.rb
 puts "Hello World"
~~~

## 引用

文頭に大なり`>`を置くことで引用になります。  
引用の上下には空行を挿入しないと正しく表示されません。  
複数行にまたがる場合、改行するたびに大なり`>`を置く必要があります。  
引用には見出し、リスト、コードブロックなどの他のMarkdown要素を含めることができます。

**記述例**

```
（空行）
> 引用
>
> # 見出し
> 
> * リスト
> + リスト
> - リスト  
>
> ~~~ruby:hello.rb
> puts "Hello World"
> ~~~
（空行）
```

**結果**

> 引用
>
> # 見出し
> 
> * リスト
> + リスト
> - リスト  
>
> ~~~ruby:hello.rb
> puts "Hello World"
> ~~~

## 多重引用

大なり`>`を2つ化されることで多重引用になります。  
引用の上下には空行を挿入しないと正しく表示されません。  
複数行にまたがる場合、改行するたびに大なり`>`を置く必要があります。

**記述例**

```
（空行）
> 引用
>
> > 多重引用
>
> 引用
（空行）
```

**結果**

> 引用
>
> > 多重引用
>
> 引用

## リンク

まず、リンクさせたいテキストを角括弧`[]`で囲みます。  
次に、リンク先のURLを丸括弧`()`で囲むとタイトル無しのリンクを表示させることができます。  
URLの後にタイトルを記述し、ダブルクォーテーション`"`で囲むとタイトル付きのリンクを表示させることもできます。  
タイトルは、リンクにマウスカーソルを合わせることで表示されます。  


**記述例**


> \[リンク](http://)
>
> \[GitHub]\(https://github.com)

**結果**

[リンク](http://)

[GitHub](https://github.com)


**記述例**


> \[リンク](http:// "タイトル")
>
> \[GitHub]\(https://github.com "GitHub")

**結果**

[リンク](http:// "タイトル")

[GitHub](https://github.com "GitHub")

## 画像埋め込み

まず、エクスクラメーションマーク`!`を挿入します。  
次に、代替テキストを記述し、角括弧`[]`で囲みます。  
最後に、画像のURLを丸括弧`()`で囲むとタイトル無しの画像を埋め込むことができます。  
URLの後にタイトルを記述しダブルクォーテーション`"`で囲むと、タイトル付きの画像を埋め込むこともできます。  
タイトルは、画像にマウスカーソルを合わせることで表示されます。

**記述例**

>
\![野球のキャッチャーのイラスト（男性）]\(https://1.bp.blogspot.com/-Pb3gcri2oVk/XexrVWSq4pI/AAAAAAABWno/w0Mo2MmqFMw0CJB-c1Q1Z78-KTlKxT5PQCNcBGAsYHQ/s1600/sports_baseball_catcher_man.png)

**結果**

![野球のキャッチャーのイラスト（男性）](https://1.bp.blogspot.com/-Pb3gcri2oVk/XexrVWSq4pI/AAAAAAABWno/w0Mo2MmqFMw0CJB-c1Q1Z78-KTlKxT5PQCNcBGAsYHQ/s1600/sports_baseball_catcher_man.png)


**記述例**

>
\![野球のキャッチャーのイラスト（男性）]\(https://1.bp.blogspot.com/-Pb3gcri2oVk/XexrVWSq4pI/AAAAAAABWno/w0Mo2MmqFMw0CJB-c1Q1Z78-KTlKxT5PQCNcBGAsYHQ/s1600/sports_baseball_catcher_man.png "野球のキャッチャーのイラスト（男性）")

**結果**

![野球のキャッチャーのイラスト（男性）](https://1.bp.blogspot.com/-Pb3gcri2oVk/XexrVWSq4pI/AAAAAAABWno/w0Mo2MmqFMw0CJB-c1Q1Z78-KTlKxT5PQCNcBGAsYHQ/s1600/sports_baseball_catcher_man.png "野球のキャッチャーのイラスト（男性）")

## テーブル

1行目で、テーブルの列の名前をバーティカルバー`|`で囲み、列の数と列の名前を設定します。  
2行目で、ハイフン`-`とコロン`:`を用いて、左揃えは`--:`、右揃えは`：--`、中央揃えは`：--:`と記述することで列の位置を設定することがきます。  
セルごとに設定することはできません。  
3行目以降でデータを`|`で囲むことで、表にデータを追加する事ができます。  
テーブルの上には空行を挿入しないと正しく表示されません。 


**記述例**

> (空行)  
> \|列1|列2|列3|  
> \|:--|:--:|--:|  
> |左揃え|中央揃え|右揃え|  
> |Left align|Center align|Right align|
>

**結果**


| 列1        |     列2      |         列3 |
| :--------- | :----------: | ----------: |
| 左揃え     |   中央揃え   |      右揃え |
| Left align | Center align | Right align |



| 列1        |     列2      |         列3 |
| :--------- | :----------: | ----------: |
| 左揃え     |   中央揃え   |      右揃え |
| Left align | Center align | Right align |


## Markdownの無効化

バックスラッシュ`\`をMarkdownの前に挿入するとMarkdownを無効化することができます。

**記述例**

> \\# h1

**結果**

\# h1

## 参考

[Markdown記法チートシート](http://qiita.com/Qiita/items/c686397e4a0f4f11683d)

[Daring Fireball: Markdown Syntax Documentation](http://daringfireball.net/projects/markdown/syntax.php)

## 使用素材

[かわいいフリー素材集 いらすとや](https://www.irasutoya.com "かわいいフリー素材集 いらすとや")
