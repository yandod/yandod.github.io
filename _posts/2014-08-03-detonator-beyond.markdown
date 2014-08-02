---
layout: post
title:  "Detonatorと爆発の未来"
date:   2014-08-03 10:00:00 +9:00
categories: unity
---

みなさん、こんにちは。@yandoです。

この記事は[Unity アセット真夏のアドベントカレンダー 2014 Summer！ - Unityアセット | Doorkeeper](http://unityassetjp.doorkeeper.jp/events/12843)に参加しています。
昨日は@nobikoさんによる「[無料アセットで作った岩場でユニティちゃんと走ってみる](http://nobikko-nobinobi.hatenablog.com/entry/2014/08/01/235000)」でした。

今回は先日のアセットまみれLT大会でも紹介した爆発アセットを記事として紹介します。

<script async class="speakerdeck-embed" data-id="75716ef0fa0c01311408323d6ac6076c" data-ratio="1.6" src="//speakerdeck.com/assets/embed.js"></script>

## 爆発はエフェクトの定番

![img1](/images/detonator_01.png)

アセットストアでExplosionのキーワードで検索するとエフェクトや音などさまざまなアセットが見つかります。
考えてみると爆発はレースゲーム、パズル、アクションと万能で使われるスイートスポットの広い要素です。これだけたくさんあるのも納得です。

たくさんある中でもレビュー数が多く高い人気を誇っているのがDetonatorです。

- [Asset Store - Detonator Explosion Framework](https://www.assetstore.unity3d.com/jp/#!/content/1)

## Detonatorは無料でカスタマイズ可能

![img2](/images/detonator_02.png)

DetonatorはUnity Summer of Codeで選出されたフリーの爆発フレームワークです。
簡単に爆風や火炎、衝撃などを実装できスクリプトからコントロールすることができます。
煙や爆音などの素材はデフォルトで付属しているものを差し替える事ができるので、なんだか見たことが有る爆発だなという感じを薄めることもできそうです。

提供されている機能は次のような機能です。

- Detonator
  - 基本となる爆発スクリプト
- Firaball
  - 火球を表示する
- Force
  - 爆発時に周囲の物体を吹き飛ばす
- Glow
  - 光る
- Heatwave
  - 熱波表現（Unity Pro）
- Light
  - 周囲を照らす
- Shockwave
  - 衝撃波の描画
- Smoke
  - 煙の表示
- Sound
  - 爆発音を再生
- Sparks
  - 火花を表示
- Object Spray
  - 任意のオブジェクトで破片をばらまく

## プレハブではなくコンポーネントがベター

![img4](/images/detonator_04.png)

動作のイメージを掴むだけなら<code>Prefabs</code>配下にあるプレハブを配置してパラメータを調整するのが簡単です。
とはいえデフォルトのパラメータを変更する部分が多くなってくると無駄も多くなってきます。何回か触ってみた結論としてはプレハブではなく、コンポーネントをアタッチして使うほうが良いのではと思います。

Detonatorを導入するとAdd Componentをクリックした後にDetonatorをアタッチするメニューが出てくるようになります。初めて気がついた時は「これがエディタ拡張というやつかー」と感心しました。
具体的には下記のようなコードがDetonatorに記述されていました。

<pre>
using UnityEngine;
using System.Collections;

[RequireComponent (typeof (Detonator))]
[AddComponentMenu("Detonator/Force")]
public class DetonatorForce : DetonatorComponent {
</pre>

先日のアセットまみれLTでもエディタ内でゲームをするアセットなどが紹介されていましたが、ワークフローに最適化した機能をエディタに追加することで開発効率を上げられそうですね。

アセットはソースコードを見ることでテクニックを学ぶことができるので奥が深いですね。

## DetonatorSoundは直接バグを修正せよ

コンポーネントを使いはじめると音声を再生するコンポーネントが動かない事に気が付きます。
色々とググった結果、ここはコード修正が必要です。

<pre>
override public void Init()
{
    _soundComponent = (AudioSource)gameObject.AddComponent ("AudioSource");
    }

void Awake()
{
    Init();
}
</pre>

<code>Awake</code>から<code>Init</code>を呼ぶというコードがプレハブでは不要ですが、コンポーネントでは必要なようです。
ここについてはコールバックの挙動を今度調べてみようと思います。

- [How to use Explosion/Detonator Framework - Unity Answers](http://answers.unity3d.com/questions/152878/how-to-use-explosiondetonator-framework.html)

## Sample Asset (Beta)という道は人柱向けだ！

![img5](/images/detonator_05.png)

現在も開発が進んでいると思われるこちらのアセットにも爆発が含まれています。
ですがこのアセットにはタグやプロジェクトセッティングなども同梱されているので安易にImport Allすると痛い目を観ますので気をつけてください。
またプロトタイピング用の積み木のようなブロックもとても便利でした。

さらに詳しい用法はQiitaもご覧ください。

- [UnityのDetonatorで爆発させる - Qiita](http://qiita.com/yando/items/eac9e0dbc1376b9cf141)


明日は@sassemblaさんによる記事です。お楽しみに。
