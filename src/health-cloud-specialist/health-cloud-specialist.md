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

### ケアコーディネーションを設定する
基本的な設定が完了したら、続いてチームごとの要件を確認します。ケアコーディネータは、特定の標準的なケアをすばやく再現する方法が必要としています。糖尿病患者の標準的な目標を含むケアプランテンプレートを作成したいと思います。新しいアプリを使用して、`Diabetes Care Plan Template` (糖尿病のケアプランテンプレート) という名前のケアプランテンプレートを作成します。以下のモデルに従います。

![](data_model.png)

ケアプランテンプレートには、これらの要素がこの順序で含まれていることを確認してください。

* ケアプランテンプレートの問題
  * `High Blood Sugar` (高血圧)
  * `Sedentary Lifestyle` (座りっぱなしの生活)
  * `Lack of Diabetes Self-Care Awareness` (糖尿病のセルフケアに対する意識の低さ)
  * `Labwork` (研究職)
* ケアプランテンプレートの目標 1
  * Related Problem (関連する問題): **High Blood Sugar**
  * Name (ToDo): `Control Glucose Levels`
  * Tasks (ToDo):
    * `Order Labs` をケアコーディネータに割り当てます。
    * `Self-Care: Daily Glucose Self-Check` を患者に割り当てます。
* ケアプランテンプレートの目標 2
  * Related Problem (関連する問題): **Lack of Diabetes Self-Care Awareness**
  * Name (名前): `Diabetes Self-Care`
  * Tasks (ToDo):
    * `Schedule Education Enrollment` をケアコーディネータに割り当てます。
    * `Exercise: Daily Walk` を患者に割り当てます。

財団は、適切な食生活が、糖尿病と同時に起こっている問題だと地域社会から聞いています。追加のケアプランテンプレートを、`Care Plan Template for Nutrition Education` (栄養指導のためのケアプランテンプレート) という名前で作成します。そのケアプランテンプレートに `Nutrition Education` のケアプランテンプレートの問題を含めてください。
#### メモ
Shankar Suman に対して複数のケアプランを作成しようとしています。組織の設定で、患者に対して複数のケアプランが作成できるようにしてください。

Shankar Suman はパイロットプログラムへの 1 人目の参加者です。彼のケアコーディネータは Dania Thurayya です。Diabetes Care Plan Template に基づいて、`Diabetes Education Care Plan` という名前のケアプランを作成します。次の問題を含めてください。

* High Blood Sugar
* Sedentary Lifestyle
* Lack of Diabetes Self-Care Awareness

件名項目には `Diabetes Education Care Plan` と入力してください。Dania Thurayya をケアコーディネータとして、Shankar Suman を患者として追加してください。

次に、Nutrition Education のケアプランテンプレートに基づいて、`Nutrition Education` という名前のケアプランを Shankar に作成します。件名には `Nutrition Education` と入力し、Dania Thurayya をケアコーディネータにしてください。

それぞれの患者ケアの 360 度ビューを得るために、Cumulus Health は分野 (ソーシャルワーカ、栄養士、専門家など) に応じてケースチームのメンバーを割り当てる方法を求めています。
Martha Ortiz と Adam Burke はケースでよく協業します。 `Diabetes Education` という名前のケースチームを作成し、Martha を Primary Care Physician の役割として、Adam を Diabetes Educator の役割としてチームに加えます。このチームを Shankar の両方のケアプランに関連づけてください。

## タイムラインビュー、患者プロファイル、社会的決定要因の設定
包括的なケアを提供するためには、チームメンバーは患者に関連する出来事を縦断的に見られる必要があります。患者のタイムラインでは、臨床医は以下を確認することができようになるはずです。

* Clinical encounters (臨床受診)
* Health conditions (健康状態)
* Medication Statements (薬剤ステートメント)
* Patient immunizations (患者免疫付与)

また、既存の Diabetes_Coaching_Session__c カスタムオブジェクトで追跡できる、糖尿病のコーチングセッションに患者がいつ参加したかについても見られるようにすべきです。チームは、糖尿病のコーチングセッションがなぜ患者のタイムラインに表示されないのかと思っています。コーチングセッションが Shankar の臨床データに追加できることを確認します。Diabetes_Coaching_Session__c カスタムオブジェクトを有効にして、患者のタイムラインに表示されるようにします。ユーザが糖尿病のコーチングセッションの上にカーソルを置いたときに、Coaching Description (コーチングの説明) 項目がタイムラインに表示されるようにしてください。

