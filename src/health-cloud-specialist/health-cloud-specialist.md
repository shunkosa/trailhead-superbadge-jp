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

### システム管理をレビューする

早速、プロジェクトに参加して設定を始めます。まず、各地域のケアコーディネータ用のカスタムプロファイルを作成します。 **Health Cloud Admin** プロファイルをコピーして、新しいプロファイル `Care Coordinator Admin` を作成します。Care Coordinator Admin プロファイルで、新しいユーザ `Dania Thurayya` を作成します。Dania に以下の権限セットを割り当ててください。
* Health Cloud Foundation
* Health Cloud Permission Set License

適切なオブジェクトに、`Patient` (患者) という名前のカスタムレコードタイプを作成します。説明には `Represents an individual patient or participant` (個人の患者または参加者を表す) と入力します。レコードタイプは Care Coordinator Admin、Health Cloud Admin、システム管理者プロファイルで利用可能にしてください。Health Cloud で個々の患者を表現する方法はたくさんあります。ベストプラクティスに従い患者のレコードタイプを作成してください。

チームはリレーションのマッピングを使用したくなるでしょう。作成したレコードタイプをカスタムメタデータで正しく設定します。新しい機能のデモンストレーションのために、`Shankar Suman` の患者レコードを作成します。

これまでの経験から、コンソールビューはチームが効率的にケアを提供するのに役立つと判断しました。コンソールナビゲーションを使用して、Care Coordination Console という名前の Lightning アプリケーションを作成します。これらのプロファイルに対してアプリケーションを有効にします。

* Care Coordinator Admin
* System Administrator
* Health Cloud Admin

アプリケーションのナビゲーション項目に以下を含めます。
+ Home (ホーム)
* Patients (稲妻アイコン)
* Leads (リード)
* Accounts (取引先)
* Cases(ケース)
* Care Plan Templates

**Patient Console with Pinned Leftbar** の Lightning レコードページをコピーして、`Care Coordination Account Page` という名前でレコードページを作成します。API 参照名が `Care_Coordination_Account_Page` となっていることを確認してください。このページを Care Coordination Console アプリケーションのデフォルトとして設定します。

## ケアコーディネーションを設定する
基本的な設定が完了したら、続いてチームごとの要件を確認します。ケアコーディネータは、特定の標準的なケアをすばやく再現する方法が必要です。糖尿病患者の標準的な目標を含むケアプランテンプレートを作成したいと思います。新しいアプリを使用して、`Diabetes Care Plan Template` (糖尿病のケアプランテンプレート) という名前のケアプランテンプレートを作成します。このモデルに従ってください。
以下のモデルに従います。

![](data_model.png)

ケアプランテンプレートには、これらの要素がこの順序で含まれていることを確認してください。

* ケアプランテンプレートの問題

* ケアプランテンプレートの目標 1
  * High Blood Sugar
  *

* ケアプランテンプレートの目標 2


## タイムラインビュー、患者プロファイル、ソーシャルデターミナントの設定

## ケア要請と利用管理を設定する
Cumulus Health には、ケアの妥当性をレビューするステップを合理化するという第二の目的があります。以前のシステムには十分な情報がなく、ビジネスニーズが変わったときに再設定するのは簡単ではありませんでした。あなたの目標は、Health Cloud がどのように合理化された利用管理を提供するかを実証することです。

Start by configuring  request customization. Create a Care Request record type with the label `Diabetes Care` (糖尿病の治療). Associate it with the Care Request's page layout. Make sure the record type is active and available for the user profiles you set up. Repeat these steps for the additional objects, using the Diabetes Care label for each object:

ケア要請のカスタマイズ設定から始めます。`Diabetes Care` (糖尿病の治療) という表示ラベルでケア要請のレコードタイプを作成します。それを Care Request (ケア要請) のページレイアウトと関連づけます。レコードタイプは有効にし、これまでに設定したプロファイルで利用可能になるようにしてください。追加のオブジェクトについてもこの手順を繰り返し、各オブジェクトにも Diabetes Care の表示ラベルを使用します。

* Caes (ケース) : Care Request のページレイアウトに関連づけます。
* Care Diagnosis (ケア診断) : Care Diagnosis のページレイアウトに関連づけます。
* Care Request Item (ケア要請品目)  Care Request Item のページレイアウトに関連づけます。

ケア要請の設定で、`Diabetes Care` という表示ラベルと、ケア要請種別を `Service Request` としたケア要請の構成レコードを作成します。Care Request Item と Care Diagnosis オブジェクトを利用可能にしてください。

新しいケア要請の構成の作成が完了したら、**Care Coordination Console Home** ページ (前の Challenge で作成したページ) に **Create Care Request** (ケア要請の作成) コンポーネントを追加します。

Care Coordination Console Home ページからケア要請を作成することで新しい機能をデモしましょう。次の情報を入力します。

* Case (ケース):
  * Case Origin (ケース 発生源): **Phone** (電話)
* Care Request (ケア要請):
  * Member (メンバー): **Shankar Suman**
  * Name (名前): `Diabetes care request`
* Care Request Item (ケア要請品目):
  * Name (名前): `Blood Glucose Monitor`
* Care Diagnosis (ケア診断):
 * Name (名前): `Type 2 Diabetes`
 * Discharge Diagnosis code (退院診断コード): **E11.22, Type 2 diabetes mellitus with diabetic chronic kidney disease**
 * Modified Diagnosis code (変更済み診断コード): **E11.22, Type 2 diabetes mellitus with diabetic chronic kidney disease**
 * Diagnosis Code (診断コード): **E11.65, Type 2 diabetes mellitus with hyperglycemia**

