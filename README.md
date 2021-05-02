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

ソフトウェアエンジニアとして，2014~現在に至るまで 7年の実務経験があります．
ゲーム系や，スマホアプリ，Webアプリケーションを開発をしてきました．いままで開発してきたものはすべてB2Cサービスです．

現職の株式会社ニューズピックスでは，iOSアプリエンジニアとして入社したのち，サーバーサイドやフロントエンドと幅広くプロダクト開発に携わってきました．

## 職務経歴

### 株式会社ニューズピックス (201811 - 現在)

#### 新規Webアプリケーション (UGM) の設計・開発

ユーザーがコンテンツを投稿するWebアプリケーションの新規立ち上げの設計と開発を行いました．

##### 環境
- チーム規模: 3人 (エンジニア)
- 役割: サーバーサイドエンジニア
- 使用技術: Kotlin, Jersey, Kodein, Grizzly2, Hibernate, React, Redux, TypeScript, Express, Contentful, Cypress, AWS (ECS/Fargate, Aurora, ElastiCache Redis etc...)

##### 主な業務と成果
- API Server技術選定
  - 社内で知見が溜まっている Kotlin を採用 (候補としては golang を検討していた)
- 認証基盤の設計と実装
  - NewsPicks のアカウントを利用した認証システムの実装
  - 複雑な認証フローを設計し実装
- APIサーバー開発
  - DB設計，クラス設計から担当
  - 4層のレイヤードアーキテクチャを採用
- フロントエンド開発
  - React を用いてページやコンポーネントの実装
- E2E テストの導入
  - 手動の結合テストの負荷を下げるべくE2Eテストを導入
  - Cypress と GitHub Actions を用いて，PullRequest 時にテストが走るように設定
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
- 使用技術: C#, SQL Server, ASP.net, JavaScript (jQuery), Visual Studio, 

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

## 業務外活動

### ブログの執筆
毎週技術ブログを書いています．このブログは，Hugo で作成されていて，S3 と CloudFront でホスティングしています．
さくらVPSからの移行は [こちらの記事](https://blog.foresta.me/posts/migrate_blog_to_aws/) で書いています．

このブログのデザインやイラスト，HTML/CSS のコーディングや，AWSでのホスティングなどすべて自前で実装しています．
(既存のHugo のテーマなどは用いていません)

https://blog.foresta.me

### 技術書展

技術書展に共著で本を出しました．

iOS で HLS 動画の配信とダウンロードについて書いています．

https://techbookfest.org/event/tbf08/circle/5682769699012608

### ISUCON

予選を通過したことはありませんが，ISUCON6 から毎年出場しています．
言語は golang を用いています．

## その他リンク

- [Machine Learning - Coursera](https://www.coursera.org/account/accomplishments/verify/7MDGD56J3TV6?utm_source=link&utm_medium=certificate&utm_content=cert_image&utm_campaign=sharing_cta&utm_product=course)
- [会社のTechBlog - Node.js の CPUプロファイリングでボトルネックを特定する](https://tech.uzabase.com/entry/2021/03/25/125942)
