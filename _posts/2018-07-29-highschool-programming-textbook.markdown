---
layout: post
title:  "高校で使われているプログラミングの教科書を全部購入して比較 (情報の科学)"
date:   2018-07-29 9:00:00 +9:00
image: /images/highschool-text.jpg
description: 義務教育ではないものの、高校ではプログラミング教育を含むIT教育が「情報」という教科として2003年から実施されてきています。今回は情報の教科書を再び大人買いしましたので、全ての教科書に目を通した上でそれぞれの教科書の特徴を見ていきます。
categories:
  - blog
---
<figure>
<img src="{{ site.url }}/images/highschool-text.jpg" style="width:100%"/>
</figure>

義務教育ではないものの、高校ではプログラミング教育を含むIT教育が「情報」という教科として2003年から実施されてきています。
今回は情報の教科書を再び大人買いしましたので、全ての教科書に目を通した上でそれぞれの教科書の特徴を見ていきます。

[以前の記事](http://yandod.github.io/blog/2018/07/17/programming-textbook/)でも触れましたが、教科書は教科書会社が学習指導要領を元に作成し、教科書検定を受けたものが各学校によって採択され使用されます。
教科書に掲載されているからといってその内容がそのまま授業で行われるわけではないのは注意が必要です。

今回はその中でも平成28年に検定を受け、現在使用されている下記の6つの教科書を紹介します。
前置きが長くなりそうなので、各教科書について見たい方はジャンプしてください。

- [東京書籍 - 情報の科学 [情科306]](#東京書籍---情報の科学-[情科306])
- [実教出版 - 最新 情報の科学 新訂版 [情科307]](#実教出版---最新-情報の科学-新訂版-[情科307])
- [実教出版 - 情報の科学 新訂版 [情科308]](実教出版---情報の科学-新訂版-[情科308])
- [数研出版 - 改訂版 高等学校 情報の科学 [情科309]](数研出版---改訂版-高等学校-情報の科学-[情科309])
- [日本文教出版 - 新・情報の科学 [情科310]](日本文教出版---新・情報の科学-[情科310])
- [第一学習社 - 高等学校 情報の科学 [情科311]](第一学習社---高等学校-情報の科学-[情科311])

- [記事の執筆に使った簡易的な一覧表](https://docs.google.com/spreadsheets/d/1pOcR8RtOKSYo-3CqCzFmY_TWoJoaywzrTk4RVr7ePCk/edit?usp=sharing)

また今回の記事は教育に携わっていない方向けに紹介しますのでは高等学校を高校など一般的な用語で表します。

## 「情報の科学」とはどんな位置づけなのか

教科「情報」が平成15年(2003年)に開始されてから普通科の高校では常に必修の教科となっています。
しかしこれは選択必修という形になっており複数の科目が想定されていてそのうちいずれかを履修すれば良いという形式です。
当初の科目編成は次の3つです。

- **情報A**
  - コンピュータや情報通信ネットワークなどの活用を通して、情報を適切に収集・処理・発信するための基礎的な知識と技能を習得させるとともに、情報を主体的に活用しようとする態度を育てる。
- **情報B**
  - コンピュータにおける情報の表し方や処理の仕組み、情報社会を支える情報技術の役割や影響を理解させ、問題解決においてコンピュータを効果的に活用するための科学的な考え方や方法を習得させる。
- **情報C**
  - 情報のディジタル化や情報通信ネットワークの特性を理解させ、表現やコミュニケーションにおいてコンピュータなどを効果的に活用する能力を養うとともに、情報化の進展が社会に及ぼす影響を理解させ、情報社会に参加する上での望ましい態度を育てる。
- 参照
  - [高等学校学習指導要領（平成11年3月）> 第2章　普通教育に関する各教科　第10節　情報](http://www.mext.go.jp/a_menu/shotou/cs/1320181.htm)

抽象的な表現になっていますが、ざっくりいうとITリテラシーを扱う情報A、計算機科学とプログラミングを扱う情報B、表現と情報社会を扱う情報Cという構成です。
そして結果としてどうなったかというと多くの学校が情報Aだけを開講し、エクセルやパワポなどを教えるというICT教育という形になり、情報Bを開講して実施できた学校は少なかったと言われています。
これは教科ができても教える教員を新規に採用できるわけではなく、短期間の研修を受けた現職教員の誰かが担当したという背景があります。

この状況を受けて平成21年の学習指導要領では教科・情報は次のように再編されます。

- **社会と情報**
  - 情報の特徴と情報化が社会に及ぼす影響を理解させ，情報機器や情報通信ネットワークなど
を適切に活用して情報を収集，処理，表現するとともに効果的にコミュニケーションを行う能
力を養い，情報社会に積極的に参画する態度を育てる。
- **情報の科学**
  - 情報社会を支える情報技術の役割や影響を理解させるとともに，情報と情報技術を問題の発
見と解決に効果的に活用するための科学的な考え方を習得させ，情報社会の発展に主体的に寄
与する能力と態度を育てる。
- 参照
  - [ 学習指導要領等（ポイント、本文、解説等）（平成20年3月・平成21年3月）](http://www.mext.go.jp/component/a_menu/education/micro_detail/__icsFiles/afieldfile/2011/03/30/1304427_002.pdf)

3つあった科目が2つに統廃合され、情報収集、情報活用、コミュニケーション(つまり情報A+情報C)を扱う**社会と情報**と計算機科学やプログラミングを重視するものが**情報の科学**と再定義されたわけです。
これによりコーディングを含むようなプログラミングは基本的に「情報の科学」の科目で実施されるようになりました。
このような経緯もあり、これから紹介する教科書の中には妙に古臭く感じる記述や内容がある時がありますが、それは過去の情報Bから引き継いでいるという側面があるでしょう。

また補足になりますが、次回の学習指導要領にて教科・情報は再びの再編を控えています。次は下記のような編成になります。

- **情報Ⅰ**
  - 情報に関する科学的な見方・考え方を働かせ，情報技術を活用して問題の発見・解決を行う学習活動を通して，問題の発見・解決に向けて情報と情報技術を適切かつ効果的に活用し，情報社会に主体的に参画するための資質・能力を次のとおり育成することを目指す。
- **情報Ⅱ**
  - 情報に関する科学的な見方・考え方を働かせ，情報技術を活用して問題の発見・解決を行う学習活動を通して，問題の発見・解決に向けて情報と情報技術を適切かつ効果的，創造的に活用し，情報社会に主体的に参画し，その発展に寄与するための資質・能力を次のとおり育成することを目指す。
- 参照
  - [高等学校学習指導要領（案)](http://search.e-gov.go.jp/servlet/PcmFileDownload?seqNo=0000170358)
  - [新学習指導要領における
情報教育の動向](https://www.ipsj.or.jp/magazine/9faeag000000tq7i-att/5901education.pdf)
  - [高等学校学習指導要領の改訂に伴う移行措置案に対する意見公募手続（パブリックコメント）の実施について](http://search.e-gov.go.jp/servlet/Public?CLASSNAME=PCMMSTDETAIL&id=185000995&Mode=0)
  - [高等学校学習指導要領（平成30年3月公示）関係](http://www.mext.go.jp/component/a_menu/education/micro_detail/__icsFiles/afieldfile/2018/07/13/1407073_11.pdf)

何が変わったかこれだけだとわからないですよね？内容の方も見るとこんどはどちらにも「プログラミング」が入ります。つまり高校でもプログラミング教育が本当に必修になります。
教育行政に興味が出てきた方はパブリックコメントの動向や続報をチェックしてみてください。というわけで本題の各教科書のレビューです。

## 各社の教科書の全体的な傾向

前置きがずいぶん長くなりましたが、ここからが情報の科学の教科書の内容です。
学習指導要領では下記のような項目が提示されているのでこれらをカバーする形で各社が教科書を編纂しています。

- コンピュータと情報通信ネットワーク
  - コンピュータと情報の処理 (注: 文字エンコーディングの言及あり)
  - 情報通信ネットワークの仕組み (注: DNS TELNET、Webサーバー、URLの言及あり)
  - 情報システムの働きと提供するサービス
- 問題解決とコンピュータの活用
  - 問題解決の基本的な考え方
  - 問題の解決と処理手順の自動化 (注: プログラム言語の言及あり)
  - モデル化とシミュレーション (注: プログラム言語の言及あり)
- 情報の管理と問題解決
  -  情報通信ネットワークと問題解決
  - 情報の蓄積・管理とデータベース (注: SQLとは書かれていない)
  - 問題解決の評価と改善
- 情報技術の進展と情報モラル
  - 社会の情報化と人間
  - 情報社会の安全と情報技術
  - 情報社会の発展と情報技術

各社の教科書がどのような意図で編纂されたのかは下記で趣意書が公開されています。

- [教科書編修趣意書　高等学校　情報の科学](http://www.mext.go.jp/a_menu/shotou/kyoukasho/tenji/1371233.htm)

個別の特徴はこのあとに記しますが、全体的な傾向としては下記のような内容が各社共通してカバーされていました。

- アナログとデジタルの違い、データ化、基数変換(2進数、16進数)、文字コード
- ネットワークの仕組み TCP/IP、DNS、E-mail
- アルゴリズム
- データベース、正規化(第1、第2、第3)
- POSシステム
- なんらかの形でのWeb
- セキュリティや関連法規、ネットトラブル

ではここからが各教科書の特徴です。

## 東京書籍 - 情報の科学 [情科306]

中学校の教科書がとても楽しい内容になっていた東京書籍の教科書は比較的スッキリした内容で、かつ興味を引くような実習内容が入っていました。

たとえば[テキスト音楽 サクラ](https://sakuramml.com/)を使ったDTMは他社の教科書には見られない実習内容です。
[ドリトル](http://dolittle.eplang.jp/)を使った実習も視覚的かつ、日本語でのコーディングが出来るので敷居が低そうです。

上記のような楽しい教材以外にはHTML、CSS、VBAなどが登場しておりテクニカルな部分は易しめになっているように感じます。
一方で知識面ではクリエイティブ・コモンズやSOHOなどのトレンドにも言及していました。
またデータベースの概念や設計に加えてSQLも例示されています。

<blockquote class="twitter-tweet" data-lang="ja"><p lang="ja" dir="ltr">東京書籍の情報の科学[情科306]<br>情報量を抑えてスッキリしている。テキストから音楽を作成する実習、メールヘッダとプロトコル、パソコンのスペック表解読などがユニーク。 <a href="https://t.co/FAylnUGet2">pic.twitter.com/FAylnUGet2</a></p>&mdash; Yusuke Ando@プログラミング教育に詳しい (@yando) <a href="https://twitter.com/yando/status/1023444743903047682?ref_src=twsrc%5Etfw">2018年7月29日</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

<blockquote class="twitter-tweet" data-lang="ja"><p lang="ja" dir="ltr">情科306 コーディングはHTML、CSS、VBA。SQLも例が示されている。ドリトルという日本語のタートル言語も。 <a href="https://t.co/Cn8O0vPWG3">pic.twitter.com/Cn8O0vPWG3</a></p>&mdash; Yusuke Ando@プログラミング教育に詳しい (@yando) <a href="https://twitter.com/yando/status/1023446107010068480?ref_src=twsrc%5Etfw">2018年7月29日</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

<blockquote class="twitter-tweet" data-lang="ja"><p lang="ja" dir="ltr">情科306<br>クリエイティブコモンズ、SOHO、ユニコード、twitterなど言及あり。 <a href="https://t.co/YRtncJykcE">pic.twitter.com/YRtncJykcE</a></p>&mdash; Yusuke Ando@プログラミング教育に詳しい (@yando) <a href="https://twitter.com/yando/status/1023446912114933760?ref_src=twsrc%5Etfw">2018年7月29日</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

## 実教出版 - 最新 情報の科学 新訂版 [情科307]

実教出版の教科書はアカデミックな雰囲気の強い教科書です。特にCPUの動作の仕組みを説明するためにレジスタやメモリの番地を操作する簡易アセンブリの例が登場するのは群を抜いています。
一方でこれだけ込み入った内容を果たして現場の先生が教えられるのかというのは不安ですが面白いですね。
暗号化やアルゴリズムについても比較的深く解説しており、VBAで書かれたコードはインデントも深い構造になっています。
SQLの具体例の例示もありました。

知識面ではクリエイティブ・コモンズやSOHO、Wikiの言及はありますが、Eメールのマナーや文字コードについての記述は一昔前の内容という感じが強いです。

<blockquote class="twitter-tweet" data-lang="ja"><p lang="ja" dir="ltr">実教出版 最新情報の科学 新訂版 [情科307]<br>計算機科学テイストが強い。擬似アセンブラやさまざまなアルゴリズム実装、データ圧縮などが目立つ。 <a href="https://t.co/ARjPu2L6p8">pic.twitter.com/ARjPu2L6p8</a></p>&mdash; Yusuke Ando@プログラミング教育に詳しい (@yando) <a href="https://twitter.com/yando/status/1023461392383242240?ref_src=twsrc%5Etfw">2018年7月29日</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

<blockquote class="twitter-tweet" data-lang="ja"><p lang="ja" dir="ltr">[情科307]<br>HTMLメールを避ける、Webページで一般的なEUCなど現在の状況にそぐわない記述もあり。<br>一方で在宅勤務、クリエイティブコモンズの言及あり。検索エンジンの分類も本文には無し。 <a href="https://t.co/QtXoRAGcgE">pic.twitter.com/QtXoRAGcgE</a></p>&mdash; Yusuke Ando@プログラミング教育に詳しい (@yando) <a href="https://twitter.com/yando/status/1023462850587590656?ref_src=twsrc%5Etfw">2018年7月29日</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

## 実教出版 - 情報の科学 新訂版 [情科308]

実教出版からは2種類の教科書が発行されており、同じ科目でありながら注力する点が変わっています。
言語のようなものはVBAしか取り扱わない代わりに、問題としては数独を解くプログラムや暗号の作成などに取り組みます。
ウェブを重視しないのであればエクセルさえあれば実習ができるような形なので使いやすいのかもしれません。

<blockquote class="twitter-tweet" data-lang="ja"><p lang="ja" dir="ltr">実教出版 情報の科学 新訂版 [情科308]<br>内容のスコープとレベルを限定することで教えやすくする意図を感じる。HTMLすら取り扱わず、実習は全てVBAに限定した上で数独を解く、オリジナル暗号などユニーク。パスワード作成にも言及も。 <a href="https://t.co/B3rYIzEn53">pic.twitter.com/B3rYIzEn53</a></p>&mdash; Yusuke Ando@プログラミング教育に詳しい (@yando) <a href="https://twitter.com/yando/status/1023473681773690882?ref_src=twsrc%5Etfw">2018年7月29日</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

<blockquote class="twitter-tweet" data-lang="ja"><p lang="ja" dir="ltr">[情科308]<br>同じ実教出版と同様の文字コードの記述。検索エンジンの使い方は以前のヤフー想定か? SQLはコラム的扱い。httpsは錠は出ますという扱い。 <a href="https://t.co/pwOLcdY3es">pic.twitter.com/pwOLcdY3es</a></p>&mdash; Yusuke Ando@プログラミング教育に詳しい (@yando) <a href="https://twitter.com/yando/status/1023475066070228993?ref_src=twsrc%5Etfw">2018年7月29日</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>


## 数研出版 - 改訂版 高等学校 情報の科学 [情科309]

数研出版の教科書の特徴は非常に豊富な実例の引用です。
ネット炎上に関するトラブルなど、ぼやかした例として紹介する教科書は多いのですがこの教科書では新聞記事のスクラップが多数貼られており、何が起きるかという事を強く伝えようとしています。

また手を動かす実習を扱わない代わりに知識の内容は先進的になっていて、「電池が長持ちする偽アプリ」やデータベースのトランザクション、Unicodeを3バイトの例として表示するなど頑張っています。
また検索エンジンについてはディレクトリ型は少なくなってきていると書かれており、ディレクトリ型の大手がなくなった現在の状況とも整合性を保っています。

ニコニコ動画や初音ミク、同人マークなどが教科書に掲載されている点も面白いですね。

<blockquote class="twitter-tweet" data-lang="ja"><p lang="ja" dir="ltr">数研出版 改訂版 高等学校情報の科学 [情科309]<br>実際にコンピューターを使う実習を廃して座学に特化。実際の新聞記事の引用が豊富。日常の問題を防ぐ意思を感じる。アルゴリズムは探索をVBA 偽アプリにも言及。 <a href="https://t.co/rznyMkg3xC">pic.twitter.com/rznyMkg3xC</a></p>&mdash; Yusuke Ando@プログラミング教育に詳しい (@yando) <a href="https://twitter.com/yando/status/1023483510152093696?ref_src=twsrc%5Etfw">2018年7月29日</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

<blockquote class="twitter-tweet" data-lang="ja"><p lang="ja" dir="ltr">[情科309]<br>SQLは扱わないが、トランザクションに言及。文字コードについてもunicodeを3バイトもあり得る例示に。クリエイティブコモンズ、同人マーク、在宅勤務も。 <a href="https://t.co/z5oBOOXEDd">pic.twitter.com/z5oBOOXEDd</a></p>&mdash; Yusuke Ando@プログラミング教育に詳しい (@yando) <a href="https://twitter.com/yando/status/1023484560774815745?ref_src=twsrc%5Etfw">2018年7月29日</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

<blockquote class="twitter-tweet" data-lang="ja"><p lang="ja" dir="ltr">[情科309]<br>ディレクトリ型サーチは少なくなってきていると言及。Eメールのマナー、あいさつ、テキスト形式など。初音ミク、ニコ動、ピクシブも登場。 <a href="https://t.co/eZeEm4bnsw">pic.twitter.com/eZeEm4bnsw</a></p>&mdash; Yusuke Ando@プログラミング教育に詳しい (@yando) <a href="https://twitter.com/yando/status/1023489876065378304?ref_src=twsrc%5Etfw">2018年7月29日</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

## 日本文教出版 - 新・情報の科学 [情科310]

日本文教出版の教科書は村井純先生の名前も入っている通り、実際に現役のエンジニアから見ると最も高度な教科書といってよいでしょう。
実習は全てJavaScriptとVBAを併記する形になっており、またプログラミング自体も分岐や変数といった基礎構文をカバーしてからアルゴリズムに進むようになっています。
またアルゴリズムのコストの比較も行われています。

ブートローダ、NoSQL、ファームウェアアップデート、NOC、オープンソースのような完全にテクニカルな単語が入ってくるのもこの教科書の特徴です。
また動画や静止画のファイルサイズについてもフレーム間圧縮にまで言及しているのはこの教科書だけです。
Unicodeが4バイトになるケースを想定した記述もありました。
大手ショッピングサイトの公開鍵の中身を確認してみましょうという課題も実世界の痛い所をついています。

検索エンジンについてはクローラを前提としてアルゴリズムで並べ替えられている事、SEO対策がある事、任意のサイトのSEO対策をmetaタグで確認するといった内容まで入っているのもこの教科書だけです。

ほとんどの点で他の教科書よりも深い内容になっており、大学レベルでの計算機科学などにつなげようとしているのではと感じました。
理数系に強い学校などには良さそうです。ですが明らかに人を選ぶ教科書で実務的な経験が薄い先生がこの教科書を使うのには大変な努力がいるかと思います。

<blockquote class="twitter-tweet" data-lang="ja"><p lang="ja" dir="ltr">日本文教出版 新・情報の科学 [情科310]<br>村井純先生の名前も入っており専門性が高い。実習はJavaScriptとマクロ言語(VBA)を常に併記。<br>逐次探索と二分探索のコストの違いの考察も行う。計算機科学やソフトウェア工学に近い。 <a href="https://t.co/rtOZpyhOyx">pic.twitter.com/rtOZpyhOyx</a></p>&mdash; Yusuke Ando@プログラミング教育に詳しい (@yando) <a href="https://twitter.com/yando/status/1023528787277885442?ref_src=twsrc%5Etfw">2018年7月29日</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

<blockquote class="twitter-tweet" data-lang="ja"><p lang="ja" dir="ltr">[情科310]<br>ブートローダ、フレーム間圧縮、WiFiのセキュリティ、NoSQLとどのトピックも一段階深い踏み込み。<br>大手ショッピングサイトの公開鍵を確認してみようという実習もよい。 <a href="https://t.co/3DdPVEXeFe">pic.twitter.com/3DdPVEXeFe</a></p>&mdash; Yusuke Ando@プログラミング教育に詳しい (@yando) <a href="https://twitter.com/yando/status/1023530515456909312?ref_src=twsrc%5Etfw">2018年7月29日</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

<blockquote class="twitter-tweet" data-lang="ja"><p lang="ja" dir="ltr">[情科310]<br>文字コードの記述も詳細、検索エンジンはクローラを前提にSEOにも言及。RSA鍵の破り方、アフィリエイトの仕組み。現代的な内容が反映されている。 <a href="https://t.co/Wy2tN6QdDg">pic.twitter.com/Wy2tN6QdDg</a></p>&mdash; Yusuke Ando@プログラミング教育に詳しい (@yando) <a href="https://twitter.com/yando/status/1023535719388610560?ref_src=twsrc%5Etfw">2018年7月29日</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

<blockquote class="twitter-tweet" data-lang="ja"><p lang="ja" dir="ltr">[情科310]<br>電子メールのマナーの記述あり。HTMLの禁止言及は無し。NOC、クリエイティブコモンズ、オープンソースの記述あり。<br>巻末にJISコード表。 <a href="https://t.co/EOWTGXhToP">pic.twitter.com/EOWTGXhToP</a></p>&mdash; Yusuke Ando@プログラミング教育に詳しい (@yando) <a href="https://twitter.com/yando/status/1023537017932541952?ref_src=twsrc%5Etfw">2018年7月29日</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

## 第一学習社 - 高等学校 情報の科学 [情科311]

第一学習社の教科書はアニメ絵が多く、一見軟派な印象を受けるのですが内容はなかなか工夫されています。
例示や実習を全てJavaScriptに統一しており、その上でプログラムの書き方に幅があることや計算量の比較、CANVASなども扱っています。
アルゴリズムの例題もパリティ、待ち行列、バブルソート、コームソート、時間量計算、ライフゲームなど幅広く登場します。
またシステム開発を想定したような「ブルックスの法則」の解説や作業ミス、USBメモリの紛失による情報漏えいなども扱っています。

クリエイティブ・コモンズについては自作の地域キャラクタを創ってライセンスを考えよう。やくまもんなどのキャラクタのライセンスを調べてみようという実地的な内容が盛り込まれています。

こちらの教科書はシステムエンジニアやプログラマを目指す職業訓練への入り口というような印象が強く、生徒の進路の状況がそういった形ならフィットするのかなと思いました。
おそらく数年でもそういった業界の経験があるとか、友人がいるという先生ならうまく教えられそうな内容です。

<blockquote class="twitter-tweet" data-lang="ja"><p lang="ja" dir="ltr">第一学習社 高等学校 情報の科学 [情科311]<br>ビット高校という設定のアニメ絵が多い教科書だが内容は本格派。例示はJavaScriptに統一されていて、さまざまなアルゴリズムに時間量計算も扱う。 <a href="https://t.co/S8uhUtHVry">pic.twitter.com/S8uhUtHVry</a></p>&mdash; Yusuke Ando@プログラミング教育に詳しい (@yando) <a href="https://twitter.com/yando/status/1023540236565995520?ref_src=twsrc%5Etfw">2018年7月29日</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

<blockquote class="twitter-tweet" data-lang="ja"><p lang="ja" dir="ltr">[情科311]<br>プログラミングは答えが一つとは限らないと言及する教科書は珍しい。素数判定、Canvasでのグラフィック処理などの例題も陳腐化していない。<br>ブルックスの法則やテストと保守に言及しているのも珍しい。 <a href="https://t.co/LvOzT6A9ev">pic.twitter.com/LvOzT6A9ev</a></p>&mdash; Yusuke Ando@プログラミング教育に詳しい (@yando) <a href="https://twitter.com/yando/status/1023541522313039872?ref_src=twsrc%5Etfw">2018年7月29日</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

<blockquote class="twitter-tweet" data-lang="ja"><p lang="ja" dir="ltr">[情科311]<br>クリエイティブコモンズの紹介と地域キャラを作ってライセンスを考える問いかけ。文字コードはUTF-8がよく使われるという記載。メールについては｢きちんとしたメール｣の例のみ。検索はクローラを前提に欄外でディレクトリ型を捕捉。 <a href="https://t.co/wWWrIuyHqR">pic.twitter.com/wWWrIuyHqR</a></p>&mdash; Yusuke Ando@プログラミング教育に詳しい (@yando) <a href="https://twitter.com/yando/status/1023542678317756417?ref_src=twsrc%5Etfw">2018年7月29日</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

## まとめ 優れた記述の教科書は存在する

なんとなくあら捜しをしようとするとさまざまな事情で不正確、あるいは陳腐化した記述を教科書から見つけるのは難しくありませんでした。
これはどの教科の教科書であってもそうかと思います。
一方で多くの教科書には工夫を凝らしたと思われる特徴があり、見比べてみるのはとても興味深い体験でした。

もちろん教科書が正確であったほうがいいのはもちろんですが、正確であればいい教科書かというとそうでもないでしょう。
学校の設備や生徒の状況、先生の対応可能な範囲などを元に教科書を選び授業を実施するという事なのだと思います。

- プログラミング教育に関するその他の記事
  - [ディスる前に知っておくべき「プログラミング教育」のこと](https://yandod.github.io/blog/2018/06/28/programming/)
  - [中学校で使われているプログラミングの教科書を全部購入して比較](https://yandod.github.io/blog/2018/07/17/programming-textbook/)
  - [日本のプログラミング教育は諸外国より遅れているのか？](https://yandod.github.io/blog/2018/07/22/ict-education-in-the-world/)

## 追記 東京都教育委員会による教科書の研究結果

各地域の教育委員会が教科書採択の助けになるような調査や学校への推奨をする場合があるようです。
東京都教育委員会の場合は結果がウェブサイトにて講評されていました。
事前に見ていたらバイアスがかかりそうなくらいよくまとまっています。私の書いた上記の評価は個人の観点ですので教育委員会による評価と合わせて見ることで教科書の特徴がさらによくわかるかと思います。

- [平成29年度使用　高等学校用教科書調査研究資料（共通教科）](http://www.kyoiku.metro.tokyo.jp/school/textbook/high_school/research_common_2017.html)

<blockquote class="twitter-tweet" data-lang="ja"><p lang="ja" dir="ltr">高校の情報の科学の教科書について東京都教育委員会が研究した内容が公表されていました。みなさんが感じた印象と教育委員会の評価は一致しますか？　発展的な内容と構成上の工夫については下記のような講評です。<a href="https://t.co/IEGTKB2ivx">https://t.co/IEGTKB2ivx</a> <a href="https://t.co/TenN9htTY2">pic.twitter.com/TenN9htTY2</a></p>&mdash; Yusuke Ando@プログラミング教育に詳しい (@yando) <a href="https://twitter.com/yando/status/1023900739196747777?ref_src=twsrc%5Etfw">2018年7月30日</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

<blockquote class="twitter-tweet" data-lang="ja"><p lang="ja" dir="ltr">各教科書の実習内容がひと目でわかりますね。 <a href="https://t.co/GpqRryeMvV">pic.twitter.com/GpqRryeMvV</a></p>&mdash; Yusuke Ando@プログラミング教育に詳しい (@yando) <a href="https://twitter.com/yando/status/1023902073551708161?ref_src=twsrc%5Etfw">2018年7月30日</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>
