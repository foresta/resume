# resume

## 個人データ

|key|value|
|---|---|
| Name | 森田和樹 Morita Kazuki|
| Blog | https://blog.foresta.me |
| Twitter | [@kz_morita](https://twitter.com/kz_morita) 
| GitHub | [@foresta](https://github.com/foresta) |
| Qiita | [@kz_morita](https://qiita.com/kz_morita) |
| LinkedIn | https://www.linkedin.com/in/kazuki-morita-598796118/ |
| Speaker Deck| https://speakerdeck.com/kz_morita |

## 概要

ソフトウェアエンジニアとして，2014~現在に至るまで 9年の実務経験があります．
B2C サービスとしてゲーム系や，スマホアプリ，Webアプリケーションを開発をしてきました．

直近での株式会社スタンバイでは，バックエンドエンジニアとして入社したのち，サーバーサイドの Scala エンジニアとして求人検索エンジンのデータの管理システムの開発に携わってきました。

## 職務経歴

### 株式会社スタンバイ（202109 - 現在）

#### 求人のデータストアの開発・運用

##### 環境
- チーム規模: 8~10人
- 役割: サーバーサイドエンジニア
- 使用技術: 
  - プログラミング: Scala, Python, ShellScript
  - インフラ: AWS (ECS/Fargate, Lambda, EMR, Athena, Aurora, ElastiCache Redis), Terraform, DataDog
  - ライブラリ: Akka, Flink, Play Framework, ZIO

##### 主な業務と成果

- 求人票取り込みシステムの開発と運用
  - 求人票を取得 (crawling) し、保管・データ付与、配信するシステムの運用・開発を実施した
  - 求人票の更新が毎日実施されており、データベースへの書き込み負荷が高いためメンテナンスが必要
  - そのため deadlock の解消や DB に対する `OPTIMIZE TABLE` などを実施した
  - 結果としてシステムの安定稼働に貢献でき、エラー・アラート数の削減を実現できた

- 求人票のデータ分析
  - 求人票をデータ基盤上で分析し、欠損している情報を可視化
  - 結果として、営業の方に共有し顧客に欠損している情報を埋めていただき欠損率を低下させた
  - ほかにも、改善施策前にデータ上でシミュレーションを行い施策の効果を可視化することで施策の Return を見積もることができた

- 求人入稿マニュアルページの設計と開発
  - 顧客にむけて求人入稿マニュアルをWebページとして作成する要件があり、技術選定と実装を行った。
  - Hugo を用いたコンテンツシステムと、S3 + CloudFront で構築
  - 結果として運用保守が楽なマニュアルシステムを短期間で構築した

### 株式会社ニューズピックス (201811 - 202108)

#### 新規Webアプリケーション (UGM) の設計・開発

ユーザーがコンテンツを投稿するWebアプリケーションの新規立ち上げの設計と開発を行いました．

##### 環境
- チーム規模: 3人 (エンジニア)
- 役割: サーバーサイドエンジニア 兼 フロントエンドエンジニア
- 使用技術: Kotlin, Jersey, Kodein, Grizzly2, Hibernate, React, Redux, TypeScript, Express, Contentful, Cypress, AWS (ECS/Fargate, Aurora, ElastiCache Redis etc...)

##### 主な業務と成果
- API Server技術選定
  - 社内で知見が溜まっている Kotlin を採用 (候補としては golang を検討していた)
  - 結果としてサービスが素早く立ち上がり，プロダクトのローンチまでスムーズに開発が進行
- 認証基盤の設計と実装
  - NewsPicks のアカウントを利用した認証システムの複雑なフローを設計し実装
  - 結果として特に大きな問題なくリリースすることができた
  - 認証のドキュメント詳細に残したことにより，社内へ共有し別プロダクトへ横展開を行った
- APIサーバー開発
  - DB設計，クラス設計(ドメインモデル設計)から担当
  - 4層のレイヤードアーキテクチャを採用
  - 初回設計からプロダクトローンチまで大きな修正なく開発が進んだ
- フロントエンド開発
  - React を用いてページやコンポーネントの実装
- E2E テストの導入
  - 手動の結合テストの負荷を下げるべくE2Eテストを導入
  - Cypress と GitHub Actions を用いて，PullRequest 時にテストが走るように設定
  - 最低限のページコンテンツが表示されることを担保でき，安全にリリースが実施可能に
- aws-cdkによるインフラ構築
  - メモリキャッシュのParge用のElasticacheの構築
  - Lambda + CloudWatch によるバッチ処理の構築

#### 新規Webメディアの設計・開発

短期間で新しい Webメディアの新規開発を行いました．

##### 環境
- チーム規模: 3人
- 役割: フロントエンドエンジニア
- 使用技術: Nuxt.js, Vue.js, Vuex, Node.js, Redis, Express, Stylus, Pug, HTML, CSS, Contentful

##### 主な業務と成果
- 使用する技術選定
  - デザイナーとの協業を鑑みて，より HTML /CSS ライクにかける Vue.js を採用
  - 開発期間が短かったので，フレームワークにのることを検討し Nuxt.js を採用
  - Webメディアの入稿や，データストアとして Contentful を選択
  - 結果として3ヶ月短い期間でローンチすることができた
- Webフロントのコーディング
  - 要素のComponent化
  - Contentful のRichTextをParseし描画する処理の実装

- Expressのバックエンド実装
  - ユーザー認証や，Contentful へのアクセスを行うBFFとして実装
  - Redis によるキャッシュ

#### 会員向けのiOSアプリ開発

NewsPicksとは別の会員向けアプリのiOS開発を行いました．時と場合に応じてサーバーサイドの開発なども適宜実施しました．

##### 環境
- チーム規模: 3~5人
- 役割: iOSエンジニア
- 使用技術: Swift, Objective-C, Realm, XCode, Bitrise

##### 主な業務と成果

- iOSアプリのオーナーとして運用
  - PRレビューや不具合修正，申請作業など
- 新規の画面や機能実装
  - 動画のダウンロード機能とオフライン再生
- iOS13 対応
  - dark mode 設定
  - モーダルの挙動修正
  - Realmバージョンアップ

### 株式会社トランスリミット (201601 - 201810)

#### 新規モバイル3Dゲームの開発

ボクセルデザインを用いた3Dゲームの新規開発を行いました．街作り機能をメインで開発しました．

##### 環境
- チーム規模: 20人ほど
- 役割: アプリのクライアントエンジニア
- 使用技術: C++11/14, Cocos2d-x, protobuf, Xcode, Android Studio

##### 主な業務と成果

- さまざまな3D表現の実装
  - どんな表現が可能かを探るため，開発スピードを意識して実装
  - 気持ち良いアニメーションや，ワクワクする表現を意識
- Blender で作成した3Dモデルの表示や，アニメーションの実装
- パフォーマンスチューニング
  - XCode のプロファイラ (Instruments の TimeProfiler) を用いて計測
  - 不用意な値をコピーをなくす (const参照)
  - 10FPS しか出ていなかったところを，30FPS (プロジェクトの最大値) 出るように改善
- 街づくりを快適に行える機能を実装
  - 追加・変更・削除などのモードをStateパターンにより実装
  - Undo/Redo をCommand パターンで実装
  - 街データのスナップショットを取る仕組みを実装

### 株式会社gloops (201404 - 201601)

#### ソーシャルゲームの運用及びイベント開発

課金系のガチャ施策や，バトル系の施策，ログインボーナス系などの施策の運用と実装を行いました．

##### 環境
- チーム規模: 20 ~ 30人ほど (うちエンジニアが5~8人)
- 役割: サーバーサイドエンジニア
- 使用技術: C#, SQL Server, ASP.NET, JavaScript (jQuery), Visual Studio, 

##### 主な業務と成果
- 新規GvGバトル (チーム戦) イベントをメインエンジニアとして設計，実装
  - DB
    - 高負荷の対策として，DBの正規化したのちに非正規化
    - インデックスの効かないクエリ（ヒープ表へのアクセス）をなくす設計
    - 実行計画を見ながら遅いクエリの改善．JOINやサブクエリの見直し
  - アプリケーション
    - SOLIDの原則を意識したイベント全体のクラス設計
    - メモリ利用率を意識した，LINQによるコレクション操作
- 既存施策の運用
- フロントエンドの開発（HTML, SCSS, JavaScript など）
  - サーバーサイドに主軸をおいていたが，リソースが足りていないフロントエンド側も積極的に開発
- 障害対応やお問い合わせ対応全般

## 学歴

東京都市大学 知識工学部情報科学科 学士

## スキル

### プログラミング言語

#### Kotlin
- 2020 ~ 2021 (1年半)
- 新規開発の際にサーバーサイドのプログラムに使用
- Gradle周りの環境構築から可能
- Androidは未経験

#### Java
- 2019 ~ 2021 (2年)
- コードリーディングと，既存コードに対する修正が可能なレベル

#### Swift 4, 5

- 2018 ~ 2020 (2年)
- 業務とプライベートのiOSアプリ開発で使用
- 1からアプリのリリースまでの経験がある

#### JavaScript (ES6)

- 2014 ~ 現在 (7年)
- エンジニア始めた当初から使っている
- 特に軸足をおいて深く掘り下げているわけではない

#### TypeScript

- 2020 ~ 2021 (1年半)
- 既存のコードに対して，追加実装，バグ修正，改善などが可能

#### React.js

- 2020 ~ 2021 (1年半)
- Component の書き方や，hooks の使用，カスタム hooks を実装などができるレベル

#### Vue.js
- 2019  (半年)
- Nuxt.js と合わせて新規サービスの開発をおこないました

#### C++11/14

- 2016 ~ 2018 (2年)
- 3Dゲーム開発で使用していたため最低限パフォーマンスを意識したコードが実装可能
- テンプレートなどもある程度は理解

#### C#

- 2014 ~ 2016 (2年)
- ASP.NET などと合わせて Webアプリケーションの追加実装，修正が可能

#### Rust

- 実務経験なし
- 調べながらコードがかけるレベル
- 個人のプロダクト開発でつかってみたり，競技プログラミングで使用

#### golang

- 実務経験なし
- 調べながらコードがかけるレベル
- ブログで使用している Hugo 周りや，ISUCONで使用

### ミドルウェア

#### SQL Server

- 2014 ~ 2016 (2年)
- 既存のDBに対して，テーブルの追加やインデックスの見直し，実行計画をみてパフォーマンスのチューニングが可能
- 1 から環境構築した経験はない

#### MySQL

- 2014 ~ 2021 (7年)
- 既存のDBに対して，テーブルの追加やインデックスの見直し，実行計画をみてパフォーマンスのチューニングが可能
- my.cnf などの設定は基本的な知識のみ

### サービス

#### AWS

- 2020 ~ 2021 (2年)
- ECS/Fargate, Aurora, ElastiCache Redis, Lambda, S3, CloudFront, EC2, Route53 などの経験あり
- VPC の作成や，IAMによるセキュリティなどは実務経験なし

#### Contenful
- 2019 ~ 2021 (3年)
- Content Model の定義などの基本的な利用が可能
- webhooks, custom editor などチームの要件に合わせて Contentful をカスタマイズ可能

#### Firebase
- 実務経験なし
- iOSアプリのバックエンドとして，Authentication，FireStore，Cloud Function などを使用

## わたしについて

### 強み
- 0 -> 1 の新規開発を多く経験
- プロダクト開発に必要なことはなんでもやるスタイル
- 好奇心が強く新しいこのに対するキャッチアップが好き
- コツコツと継続的にアウトプットできる
  - ブログを 2018.8 から週1で書き続けている

### これから伸ばしたいこと
- より低レイヤーのCSの知識
- 規模の大きいサービスに対する設計力

### 興味があること
- 良いプロダクトを良く作ること
- 低レイヤーの知識
  - 自作OS
  - コンパイラ作成
  - ネットワーク
  - アルゴリズムとデータ構造
  - etc...
- 情報検索

## 業務外活動

### ブログの執筆
毎週技術ブログを書いています．このブログは，Hugo で作成されていて，S3 と CloudFront でホスティングしています．
さくらVPSからの移行は [こちらの記事](https://blog.foresta.me/posts/migrate_blog_to_aws/) で書いています．

このブログのデザインやイラスト，HTML/CSS のコーディングや，AWSでのホスティングなどすべて自前で実装しています．
(既存のHugo のテーマなどは用いていません)

https://blog.foresta.me

### 技術書典

技術書典に共著で本を出しました．

iOS で HLS 動画の配信とダウンロードについて書いています．

https://techbookfest.org/event/tbf08/circle/5682769699012608

### iOSアプリ開発

ノミニコという，気軽に飲みに誘えるアプリの開発を担当しました．
アプリが Swift で，バックエンドにFirebase を用いています．

https://nominico.com/

### 登壇

主にLTの発表をしています．

- [なんでもLT大会 第3弾](https://itmokumoku.connpass.com/event/119460/)
  - [スライド](https://speakerdeck.com/kz_morita/buroguzhi-bi-wozhi-eruji-shu)

- [エンジニアの成長を応援する忘年LT大会2019](https://engineers.connpass.com/event/158599/)
  - [スライド](https://speakerdeck.com/kz_morita/buroguwoshu-kisok-ketahua)


### ISUCON

予選を通過したことはありませんが，ISUCON6 から毎年出場しています．
言語は golang を用いています．

参加ログはこちら

- https://blog.foresta.me/tags/isucon

### AtCoder

参加回数が少ないですが，たまに参加しています．C++やRustで解いています．

https://atcoder.jp/users/kz_morita

## その他リンク

- [Machine Learning 修了証 - Coursera](https://www.coursera.org/account/accomplishments/verify/7MDGD56J3TV6?utm_source=link&utm_medium=certificate&utm_content=cert_image&utm_campaign=sharing_cta&utm_product=course)
- [会社のTechBlog - Node.js の CPUプロファイリングでボトルネックを特定する](https://tech.uzabase.com/entry/2021/03/25/125942)
