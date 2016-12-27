---
layout: post
title:  "2016年を振り返る (1アプリ 6投稿 8講演)"
date:   2016-12-27 00:00:00 +9:00
categories:
  - blog
---

早いもので2016年も間もなく終わります。
今年の自分自身のアウトプットを棚卸しするポストを書くことにしてみます。
今年はアプリの開発という長期間かつ労力の大きい活動があったため、従来と比べると活動量が少なくなりました。まぁ、アプリを作るのは大変ですねという事でしょうか。

## 初モバイルアプリリリース

<iframe frameborder="0" src="https://itch.io/embed/84727" width="552" height="167"></iframe>

初めてモバイルアプリをiOSとAndroid用にリリースしました。ちょうど2015年の年末にプロトタイプを作成し、そこから9ヶ月近く作業をしてリリースに漕ぎ着けました。
アプリをリリースするというのはわりとよくある開発者の個人活動のコミットメントだと思いますが、実際にやってみてどれだけ大変なのかを理解した気がします。

<figure>
<img src="{{ site.url }}/images/friedrice-analytics-2016.png" style="width:70%"/>
<caption>炒飯食堂のスタッツ</caption>
</figure>


リリース後も少しづつ改善を続けており、間もなく英語版への切り替え機能をリリースします。これまでの所、650人ほどの方に述べ、9800回ほど遊んで頂いたようです。英語や中国語に対応する事でプレイヤーの幅も広がるのでまずは1000人を目標にやっていくつもりです。

アプリを実際にリリースする所までやってみた上での気付きとしては

- ゲームの適切な難易度や操作性を模索するにはフィードバックを得るしかない。
- AppleとGoogleのそれぞれのプラットフォームとの繋ぎ込みに個別の知識が必要になる。
- アチーブメントやリーダーズボードの実装も結局は必要になる。
- Facebookのアナリティクスなどユーザーの動向を見るデータの重要性。
- 一度、アプリを公開するとライブラリやエンジンのアップデートは腰が重い。
- Unityのクラウドビルドはマルチプラットフォームビルドに超便利。

## ブログ投稿とQiita

<figure>
<img src="{{ site.url }}/images/blog-ga-2016.png" style="width:70%"/>
<caption>2016のアクセスログ</caption>
</figure>


ブログ記事に適したオープンソースな活動をあまりしていないので、投稿は少なかったです。この傾向は当面は変わらない気がします。もっと気軽に書ければいいんですが。
あまり更新していないわりにはアクセスは細々とあるようです。

- <a class="post-link" href="/blog/2016/10/10/line-bot/">LINEボットをPHPで作ってみた</a>
- <a class="post-link" href="/blog/2016/05/27/i-feel-fantastic/">薬物で全てをコントロールする時代の歌 I feel fantastic</a>
- <a class="post-link" href="/blog/2016/05/20/skullcrusher_mountain/">ギーク系ソング Skullcrusher Mountain</a>
- <a class="post-link" href="/blog/2016/05/20/chiron-beta-prime/">ギーク系ソング Chiron Beta Prime</a>
- <a class="post-link" href="/blog/2016/04/15/future-soon/">ギーク系ソング The Future Soon の歌詞の和訳</a>
- <a class="post-link" href="/blog/2016/03/14/philz/">打点が高いコーヒー、Philz Coffeeが気になる</a>

アクセス数の観点からいうと、以前開催したUnityの勉強会の資料をQiitaにアップしているものへのアクセス数が凄まじいです。

<figure>
<img src="{{ site.url }}/images/qiita-ga-2016.png" style="width:70%"/>
<caption>2016のqiitaアクセスログ</caption>
</figure>

上記は2016年1月1日から12月27日までのデータですが、閲覧者数で7万人強、ページビューは約18万ということでUnityを学びたい人が非常に多いことを痛感します。

<figure>
<img src="{{ site.url }}/images/qiita-gapage-2016.png" style="width:70%"/>
<caption>2016のqiitaページアクセスログ</caption>
</figure>

見る限り、Rigidbody、Input、Mecanimということでシーンにオブジェクトを登場させてキャラクタを操作して物理演算でインタラクションするという感じのところから触っていることが想像できます。また平均滞在時間が8分強ということで、熟読して頂いているみたいです。

Unityのバージョンも新しくなっていますし、頃合いをみてまとめなおしてみようかなと思います。

## 講演

講演については主に業務の一環としてFacebookのマーケティングソリューションについて話す事が多かったです。クローズドなものを合わせるともっとありますが、ひとまずパブリックなものは下記のような感じです。

- <a href="https://feedtech.net/">2016/09/06 FeedTech "Facebookダイナミック広告で勝ち続ける技術"</a>
- <a href="https://www.facebook.com/marketingjapan/videos/1137208323033284/">AdTech Tokyo 2016 ブースセッション</a>
- <a href="http://phpcon.php.gr.jp/2016/">2016/11/03 PHPカンファレンス2016 "Better PHP Development using HHVM and hack"</a>
- <a href="https://eventdots.jp/event/607872">2016/12/17 ビッグデーターオールスターズ "アドテク最前線　これが今のアドテクデータ活用法！"</a>
- <a href="https://facebookmarketingapi.doorkeeper.jp/events/54783">2016/12/15 Facebook Ads API meetup #4</a>
- <a href="https://facebookmarketingapi.doorkeeper.jp/events/52976">2016/10/26 Facebook Ads API meetup #3</a>
- <a href="https://facebookmarketingapi.doorkeeper.jp/events/40291">2016/03/15 Facebook Ads API meetup #2</a>
- <a href="https://facebookmarketingapi.doorkeeper.jp/events/37147">2016/01/27 Facebook Ads API meetup #1</a>