タイムラインを設定している間、ケアプランの ToDo がタイムラインに表示されることに注意してください。Shankar Suman の各オブジェクトの臨床データの例を 1 つ、次のように入力します。

* Clinical Encounters
  * Status: **Finished**
  * Start Date: choose a date and time within the last 30 days
  * End Date: 開始日から 1 時間後
  * Category: **Home Health**
  * Service Type: **Homoeopathy**
* Health Conditions
  * Condition Code: **Type 2 Diabetes**
  * Onset Period Start: 約 1 年前の日付と時間を選択してください。
* Medication Statement
  * Medication: **Metformin**
  * Status: **Completed**
  * Start Date: 過去 30 日以内の日付と時間を選択してください。
* Patient Immunization
  * Vaccine Code: **Pfizer-BioNTech COVID-19**
  * Status: **Completed**
  * Vaccination Date: 過去の任意の日付と時間を選択してください。
* Diabetes Coaching Session
  * Coaching Description: `Initial coaching session, with resources and plan`
  * Session Type: **Extended**
  * Coaching Date: 本日の日付

Diabetes Education Care Plan のケアプランの下に Shankar Suman に対して以下の ToDo を追加します。

* 件名が `Education on daily management` で期日が本日より 1 週間後
* 件名が `Fasting blood glucose check` で期日が明日

Shankar のタイムラインタブを参照し、ToDo、臨床受診、健康状態、薬剤ステートメント、患者免疫付与、糖尿病のコーチングセッションのレコードが表示されていることを確認します。

ケアコーディネータは、大切な情報を素早く見つけるために、患者の情報のスナップショットビューを必要としています。C患者カードを設定して、参加者に関する以下の関連情報を表示します。組織内には、すでに非アクティブな設定レコードがいくつかあります。それらを自由に使ってください。

* Address
* Contact Preferences
* Medications
* Conditions
* Insurance Plan
* Member Id
* Allergies

ケアコーディネータは患者に関連する様々な人々とコミュニケーションをとります；。Shankar の人間関係を追跡するため、世帯と適切なロールを設定します。それらの個人のレコードは既にシステムに存在しますが、Shankar とまだ関連づけられていません。(Shankar を患者のロールで自身の世帯に関連づけることを忘れないでください。) 以下に対してリレーションを設定します。

* **Karpani Burman** (spouse / 配偶者) 
* **Get Cloudy Consulting** (employee / 従業員)
* **Anna Jones**
  * Role: `Transportation Coordinator`
  * Inverse Role: `Patient`

ケアコーデネーションの土台はほぼ全て整っています。最後の課題は、患者の健康に影響を与える社会経済的な要因を財団がすべて理解することです。プログラム参加への重要な障壁の 1 つが交通手段であることをチームは既に知っています。プログラムチームは、この障壁を克服するための介入策をブレインストーミングしました。このソリューションをモデル化するるために、`Transportation Program` という名前のケア介入種別と、`Inadequate Transportation` という名前のケア障壁種別を作成します。両方のレコードを有効にしてください。

Shankar Suman にケア障壁のエントリを作成することで新しい機能をデモします。

* Tab (タブ): Social Determinants (社会的決定要因)
* Name (名前): `No Automobile` (自動車を保有していない)
* Type (ケア障害種別): **Inadequate Transportation** (交通手段の不足)
* Start and End Dates (開始日と終了日): 任意の日付を入力してください

最後に、以下の名前で 2 つの介入を追加します。
* `Call patient to arrange transportation` (移動を手配するために患者に電話する)
* `Provide public transportation resources` (公共交通機関の情報を提供する)

## ケアプログラムを設定する
財団は、ケアプログラムの提供を標準化することを目標としています。チームは、患者の転帰を改善するためのケアプログラムの例を見たいと考えています。`Diabetes Management` という名前で、`Care Program to help patients manage diabetes conditions` という説明のあるケアプログラムを作成します。親プログラム項目は空白のままにしてください。開始日と終了日には任意の日付を入力してください。

Shankar のケアコーディネータである Dania は、彼に糖尿病のケアプログラムに登録してもらいたいと考えています。しかし初めに、チームはプログラムに参加するための対象資格と規則を設定する必要があります。以下の3つの、登録対象資格基準レコードを作成してください。

1. 名前: `Confirm Type 2 diabetes`
2. 名前: `Confirm low income household band`
3. 名前: `Confirm physician referral or prescription received`

* ケアプログラム: **Diabetes Management**
  * 登録対象資格基準: **Confirm Type 2 diabetes**
* ケアプログラム: **Diabetes Management**
  * 登録対象資格基準: **Confirm low income household band**
