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
![1](https://user-images.githubusercontent.com/32507455/117244354-d4d2f800-ae73-11eb-96bc-f2e5eaba366d.png)  
これにより始まりと終わりに、それぞれ記号が足されます。  
### 通常の処理
:と;ではさむと通常の処理を書けます
```
:処理内容;
```
![2](https://user-images.githubusercontent.com/32507455/117244706-82460b80-ae74-11eb-827c-1a75a2219555.png)
### if文
if文を書くには以下のように書いていきます
```
if(条件)then(yesの場合)
:条件の場合;
else (noの場合)
:条件じゃない場合;
endif 
```  
![3](https://user-images.githubusercontent.com/32507455/117244707-82dea200-ae74-11eb-9e79-a72e2bfaa203.png)  
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
:numberが1の時の処理;
else(全部違う)
:numberが1，3，5以外の時の処理;
endif
```
elseの後に(NO)の様に分岐のYes,Noなどをいれると  
elseの時の矢印にNoなどが出できます  
![4](https://user-images.githubusercontent.com/32507455/117244708-82dea200-ae74-11eb-896f-30cfbe129c70.png)  
### while文(前判断)
while文は以下のように書いていきます。
```
while(条件文) is (yesの場合)
:ループ内の処理1;
:ループ内の処理2;
endwhile (noの場合)
```  
![5](https://user-images.githubusercontent.com/32507455/117245902-9a1e8f00-ae76-11eb-959c-25e5095b7f57.png)  

前判断とは最初にループするか判断をしてから行われる処理のことです。
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
