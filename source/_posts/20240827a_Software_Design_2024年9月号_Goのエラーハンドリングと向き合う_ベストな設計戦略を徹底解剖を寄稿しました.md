---
title: "Software Design 2024年9月号 Goのエラーハンドリングと向き合う ベストな設計戦略を徹底解剖を寄稿しました"
date: 2024/08/27 00:00:00
postid: a
tag:
  - SoftwareDesign
  - Go
  - 寄稿
  - エラーハンドリング
category:
  - Programming
thumbnail: /images/20240827a/thumbnail.png
author: 後藤玲雄
lede: "2024年8月17日に発売された、[Software Design 2024年9月号]の第二特集である、「Goのエラーハンドリングと向き合う  ベストな設計戦略を徹底解剖」 の2章を後藤、3章を渋川で執筆し寄稿させていただきました。"
---

## はじめに

2024年8月17日に発売された、[Software Design 2024年9月号](https://gihyo.jp/magazine/SD/archive/2024/202409)の第二特集である、**「Goのエラーハンドリングと向き合う  ベストな設計戦略を徹底解剖」** の2章を後藤、3章を渋川で執筆し寄稿させていただきました。

このような貴重な機会をいただいた栗木さんをはじめ技術評論社の方々には、心からお礼申し上げます。

<img src="/images/20240827a/image.png" alt="" width="320" height="452" loading="lazy">

## みどころ

Go言語初心者から熟練者まで楽しんでいただける内容になっていると思います。

Go言語を利用する上でエラーハンドリングは必須の知識になるので、ぜひご一読ください。Goに馴染みのない方でもGo特有のエラー処理の方法を知ることで、普段触れている言語の理解を深めることができると思います。他言語と比較した、Go言語のエラーの特徴もみどころの一つです。

【第2特集】Goのエラーハンドリングと向き合う
第1章　Goのエラー処理を理解する／mattnさん
第2章　失敗しないGoのエラー設計戦略／後藤 玲雄
第3章　GoのエラーハンドリングQ＆A／渋川 よしき

2章ではGoのエラーの基本要素を標準ライブラリの実装から丁寧に説明しています。エラーの分類やアンチパターンの紹介、Go流のエラーハンドリングの方法など、Goでエラー設計をする上で必要な情報をカバーしています。

3章はエラーハンドリングのQ＆Aで、スタックトレースや並列処理など一歩進んだGoのエラーハンドリングの方法やエラーハンドリングとは何かといった深い部分の解説がみどころです。Goのエラーハンドリングに関する疑問を解決してくれること間違いなしの内容になっています。

## Software Design とは

技術評論社が出版している月刊の技術情報誌です。Webサービスを開発するソフトウェア業界のエンジニアにとっては説明不要と言っていいくらい鉄板です。

毎月様々なテーマについて特集を組んで取り扱っており、プログラミングだけでなく、OSやネットワークまで、その内容は多岐に渡ります。入門者・初心者向けの内容から実践的な内容も多く含まれているので、新人からベテランまであらゆるエンジニアにおすすめできる雑誌です。

[定期購読](https://www.fujisan.co.jp/product/1535/?tt=opt&gad_source=1&gclid=CjwKCAjwoJa2BhBPEiwA0l0ImNtJPU8-qPk3sAeCDs0DBF7p_5a5Do0DlzA_EwQ01jfqNWn-xcsG8hoCAJwQAvD_BwE)をして、業界の最新情報をアップデートするのもおすすめです！

## 執筆のきっかけ

「[実用 Go言語](https://www.oreilly.co.jp/books/9784873119694/)」の著作である渋川に、技術評論社からお声かけいただいたことがきっかけになります。渋川がフューチャー社内で執筆希望者を募集しており、私は普段業務でGo言語を利用しているので、いい機会だと思い執筆に挑戦させてもらいました。

Software Designという権威ある雑誌への寄稿ということで、不安はありましたが、執筆未経験であっても社内有数のGo言語の有識者である渋川、真野からレビューをもらえるという安心感もあり執筆することになりました。挑戦してみたいが少し不安があると真野に相談したところ「渋川さんにレビューしてもらえるんだから、不安に思うことってある？せっかくの機会なのにやらない理由ってないよね」と言われその通りだと思った事を鮮明に覚えています。フューチャーでは若手であっても手を挙げれば、難しい事でも任せてもらえる機会が多いと思います。

## 学んだこと

今回の執筆で得た学びを箇条書き形式で紹介していきます。

### 文章を書くテクニック

- お題に関して伝えたい内容を箇条書きで一覧に書き出す
- まとめたトピック一覧に過不足がないか有識者にレビューをしてもらう
- 有識者に最新の動向や過去の面白い話を聞けるたりもするので、周りの人に積極的に頼る
- 構成が決まりきっていない段階から、それぞれのトピックについて書きたい事を書く
- 文章を書いているうちにより良い構成を思い浮かぶことが多い
- 経験が浅いと良い構成を考えることは難しいので、積極的にフィードバックをもらう（特に相互依存しているトピックの構成は難しい）
- 記事や書籍を書き慣れている方や編集者の方の文章力や構成力はすごい（一度弟子入りすべき）
- 定義、原理、そのものが生まれた背景を理解して説明に盛り込むと全体感が伝わりやすい
- 複雑なものは表にまとめて特徴や解説を記載する

### 技術記事を書くうえで必要だと感じたこと

- [技術書執筆のススメ](https://future-architect.github.io/articles/20240403a/)を読む
- 普段から情報収集を行いネタをストックする
- 普段の業務でより良い方法を模索して実践する
- 言語や技術の背景や原理を理解する（ソースコードを読む）
- よいお手本を見つける
  - Goのエラーハンドリングをうまく行っているライブラリを読み込むなど
- 広い視野を持つ
  - 日本語の特徴を語る上では、英語などその他の言語の特徴を知る必要がある
  - Goにつて語るためには、JavaやPythonなどの仕組みや特徴を理解する必要がある

## 最後に

とても素晴らしい機会をいただきありがとうございました。

渋川さん、真野さんには構成の相談からレビューまでとても手厚くサポートいただきました。執筆期間の約3週間、ほとんど毎日原稿を修正して、その都度レビューをいただきました。合計で100件以上レビューをいただき良い記事を書くことができました。本当にありがとうございました！