* ケアプログラム: **Diabetes Management**
  * 登録対象資格基準: **Confirm physician referral or prescription received**

ケアプログラムの目的に合わせて、プログラム目標を設定しましょう。チームは、糖尿病管理ケアプログラムの目標を以下のように設定しました。

* `Adhere to treatment protocol` (治療プロトコルを遵守する)
* `Maintain healthy lifestyle` (健康的なライフスタイルを維持する)
* `Exercise 30 minutes each day` (毎日30分運動する)
* `Improve quality of life` (生活の質を改善する)

プログラム参加者に特典を提供しようと、チームは張り切っています。現在、いくつかの商品が利用可能です。以下の商品を Diabetes Management のケアプログラムに関連付けてください。

* 名前: `Monthly consultation with a nutritionist`
  * 商品: **Nutritionist Services**
* 名前: `Weekly coaching with care coordinator`
  * 商品: **Coaching**

このプログラムは、まず 2 つのプロバイダーから展開されます。次のステップは、ケアプログラム提供者を設定することです。以下の詳細に基づいて 2 つのケアプログラム提供者レコードを作成してください。

|名前|アカウント(取引先)|ケアプログラム商品|
|-|-|-|
|Cumulus Health Nutritionist|Cumulus Health Physician Group|Monthly consultation with nutritionist|
|Cumulus Health Wellness Clinic|Cumulus Health Hospital|Weekly coaching with care coordinator|

リーダーシップチームは、特定のケアプログラムへの募集活動をどのように追跡すればよいかと考えています。`Initial outreach: radio spots` という名前のキャンペーンを作成します。ケアプログラムのキャンペーンを定義し、**Initial outreach: radio spots** キャンペーンと Diabetes Management ケアプログラムを関連付けます。

次に、同意ドキュメントをケアプログラムに関連付けて、参加者の同意を追跡できるようにします。Diabetes Management ケアプログラムに対して、以下のデータ使用目的レコードを作成します。

* 名前: `Diabetes Management Care Program Consent Forms`
* 目的 (ケアプログラムオブジェクトを選択): **Diabetes Management**

**注意:** データ型として、目的項目でケアプログラムを選択する必要があります。

次の認証フォームを作成します。

* 認証フォーム名: `Authorization to Disclose PHI`
* リビジョン番号: `1.0`
* 有効開始日: 本日から一週間後の日付
* 有効終了日: 本日から一年後の日付
* 署名が必要: **True**

次の認証フォームテキストを作成します。

* 名前: `Authorization to Disclose PHI`
* 認証フォーム: **Authorization to Disclose PHI**
* コンテンツドキュメント: **AUTHORIZATION TO DISCLOSE PERSONAL AND HEALTH INFORMATION**
* ロケール: ユーザのロケールレコードに合わせます
* 有効: **True**

Authorization to Disclose PHI の認証フォームを編集します。

* デフォルトの認証フォームテキスト: **Authorization to Disclose PHI**

次の情報で認証フォームデータの使用レコードを作成します。

* 名前: `Authorization to Disclose PHI`
* 認証フォーム: 作成した認証フォームを選択します
* データ使用目的: 作成したデータ使用目的を選択します

財団は、これまでの作業をとても心強く思っており、ケアプログラムへの参加と同意ですべてがうまくいくことを望んでいます。
最初のステップは、参加者を迅速に登録するために、プログラムへの登録の標準的な自動化を調整することです。**Program Enrollment** という名前のフローを使用したアクションを作成します。作成したアクションは患者のレコードページで利用できるようにしてください。

* 表示ラベル: `Enroll in Care Program`
* 名前: `Enroll_in_Care_Program`
* 説明: `Enroll in Program flow with care plan selection`

デモでは、Shankar の登録の自動化をユーザがどのように素早く起動できるかを示しましょう。患者レコード上の自動化を使用して、Shankar をDiabetes Management のケアプログラムに登録してください。

* 商品を選択してください
  * **Monthly consultation with a nutritionist**
  * **Weekly coaching with care coordinator**
* 商品に関連する提供者を選択してください

登録を完了し、同意の取得に進みます。同意書を確認し、(これはデモであることを忘れないでください)、署名欄で署名し、同意を完了します。
## プロバイダのプロファイルを定義する

## ケア要請と利用管理を設定する
Cumulus Health には、ケアの妥当性をレビューするステップを合理化するという第二の目的があります。以前のシステムには十分な情報がなく、ビジネスニーズが変わったときに再設定するのは簡単ではありませんでした。あなたの目標は、Health Cloud がどのように合理化された利用管理を提供するかを実証することです。

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