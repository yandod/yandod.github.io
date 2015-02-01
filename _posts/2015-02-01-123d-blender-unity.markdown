---
layout: post
title:  "友人をスマホで撮影して3Dモデル化してUnityで動かしてみた"
date:   2015-02-01 12:00:00 +9:00
categories: blog
---

![ito](/images/itosan_blend.png)

Unityなどでゲーム作りをする上で欠かせないのが3Dモデル。

プログラマだと自分自身でモデルデータを作る事ができず、アセットストア上のモデルやユニティちゃん、MMDのモデルデータの流用などいろいろと苦心しているのではないでしょうか。
絵心を欠いている自分としては、なんとか写真などからモデルを作る方法を練習しており、今回、一応動くようになったので紹介します。

# Autodesk 123D Catchで撮影

まず、撮影はAutodeskが出している123D Catchという無料のアプリを使います。こちらはiOSとAndroidに対応しています。またPC版とWeb版も存在しているのでスマホではなく一眼などを使って高品質な撮影を行えばモデルの精度をさらに高めることもできます。

- [Autodesk 123D Catch | 3d model from photos](http://cdn.123dapp.com/wp/wp-content/uploads/2014/09/catch-for-android.jpg)

<iframe src="https://www.youtube.com/embed/OxsmnDKO7D0" frameborder="0" allowfullscreen style="width:100%; min-height:315px"></iframe>

上記のビデオにもありますが、基本的には周囲をぐるぐると回りながら20枚前後の写真を撮影、123Dのサイトにアップロードすることでモデルデータ化されます。

今回、友人の小島さんが撮影した友人の伊藤さんは次のようなデータになりました。iPhone5での撮影です。

![ito](/images/ito_123d.png)

- [2014-07-27-18-27-10 3D Model Made with 123D 123D Catch](http://www.123dapp.com/catch/2014-07-27-18-27-10/2583019)

なかなか綺麗な仕上がりです。背景になっていた壁や道路、カフェもモデル化されており妙な迫力があります。そしてモデルデータは<code>.obj</code>形式か<code>.3dp</code>形式でダウンロードできます。このままでも一応、Unityへ持っていく事が可能です。

# Blenderで背景を削除し、頂点数を削減する。

![](/images/itosan_blend2.png)

123DからダウンロードしたデータをBlenderにインポートすると、その巨大さに圧倒されます。今回の場合ですと、 **頂点数が39万、ポリゴン数が78万** ということでUnity上での実用には耐えません。また背景部分のゴミが付いているのもキャラクターとして使うのには邪魔です。

自分は今回がBlender初体験だったのですが、書籍の説明を見ながら背景部分の削除、頂点の削減を行いました。具体的には下記のような作業を行いました。

<iframe src="http://rcm-fe.amazon-adsystem.com/e/cm?lt1=_blank&bc1=000000&IS2=1&bg1=FFFFFF&fc1=000000&lc1=0000FF&t=yandod-22&o=9&p=8&l=as4&m=amazon&f=ifr&ref=ss_til&asins=4861007658" style="width:120px;height:240px;" scrolling="no" marginwidth="0" marginheight="0" frameborder="0"></iframe>


- オブジェクトを選択して、編集モードに入り、頂点選択モードに。
- 投げ縄選択ツールで不要な部分を囲んで削除(X)をひたすら繰り返す。
- モディファイアーのDecimateを使って頂点数を減らす。

不要な部分の選択と削除はやや根気が必要でしたが、頂点数の削除はスライダーでパラメータを調整しつつプレビューもできるのでとてもカンタンでした。この作業により頂点数は1500前後、ポリゴン数も3000弱に削減できました。これくらいになるとUnityへのインポートもあっというまです。

![](/images/itosan_blend3.png)

# Blenderでボーンの埋め込みを行う。

![](/images/itosan_blend4.png)

次にMecanimなどで動かすためのボーンの埋め込みです。こちらはMixiamoを使えば自動で出来るのですが、そこそこの金額がかかってきます。今日からBlenderを始めた人間には荷が重いかもしれませんが、ボーンの埋め込みを行ってみます。実際には下記のビデオを見ながら試行錯誤してみたのですが、2時間とかからず作業が完了しました。

<iframe style="width:100%; min-height:315px" src="https://www.youtube.com/embed/Z9iUm2llVPc" frameborder="0" allowfullscreen></iframe>

実際のところ、Blenderの操作や画面レイアウトなどに戸惑っていた時間の方が長かったとは思います。終わってみるとこれまでBlenderでの作業を敬遠していたのがもったいなかったなというくらいにサクっとボーンを作成できました。データは<code>.fbx</code>でエクスポートします。これでもうアセットとして配布されている人間型のモデルデータと形式上は大差ありません。

# UnityでMecanimからコントロールする。

<iframe style="width:100%; min-height:315px" src="https://www.youtube.com/embed/zihG1ibqxpE" frameborder="0" allowfullscreen></iframe>

必要な数のボーンが埋め込まれていれば後はいつもどおりです。Humanoid向けに公開されているモーションやユニティちゃんのデータの流用などが自由に行えます。

- [UnityのMecanimでキャラクターを動かす - Qiita](http://qiita.com/yando/items/601e6fd35002e77ae9c8)

まさにMecanimの威力を実感できます。AvatarがHumanoidであればコードの互換性もあるので、サンプルプロジェクトにオリジナルのモデルを登場させて動かすなんていう事もコーディング不要、1分もかからずに完了します。

<iframe style="width:100%; min-height:315px" src="https://www.youtube.com/embed/xEQgmhpPB6M" frameborder="0" allowfullscreen></iframe>

# まとめ

要点だけの紹介でしたが、Blender入門初日の自分でも実際に動作するモデルを作成できました。
アップでの使用に耐えるデータにするにはテクスチャやボーンにさらなる調整が必要かとは思います。とはいえスマホで撮影した人物がUnity上で駆けまわる様子を見た時には感動しました。
これまでBlenderなどの3Dソフトを避けてきましたが、食わず嫌いせずにやっておけばよかったと思います。とてもカンタンなのでぜひお試しください。

使うソフトが違いますが、下記の動画も参考にしました。

- [【ユニティちゃん】HGベアッガイさんが踊ってみた【3Dキャプチャ】 ‐ ニコニコ動画:GINZA](http://www.nicovideo.jp/watch/sm25110485)

またクドいようですが、下記の本は基本操作やリギングなどをカバーしていてとても役に立ちました。

<iframe src="http://rcm-fe.amazon-adsystem.com/e/cm?lt1=_blank&bc1=000000&IS2=1&bg1=FFFFFF&fc1=000000&lc1=0000FF&t=yandod-22&o=9&p=8&l=as4&m=amazon&f=ifr&ref=ss_til&asins=4861007658" style="width:120px;height:240px;" scrolling="no" marginwidth="0" marginheight="0" frameborder="0"></iframe>
