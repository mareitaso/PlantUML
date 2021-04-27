## PlantUMLとは？
PlantUMLとはJavaで動く、図をコードで書ける言語です

## PlantUMLの書き方
PlantUML
### まず準備すること
最初に
@startUML
最後に
@endUML
を書かなければなりません
```
@startUML
//処理内容
//処理内容
//処理内容
@endUML
```
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

### elseif文
elseif文を書くには以下のように書いていきます
```
if(条件)then(yesかNoなど)
:条件の場合;
elseif()then
:条件じゃない場合;
endif
```
elseはなくても大丈夫ですが、"endif"は無いとエラーになります。  
then(yes)は書かなくてもエラーは出ませんが、どちらに分岐するかわかりにくいので書いたほうがいいでしょう。

### while文
while文は以下のように書いていきます。
```
while(条件文) is()
```
### エラーが出たときは



## 詳しくは
<https://plantuml.com/ja/activity-diagram-beta>
