---
layout: post
title:  "LEAP MotionとOculus Riftでチャーハンゲームを作って世界17位に入賞した"
date:   2015-01-11 12:00:00 +9:00
categories: blog
---

![ss](/images/FriedRice_Mac.png)

2014年11月29日に開催されたOculus GameJamで開発したチャーハンを作るゲームが、全世界から150以上の応募の集まったオンラインのコンテストで17位という最終結果になりました。

- [Announcing the Leap Motion 3D Jam Winners!](http://blog.leapmotion.com/announcing-leap-motion-3d-jam-winners/)
- [Winners of Leap Motion '3D Jam' Game Jam Contest Announced - Road to VR](http://www.roadtovr.com/leap-motion-3d-jam-winners-announced-indiecade-oculus-rift-virtual-reality/)

あくまで趣味で行っているゲーム開発で形になった結果を得ることが出来てとても嬉しく思っています。
MacとWindowsに対応していてLEAP Motionがあれば遊べます。プラスアルファでOculusに対応したビルドも用意していますので、もし宜しければ遊んでやってください。

<iframe src="//itch.io/embed/14880?dark=true&linkback=true" width="552" height="167" frameborder="0"></iframe>

せっかくなので開発中のバージョンの映像などを。

# 最初のバージョン (2014/11/17)

<iframe width="560" height="315" src="//www.youtube.com/embed/lLnmjmkI8eQ" frameborder="0" allowfullscreen></iframe>

LEAP Motionの道具追跡を試してみたところ面白そうだったので、これで炒飯を炒める事が出来るのではと思ったのがきっかけ。
フライパンのモデルデータは11/15に購入しているので、フライパンとLEAPのインテグレーションに2日ほど費やした形。

この時点ではLEAP Motion 3DJAMの存在は認知していなかったはず。
またOculus GameJamでこれをやるかどうかも未定でした。

# 背景とゲームルールを実装 (2014/11/17)

<iframe width="420" height="315" src="//www.youtube.com/embed/n72zS9Vl5pw" frameborder="0" allowfullscreen></iframe>

フライパンの動きが気に入ったので、米オブジェクトやキッチンをその日のうちに実装。
一定の制限時間内でスコアを稼ぐ形式を検討しているが、得点ロジックやゲームの流れは特に煮詰まっていないバージョン。

キッチンのモデルが不潔であるという点に苦言を呈され始める。

# GameJam前のプロトタイプ (2014/11/24)

<iframe width="420" height="315" src="//www.youtube.com/embed/GO6q4AcIrJM" frameborder="0" allowfullscreen></iframe>

オブジェクトの見た目が少しでも米に見えるようにするにはどうすればいいかを模索。
ニコニコ動画でMMDを使った炒飯を作った人が採用していた立方体型のモデルに変更した。
また巻き上げた食材が空中で一定のポイントに吸引される謎の力を実装。

- [【MMD】 チャーハン作るよテスト - ニコニコ動画:GINZA](http://www.nicovideo.jp/watch/sm13316405)

# Oculus GameJamバージョン (2014/11/30)

<iframe width="420" height="315" src="//www.youtube.com/embed/djZ0dGvcFnE" frameborder="0" allowfullscreen></iframe>

チームメイトの@nyakagawan さんとの相談の中でゲーム性などを検討し、複数の種類の炒飯を作って得点を算出する形式に変更。

食材のルーレットやオーダー表示のシステムなどは @nyakagawan さんの作です。
また食材の吸引にRigidbodyを使うのがうまくいかず時間を浪費してしまったのですが、教えていただいたiTweenを使うと劇的に簡単に実装できました。
それ以来iTweenを多用していて、個人的にはGameJamでの一番の収穫でした。
LEAP Motion 3DJamの締め切りも翌日だったのでこのバージョンをまずはアップロードしたのを覚えてます。

# セミファイナルバージョン (2015/01/07)

<iframe width="420" height="315" src="//www.youtube.com/embed/BIZsFt6Q0HM" frameborder="0" allowfullscreen></iframe>

セミファイナルに選ばれたということで最終選考に備えて手直しをしたバージョン。
時間がなくて調整しきれなかったモデルの改変やリザルト画面、ロゴなどをつくって作品としての体裁を調整。

やはり自分でモデリングなどが出来たほうがいいんだろうなと痛感することに。

# 米粒モデル化失敗作

<iframe width="420" height="315" src="//www.youtube.com/embed/6mAFQZbncfU" frameborder="0" allowfullscreen></iframe>

GameJam後に抜本的に米粒の動きを変更するべく試作したバージョン。しかしながら処理能力的に目標の3000粒には届かないので放置中。
Unity5の改良された物理エンジンで再挑戦したいが、現状のモデルでは対応できないコリジョンがあるようなので様子見。


# 振り返ってみて

やはりGameJamなくして今の形にはなっていないと思います。直近ですとGlobal GameJamが迫っています。
何か面白い作品が作ってみたい人は参加してみるといいのではないでしょうか。特にプログラマーではなくてもモデルや画像のデザイナーも需要があると思います。

- [Global Game Jam 2015 バンダイナムコ未来研究所会場 | Peatix](http://ggj2015-bns.peatix.com/)
