#### 図が欲しい ####
Github pagesでブログを書くに当たり  
図を挿入するのがどうしても欲しいと思っていました。

画像を都度作るのはメンテナンスしづらいので  
文字列でUMLが書けるPlantUMLとか使えれば

#### Github pagesはプラグインで拡張できる ####
Github pagesのドキュメントを読んでいると  
Github pagesはJekyllというブログシステムが使われていて  
プラグイン機能などもあるということ

#### Github pagesでjavaは動くのか ####
Jekyllはファイルとして保存されたマークダウンテキストを  
HTML変換する仕組みです。

Githubにプッシュされた時点で  
自動でデプロイしてくれるのですが、果たしてjavaプログラム  
の実行を許可してくれるでしょうか？

javaで動くPlantUMLは動かない気がします

#### javascriptで動くmermaid ####
探してみるとPlantUMLと同じように  
テキストを図形化するプログラムに「mermaid」がありました  
https://mermaid-js.github.io/mermaid/#/

これならHTMLを表示するクライアント側で動くのでは

