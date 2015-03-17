---
layout: post
title:  "Mementoで自分自身の3Dモデルを30分で生成"
date:   2015-03-16 12:00:00 +9:00
categories: blog
---

前回、前々回とAutodeskの123D Catchを使ったモデル作成を試しました。

- [友人をスマホで撮影して3Dモデル化してUnityで動かしてみた - Yusuke Ando a.k.a yando](http://yandod.github.io/blog/2015/02/01/123d-blender-unity/)
- [123D CatchのWindows版で友人の3Dモデル化が捗った - Yusuke Ando a.k.a yando](http://yandod.github.io/blog/2015/03/15/123d-on-windows/)

今回、それを更に上回るソフトがAutodeskからオープンβで公開中という事に気が付き、試してみました。
そのソフトとはProject Mementoと呼ばれていたもので、Autodeskが以前から扱っていた123D Catchや
Recapなどのキャプチャ製品をさらに発展させたソフトウェアのようです。

![ito](/images/memento-01.png)

- [Autodesk Memento](http://memento.autodesk.com/assets/home_slider/garuda_morph-v3-da3e37d5488e50091541e11b77f4f267.png)

Mementoの特徴としては下記のような点が挙げられます。

- 膨大な頂点数のデータを扱い、精度が高い
- データの編集や修正を行う機能がある
- FBX、OBJへのエクスポートやテクスチャのベイクに対応
- エクスポート時に頂点数の減算が可能
- 3Dプリンタ用にデータを最適化する機能もサポート
- Windows専用

実際の動作の流れは動画で見たほうがわかりやすそうです。

<div id="fb-root"></div><script>(function(d, s, id) {  var js, fjs = d.getElementsByTagName(s)[0];  if (d.getElementById(id)) return;  js = d.createElement(s); js.id = id;  js.src = "//connect.facebook.net/en_US/all.js#xfbml=1";  fjs.parentNode.insertBefore(js, fjs);}(document, 'script', 'facebook-jssdk'));</script><div class="fb-video" data-allowfullscreen="true" data-href="https://www.facebook.com/video.php?v=294738837354631&amp;set=vb.195716063923576&amp;type=1"><div class="fb-xfbml-parse-ignore"><a href="https://www.facebook.com/video.php?v=294738837354631&amp;set=vb.195716063923576&amp;type=1">Video</a></div></div>

今回は123D Catch用にミラーレスで撮影した画像を再度処理してみました。
処理時間は30分以上かかったとおもいますが、出来上がりのデータは驚異的な精度。

![ito](/images/memento-02.png)

顔はぶれてしまいましたが、道路や壁などについては強烈なリアリティです。
不要な部分を削除してFBXにエクスポート、Mixiamoでリギングすると一発で成功！
エクスポートの時間を短縮するため、頂点数は2万以下にしています。(元は500万くらい)

<iframe style="width:100%; min-height:315px" src="https://www.youtube.com/embed/sgKo15B05SE" frameborder="0" allowfullscreen></iframe>

この作業能率だと、かなりの人数のモデルデータを作成してコンテンツにできそうな気がします。
というか、本来の用途だと3Dプリンタとの組み合わせでデジタルからアナログへというのもアリらしいです。

いやー、すごいですね。
