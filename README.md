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

## リンク(タイトル無し)

リンクさせたいテキストを角括弧`[]`で囲み、リンク先のURLを丸括弧`()`で囲むことでタイトル無しのリンクを表示させることができます。


**記述例**


> \[リンク](http://)
>
> \[GitHub]\(https://github.com)

**結果**

[リンク](http://)

[GitHub](https://github.com)

## リンク(タイトル付き)

リンクさせたいテキストを角括弧`[]`で囲み、リンク先のURLとタイトルを記述し、タイトルをダブルクォーテーション`"`で囲み、最後にURLとタイトルを丸括弧`()`で囲むことでタイトル付きのリンクを表示させることができます。


**記述例**


> \[リンク](http:// "タイトル")
>
> \[GitHub]\(https://github.com "GitHub")

**結果**

[リンク](http:// "タイトル")

[GitHub](https://github.com "GitHub")