レコードを保存し、新しいケア要請を確認してください。
## インテリジェントなセールスを使用して生産性を最大化する
医療技術企業である Vance Laboratories は、財団への主要な寄付者です。同社の支援により、Cumulus Health グローバル財団は当初の予定よりも早く成長することができました。あなたは、Vance のチームメンバ数人と何度か会話を交わし、医療技術営業におけるペインポイントを聞いてきました。あなたの洞察は次の通りです。Vance の売上が増えれば、財団の資金も増える。そこで、Health Cloud のインテリジェントなセールス機能のデモを提案することになりました。

最初のステップは在庫のロケーションの設定です。ミネソタ州から始めましょう。

* Name (ロケーション名): `Minnesota Medical Supplies`
* Location Type (ロケーション種別): **Inventory Location**
* Inventory Location (在庫のロケーション): **True**

Visitor Address (訪問者住所) は、ユーザが近くの在庫を探したり、商品の転送を依頼するのに役立ちます。訪問者住所を作成して、訪問者住所項目で選択できるようにします。

* Address (町名・番地): `7255 Minnesota 61`
* City (市区郡): `Tofte`
* State (都道府県): `MN`
* Zip/Postal Code (郵便番号): `55615`
* Country (国): `United States`
* Location Type (ロケーション種別): `Warehouse`
* Address Type (住所種別): `Mailing`

次に、在庫を定義しましょう。`Hip Prosthesis` という名前の商品を、Minnesota Medical Supplies のロケーションに対して作成します。このデモでは、在庫数量を `50`、数量測定単位を `Each` とします。

最後に、商品履行場所を作成します。

* Name (商品履行場所名): `Minnesota Hip Devices`
* Product (商品): `Hip Prosthesis`
* Fulfillment Location (履行場所): `Minnesota Medical Supplies`
* Responsible User (担当ユーザ): `Janet Campbell`
* Account (取引先): `Cumulus Health Hospital`
* Account Location (取引先所在地): `Cleveland`

Set up an action plan template to have a predefined list of tasks that med tech sales executives must execute during a surgical case visit. Create an action plan template:

アクションプランテンプレートを設定し、医療技術営業のエグゼクティブが外科症例訪問時に実行しなければならないタスクを、事前定義したリストとして管理します。次のアクションプランテンプレートを作成しましょう。

* Name (名前): `Surgical Visit`
* Action Plan Type (アクションプラン種別): **Visit Execution** (訪問実行)
* Target Object (対象オブジェクト): **Visit** (訪問)

次に **Order Authorization** フローを追加し、必須にします。Surgical Visit アクションプランてプレートを公開します。

アプリケーションのホームページ上の **My Visits** (私の訪問) コンポーネントから、外科症例訪問を作成して、**Intelligent Sales** (インテリジェントなセールス) アプリケーションのでデモをしましょう。次の情報を含めます。

* Visit Location (場所): **Minnesota Medical Supplies**
* Visit Type (訪問種別): **Replenish Hip repair devices**
* Primary Visitor (プライマリの訪問者): **Janet Campbell**
* Account to Visit (取引先): **Cumulus Health Hospital**
* Product (商品): **Hip Prosthesis**
* Product Quantity (数量): `2`
* Action Plan Template (アクションプランテンプレート): **Surgical Visit**

## 患者のデバイスを管理する
パイロットプログラムの一部として、Shankar は SmartScale を受け取ることになりました。以下の情報で納入商品レコードを作成して、デバイスを追跡する方法をデモしてみましょう。

* Asset Name (納入商品名): `Shankar Suman's SmartScale 2.0`
* Product (商品): **SmartScale 2.0**
* Account (取引先): **Shankar Suman**
* Serial Number (シリアルナンバー): `PMSS2020001`
* Unique Identifier (一意の識別子): `PM_SS_JF001`
* Description (説明): `SmartScale shipped to Shankar Suman`
* Price (価格): `$299`
* Quantity (数量): `1`

あらかじめ設定された自動化機能を使って、個々の患者への機器登録を効率化したいです。患者のレコードページに、**Register Device and Create Shipping Request** (デバイスの登録と出荷依頼の作成) というクイックアクションを追加します。Shakar の SmartScale の出荷依頼を作成してください。

機器の出荷情報として次の情報を利用します。

* Street: `1 Market Street`
* City (市区郡): `San Francisco`
* State/Province (都道府県): `CA`
* ZipCode (郵便番号): `94105`
* Country (国): `US`

Shankar が体重計を受け取った後、彼のケアコーディネーターは Shankar のレコードページの **Remote Monitoring** (リモート監視) タブでケア指標目標を作成することができます。次の情報を入力して、Shankar のケア指標目標を追加してください。

* Name (名前): `Individual Body Weight - Shankar Suman`
* Patient (患者): `Shankar Suman`
* Type (種別): MAX (最大)
* Numeric Value (数値): `210`
* Code (コード): `Body Weight Code Set`
* Units of Measure (測定単位): **lbs**
* Start Date (開始日): 本日から1ヶ月前の日付
* End Date (終了日): 本日から1年後の日付

最後に、患者のレコードの Remote Monigoring (リモート監視) タブの下にリモート監視グラフを表示し、デバイスデータに簡単にアクセスできるようにします。リモート監視グラフのデモを行うため、いくつかのケア観察レコードを作成してください。

やりました！デモは大成功でした。おめでとうございます。この成果は、財団を成長させ、世界中の地域社会にポジティブな健康成果をもたらすでしょう。
## Challenge

## 補足とヒント