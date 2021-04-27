## PlantUMLとは？
PlantUMLとはJavaで動く、様々な図をコードで書ける言語です。  
処理内容や分岐条件には**日本語**が使えるのでわかりやすく伝えることができます。  
今回はフローチャート(公式にはアクティビティ図)を書く際の書き方です。
## PlantUMLの書き方
### まず準備すること
最初に  
@startuml  
start  
最後に  
end  
@enduml  
を書きましょう
```
@startuml
start
～～～
処理内容
～～～
end
@enduml
```
これにより始まりと終わりに、それぞれ記号が足されます。  
### 通常の処理
:と;ではさむと通常の処理を書けます
```
:処理内容;
```
### if文
if文を書くには以下のように書いていきます
```
if(条件)then(yesかNoなど)
:条件の場合;
else
:条件じゃない場合;
endif
```
elseはなくても大丈夫ですが、"endif"は無いとエラーになります。  
then(yes)は書かなくてもエラーは出ませんが、どちらに分岐するかわかりにくいので書いたほうがいいでしょう。

### else if文
elseif文を書くには以下のように書いていきます
```
if(number == 5)then(yes)
:numberが5の時の処理;
else if(number == 3)then(yes)
:numberが3の時の処理;
else if(number == 1)then(yes)
numberが1の時の処理
else(全部違う)
numberが1，3，5以外の時の処理
endif
```
elseの後に(NO)の様に分岐のYes,Noなどをいれると  
elseの時の矢印にNoなどが出できます

### while文
while文は以下のように書いていきます。
```
while(条件文) is()
:ループ内の処理;
:ループ内の処理;
endwhile
```
## エラーが出たときは
if文やwhile文の終わりにendif・endwhileは書けてますか？  
while文やif文の数に合わせてendif・endwhileも書かなければなりません。  
if文の中にwhile文やif文・while文の中にwhile文やif文を書いていくと少しわかりづらくなるので注意が必要です。  
()が全角の（）になっていませんか？  
通常処理の : ; はしっかりありますか？

## エラー出ないけど表示がおかしい
thenなどのタイプミスはありませんか？  
また () の数も確認してみましょう。

## 詳しくは
-公式
<https://plantuml.com/ja/activity-diagram-beta>

-第二弾
<https://github.com/mareitaso/PlantUML/blob/main/README2.md>
