# Health Cloud Specialist
[![](https://img.shields.io/badge/-view%20on%20gitbook-blue?logo=markdown)](https://shunkosa.gitbook.io/trailhead-superbadge-jp/health-cloud-specialist) [![](https://img.shields.io/badge/-view%20on%20github-black?logo=github)](https://github.com/shunkosa/trailhead-superbadge-jp/blob/master/src/health-cloud-specialist/health-cloud-specialist.md)
* Trailhead のスーパーバッジ、[Health Cloud Cloud Specialist](https://trailhead.salesforce.com/content/learn/superbadges/superbadge-health-cloud-specialist) の日本語訳(**非公式**)です。
* 各カスタマイズ要素のラベル部分には補足として日本語を括弧内に記載している場合がありますが、正解チェックは英語のラベルを元に行われるため、実際のチャレンジには日本語表記を含めず、英語表記のみを使用して行って下さい。また、チャレンジ前にユーザと組織の言語・ロケールを英語に切り替えておくことを推奨します。

---
## このスーパーバッジを取得するためにすること
* Health Cloud のユーザ、プロファイル、権限を作成します。
* Health Cloud において Lightning アプリケーションビルダーを使用します。
* ケアコーディネーションへの洞察を示します。
* 患者の 360 度ビューを表示します。
* 医療技術セールスチームを強化するための戦略を作成します。

## このスーパーバッジでテストする概念
* Health Cloud の設定とセットアップ
* ケアコーディネーション
* ケアプログラム
* 提供者
* 相互運用性
* 利用管理
* インテリジェントなセールス
* デバイス管理
* セキュリティ

所用時間 : 推定 8 時間 

## 事前準備とメモ

### Health Cloud を備える Developer Edition 組織の作成
このスーパーバッジを完了するには、Salesforce Health Cloud、専用の設定、サンプルデータを含む特別な Salesforce 環境が必要です。特別に Health Cloud が有効化された Developer Edition 組織に最近サインアップした場合でも、このスーパーバッジのために新しい組織にサインアップしてください。**また、Health Cloud 管理パッケージは 30 日後に期限切れになることに注意してください。**

1. [こちら](https://trailhead.salesforce.com/en/promo/orgs/healthcloudspecialist)から、Health Cloud を備える無料のテスト環境にサインアップします。
2. フォームに入力します。Email の欄には、有効な電子メールアドレスを入力します。Username の欄には、メールアドレス形式の一意のユーザ名を入力しますが、有効な電子メールアカウントと一致している必要はありません。(例: `@hc4ever.sample.com`) 
3. フォームに入力したら、**Sign Me Up**  (サインアップ) をクリックします。確認メッセージが表示されます。
4. ようこそメールを受信 (数分かかる場合があります) したら、それを開き、**Verify Account** (アカウントを確認) をクリックします。
5. パスワードと秘密の質問を設定して、登録を完了します。**ポイント**: 後で簡単にアクセスできるように、ユーザ名、パスワード、およびログイン URLを書き留めます。
6. Health Cloud が有効化された Developer Edition にログインされた状態になります。

次に、新しい Developer Edition 組織を Trailhead に接続します。

1. Trailhead アカウントにログインしていることを確認してください。
2. このページの下部にある **Challenge** セクションで、選択リストから **Log into a Developer Edition** (Developer Edition にログイン) を選択します。
3. ログイン画面で、先ほど設定した Developer Edition のユーザ名とパスワードを入力します。
4. Allow Access? (アクセスを許可しますか？) の画面で、**Allow** (許可) をクリックします。
5. Want to connect this org for hands-on challenges? (この組織をハンズオンの Challenge 用に保存しますか？) の画面で、**Yes! Save it** (はい、保存します) をクリックします。Challenge のページにリダイレクトされ、新しい Developer Edition を使用してこのスーパーバッジを獲得する準備が整います。
6. 専用の管理パッケージがインストールおよび有効化された Salesforce 組織ができたので、準備完了です。

### 備考
* Challenge を始める前に、[このスーパーバッジの Help 記事](https://trailhead.salesforce.com/help?article=Health-Cloud-Specialist-Superbadge-Trailhead-Challenge-Help)を確認してください。このドキュメントは、このスーパーバッジを完了させるのに役立つリソースを見つけたり、よくある質問をサポートしたりするのに役立ちます。
* 他のスーパーバッジと同様に、正しく設定するための要件が詳しく説明されています。ブラウザのタブを 2 つ使用することをお勧めします。1 つはシナリオを進めるために表示し、もう 1 つは Challenge をチェックするために表示します。これにより、スーパーバッジのコンテンツをスクロールする手間を省くことができます。

## ユースケース
医療イノベーションのリーダーである Cumulus Health は、2 型糖尿病の発生を減少させるための重要なインフルエンサーとなることを約束しました。新設された Cumulus Health グローバル財団 (以下、財団) は、世界中で個人のウェルビーイングを促進し、健康格差を減らすことを目的としています。

主な取り組みの 1 つとして、新しい健康アドボカシー・教育プログラムによる、個人の教育と能力向上の支援があります。この財団は、そのビジョンを実現するために、いくつかの異なる地域のコミュニティや医療従事者と提携しています。そのためには、世界各地のプログラムをサポートできるシステムが必要です。来月には、糖尿病予防・教育プログラム (Diabetes Prevention and Education Program, DPEP) の効果を実証するためのパイロットプログラムを展開したいと考えています。

各地域のサイトには、主任ケアコーディネータとパイロットプログラムの患者たちがいます。あなたは、新しいプログラムのニーズを満たすために、新しい Health Cloud の実装が適切に設定されていることを確認する責任があります。一部の設定はすでに実施されていますが、チームはそれが最も効果的な方法で機能しているかどうか確信が持てていません。また、可能な限り **FHIR R4 に準拠した医療データモデル** を活用するなど、Health Cloud を使用するための最新のベストプラクティスに従っていることを確認したいと考えています。チームの要件を確認し、プログラムのロールアウトをサポートするための戦略を定義しましょう。

## ビジネス要件

## Challenge

## 補足とヒント