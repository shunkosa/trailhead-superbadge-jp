# Financial Services Cloud Specialist
[![](https://img.shields.io/badge/-view%20on%20gitbook-blue?logo=markdown)](https://shunkosa.gitbook.io/trailhead-superbadge-jp/fsc-specialist) [![](https://img.shields.io/badge/-view%20on%20github-black?logo=github)](https://github.com/shunkosa/trailhead-superbadge-jp/blob/master/src/fsc-specialist/fsc-specialist.md)
* Trailhead のスーパーバッジ、[Financial Services Cloud Specialist](https://trailhead.salesforce.com/content/learn/superbadges/superbadge-fsc-specialist) の日本語訳(**非公式**)です。
* 各カスタマイズ要素のラベル部分には補足として日本語を括弧内に記載している場合がありますが、正解チェックは英語のラベルを元に行われるため、実際のチャレンジには日本語表記を含めず、英語表記のみを使用して行って下さい。また、チャレンジ前にユーザと組織の言語・ロケールを英語に切り替えておくことを推奨します。

---
## このスーパーバッジを取得するためにすること
* Financial Services Cloud のユーザ、プロファイル、権限を作成します。
* Financial Services Cloud において Lightning アプリケーションビルダーを使用します。
* リレーション管理を使用して顧客ポートフォリオへの洞察を示します。
* ライフイベントを用いて顧客の 360 度ビューを表示します。
* アクションプランを用いてエンゲージメントのための戦略を作成します。
* リードと商談を扱います。
* ドキュメントの追跡と支援について顧客のオンボーディングを支援します。
* レポートで主要な洞察を表示します。

## このスーパーバッジでテストする概念
* Financial Services Cloud の設定とユーザ管理
* リレーション管理と積み上げ集計
* ライフイベント
* アクションプラン
* リードと紹介 (リファラル)
* ドキュメントの追跡と承認
* レポーティング

所用時間 : 推定 10 時間 

## 事前準備とメモ
* 詳細なリソースとドキュメントについては、この [Help 記事](https://trailhead.salesforce.com/ja/help?article=Financial-Services-Cloud-Specialist-Trailhead-Challenge-Help)を参照してください。
* このスーパーバッジで利用される用語のいくつかは、UI に表示される設定上の名称と完全に一致しない場合があります。これは、Salesforce の機能に関する知識と、ビジネス上のニーズを満たす正しい機能を選択する能力をテストするためです。
* **ポイント**: メタデータおよびレコードデータを設定するために示されている値は手動で入力せず、コピー・ペーストしてください。これにより、Challenge の失敗を引き起こすタイプミスやスペルミスの可能性が減ります。

### Financial Services Cloud を備える Developer Edition 組織の作成
このスーパーバッジを完了するには、Salesforce Financial Services Cloud、専用の設定、サンプルデータを含む特別な Developer Edition 組織が必要です。特別に Financial Services Cloud が有効化された Developer Edition 組織に最近サインアップした場合でも、このスーパーバッジのために新しい組織にサインアップしてください。**また、管理パッケージは 30 日後に期限切れになることに注意してください。**

1. [こちら](https://developer.salesforce.com/promotions/orgs/fscspecialist)から、Salesforce Financial Services Cloud を備える無料の Developer Edition 組織にサインアップします。
2. フォームに入力します。Email の欄には、有効な電子メールアドレスを入力します。Username の欄には、メールアドレス形式の一意のユーザ名を入力しますが、有効な電子メールアカウントと一致している必要はありません。(例: `yourname@fsc4ever.sample.com`) 
3. フォームに入力したら、**Sign Me Up**  (サインアップ) をクリックします。確認メッセージが表示されます。
4. ようこそメールを受信 (数分かかる場合があります) したら、それを開き、**Verify Account** (アカウントを確認) をクリックします。
5. パスワードと秘密の質問を設定して、登録を完了します。**ポイント**: 後で簡単にアクセスできるように、ユーザ名、パスワード、およびログイン URLを書き留めます。
6. Financial Services Cloud が有効化された Developer Edition にログインされた状態になります。
7. 私のドメインを有効化し、**すべてのユーザにデプロイ**します。
8. 複数のリレーショングループを有効化します。

次に、新しい Developer Edition 組織を Trailhead に接続します。

1. Trailhead アカウントにログインしていることを確認してください。
2. このページの下部にある **Challenge** セクションで、選択リストから **Log into a Developer Edition** (Developer Edition にログイン) を選択します。
3. ログイン画面で、先ほど設定した Developer Edition のユーザ名とパスワードを入力します。
4. Allow Access? (アクセスを許可しますか？) の画面で、**Allow** (許可) をクリックします。
5. Want to connect this org for hands-on challenges? (この組織をハンズオンの Challenge 用に保存しますか？) の画面で、**Yes! Save it** (はい、保存します) をクリックします。Challenge のページにリダイレクトされ、新しい Developer Edition を使用してこのスーパーバッジを獲得する準備が整います。

専用の管理パッケージがインストールおよび有効化された Salesforce 組織ができたので、準備完了です。

### 備考
Challenge を始める前に、[このスーパーバッジの Help 記事](https://trailhead.salesforce.com/ja/help?article=Financial-Services-Cloud-Specialist-Trailhead-Challenge-Help)を確認してください。このドキュメントは、このスーパーバッジを完了させるのに役立つリソースを見つけたり、よくある質問をサポートしたりするのに役立ちます。

## ユースケース
Cumulus Global Bank (CGB) は、パーソナライズされたバンキングのリーダーです。同行は、顧客を理解し、ハイタッチな顧客体験を提供するためのプロセスに磨きをかけるために、多大な努力を重ねてきました。同行は最近、その取り組みをサポートし、継続的な成長を促進するために Salesforce Financial Services Cloud (FSC) を導入しました。

CGB は、銀行のチームに力を与え、顧客が期待するパーソナライズされたプロアクティブなサービスを提供する FSC に感銘を受けています。さらに重要なことは、顧客のエンゲージメントを向上させながら、情報への適切なアクセスを担保する必要があるということです。また、CGB は手動のプロセスを合理化し、より良い洞察を得たいと考えています。

あなたは、CGB の FSC スペシャリスト (FSC 経験のある Salesforce システム管理者) として活躍することになります。Financial Services Cloud を特徴とする Salesforce インスタンスが、CGB が必要とする機能を提供できるようにすることを担当します。また、資産運用アドバイザー、パーソナルバンカー、住宅ローン融資担当の業務をハンズオンでサポートすることも多くあります。そのような場合は、必要に応じて各ペルソナでログインして要件を満たしてください。

## 主要なステークホルダ
* Ryan Dobson - 資産運用アドバイザー
* Hank Burton - パーソナルバンカー
* Sue Berry - 住宅ローンの融資担当
* Rachel Adams - 顧客
* Scott Adams - 顧客
* Vivian Torres - 顧客

## ビジネス要件

### 設定の更新
最初の目標は、チームメンバーの情報への適切なアクセスを設定することです。既存の FSC Admin プロファイルをコピーして、新しい `FSC Personal Banker` プロファイルを作成します。FSC Personal Banker プロファイルが Financial Account Transactions (金融口座取引オブジェクト) にフルアクセス権限を与えます。次に、FSC Admin プロファイルを複製して、新しい `FSC Mortgage Officer` プロファイルを作成します。このプロファイルは、Financial Account Transactions にはアクセスできませんが、Loan Application Liabilities (ローン申込債務オブジェクト) と Loan Applicant Liabilities (ローン申込人債務オブジェクト) にはフルアクセスできるようにします。

Hank Burton と Sue Berry のユーザを設定し、各ユーザに適切なプロファイルを割り当てます。(Ryan のユーザと、カスタムの FSC Wealth Advisor のプロファイルは既に存在していることに注意してください。) ユーザを作成した後、以下の権限セットを Hank と Sue に適用します。

* Document Checklist
* ActionPlans
* Financial Services Cloud Standard
* Relationship Manager Access
* FSC Insurance

Hank は、富裕層の顧客レコード上に特定の情報とコンポーネントを表示させたいと考えています。管理者として、あなたは Hank を支援するために、後日別のページレイアウトを追加することになるでしょう。今のところは、個人取引先に `Gold Client` という新しいレコードタイプを作成し、その新しいレコードタイプをカスタムメタデータ型に適切にマッピングすることで、これを実現できることはご存知でしょう。

#### Lightning アプリケーションとページ
次のタスクは、資産運用マネージャのために Lightning アプリケーションを設定することです。このアプリケーションは、アドバイザリチームのためのコラボレーションツールと生産性向上ツールで、顧客の信頼を構築するのに役立ちます。`FSC Wealth Management` という名前の新しいアプリケーションを作成し、標準の Wealth Management アプリケーションと同じタブが含まれるようにします。

資産運用アドバイザーチームは、Wealth Management Home ページ上で、トップの紹介者が誰なのかを確認したいと考えています。標準の Wealth Home Page に基づいて、カスタムの `FSC Wealth Home` ページを作成します。チームは、アプリケーションを起動するたびにホームページ上でトップ紹介者を確認したいと考えています。 **Referrals Top Referrers** コンポーネント (私のドメインがリリースされた後に利用可能なカスタムの Lightning Web コンポーネント) を FSC Wealth Home ページに追加します。この新しいページがアプリケーションのホームページであり、カスタムの FSC プロファイル群からアクセスできるようにします。

チームは、カスタムの FSC プロファイル群とシステム管理者プロファイルからアクセス可能な、新しい `FSC Lending` アプリケーションを確認したいと考えています。新しいアプリケーションは、以下のタブを表示する必要があります。

* Home (ホーム)
* Accounts (取引先)
* Contacts (取引先責任者)
* Leads and Referrals (リード)
* Assets and Liabilities (資産と負債)
* Analytics (分析)
* Financial Accounts (金融口座)
* Financial Goals (投資運用ゴール)
* Financial Holdings (保有銘柄)
* Loan Applicants (ローン申込人)
* Residential Loan Applications (住宅ローン申込)
* Reports (レポート)

カスタムの `FSC Lending Home` ページを作成します。それが FSC Lending アプリケーションのホームページとなり、カスタムの FSC プロファイル群からアクセスできるようにしてください。ホームページには、以下のコンポーネントを表示する必要があります。

* Referrals Made Summary
* Referrals Assigned List
* Task Card
* Opportunity Card

また、取引先のレコードページ上で重要なライフイベントを追跡し可視化することで、パーソナルでタイムリーな顧客エンゲージメントを提供したいと考えています。**ClientRecordPage4** Lightning レコードページをコピーし、`FSC Client Record Page` という名前を付け、適切な修正を行ってください。レコードページを、**FSC Wealth Management**、**FSC Retail Banking**、**FSC Retail Banking Console**、および **FSC Lending** アプリケーションのデフォルトとして割り当てます。

チームの次の要望は、バンカーの住所更新プロセスを合理化することです。FSC の専門家であれば、このプロセスを容易にするために、すぐに使えるフロー機能があることをご存知でしょう。住所更新 (Address Update) リクエストを効率的に処理するために、自動化機能を確認して有効化します。適切な取引先ページレイアウトにクイックアクションボタンがあることを確認してください。

### 個人取引先を扱う
設定が完了すると、チームが魔法を働かせるのを飛び込んで助けることができます。

Rachel Adams は、15 年以上にわたって CGB で資産を保有しています。Rachel は、息子である Scott Adams との共同当座預金口座を開設したいと考えています。Rachel は、息子のための当座預金口座を開設するためにバンカーの Hunk Burton に会います。Hunk としてログインし、Scott のための新しい個人取引先を作成し、種別を **Customer - Direct** とし、Adams の Household (世帯) に彼を追加します。Hank は、Scott Adams に対して、10,000 ドルの新しい Financial Account (金融口座) `Primary Checking Account` (レコードタイプを Bank Accounts として) を作成します。Rachel Adams を **Joint Owner** (共同所有者) として追加します。

Scott はパートナーの Vivian Torres と将来を計画しています。彼は Hank に Vivian を新規顧客として紹介します。彼らの銀行業務をより良くサポートするために、Hank は新しく **Torres-Adams Household** の世帯レコードを作成し、Vivian の個人取引先レコードを作成します。Torres-Adams Household が Vivian と Scott の両方の **Primary Group** となるようにしてください。また、Vivian が世帯の **Primary Member** となるようにします。

Hank は、Vivian の退職後の計画について詳しく知るための打ち合わせを設定します。Hank は、老後のための投資について話し合ってもらうため、Vivian をファイナンシャルアドバイザーの Ryan Dobson に紹介します。Ryan は、Vivian の退職後のゴールについて話し合うために、Vivian と会うことを計画します。Ryan Dobson としてログインし、新しいゴール、`Vivian's Retirement` を設定します。このゴールは開始せず (Not Started)、種別は **Retirement** にしてください。

彼らが行っている他の将来の計画と一緒に、Vivian と Scott は家を購入したいと考えています。2 人とも、新しい家を購入するための銀行口座を保有しています。FSC の専門家であるあなたは、Torres-Adams Household に Vivian と Scott の口座を集約して表示することが可能であることを知っています。この情報は、Vivian と Scott が住宅ローンを組むためにどれくらいの金額を支払うことができるのかを知るのに役立ちます。Ryan Dobson は Vivian の銀行口座を `Vivian Savings Account` という名前で残額を $25,000 として作成し、種別を **Savings** (貯蓄) に設定します。Vivian の銀行口座と Scott の当座預金口座が自動的に **Total Bank Deposits** (銀行預金総額/口座総額)に積み上げ集計されるようにしてください。

銀行は、アソシエイトの Kotori Mizono を雇うことになりました。アソシエイトとして、Kotori はすべての金融口座を管理することができますが、リレーションシップの特定の側面を参照することはできません。**Personal Banker** プロファイルをコピーして、**FSC Associate Banker** プロファイルを作成します。**ClientRecordPage4** Lightningレコードページをクローンし、`FSC AB Client Record Page` という名前をつけ、すべての FSC アプリケーションにおいて FSC Associate Banker プロファイルに対して (リレーションシップマップコンポーネントの) Related Accounts (関連取引先) と Related Contacts (関連取引先責任者) への参照を制限してください。Kotori 用の新しいユーザーを作成し、以下の設定を完了します。

* **Salesforce User** ライセンスと **FSC Associate Banker** プロファイルを割り当てます。
* 権限セットライセンス **Financial Services Cloud Standard** を割り当てます。
* 権限セット **Financial Services Cloud Standard** と **Personal Banker Access** を割り当てます。

Kotori Mizono としてログインし、リレーションシップマップ (リレーションの対応付け) とグループビルダーで、Related Accounts (関連取引先) と Related Contacts (関連取引先責任者) が表示されていないことをテストしてください。

Scott と Vivian の住宅購入計画は急速に進んでいます。Hank は不動産業者の Carolyn Kane を追加したいと考えており、その結果 Sue Berry は主要な関係者をすぐに参照できるようになります。リレーションシップマップを使用して、不動産業者の Carolyn を表示しましょう。Torres-Adams Household と不動産業者 `Caroline Kane - Lakeshore Realty` との間に、取引先間リレーションを作成して下さい。関連ロールは、`Realtor` (Torres-Adams Household から見て) と `Customer` (Caroline Kane - Lakeshore Realty から見て) としてください。

また、Scott と Vivian は、家の購入にあたり弁護士を必要としており、Scott の母親である Rachel Adams は、彼女の弁護士である Ivan M. Kohl と一緒に仕事をしてほしいと考えています。Vivian は弁護士として Ivan に依頼して物件の取引を成立させます。Torres-Adams Household に関連する取引先責任者として Ivan を追加し、相互ロール (関連ロール) に **Lawyer** (弁護士) を設定します。Ivan の取引先責任者と関連ロールの Lawyer は既に作成されていることに注意してください。

### ライフイベント
Scott と Vivian の新居は湖の上にあり、2 人はボートを購入する計画を立てたいと考えています。新しい Person Life Event (個人ライフイベント) の種別として **Boat** を追加します。 次に、その新しい個人ライフイベントの種別に対して画像をアップロードします。ボートのライフイベント用の SVG ファイルをこちらの [boat.zip](https://developer.salesforce.com/files/boat.zip) からダウンロードしてください。

これで Ryan は新しいライフイベントを作成することができます。Ryan としてログインし、`Ski Boat` という名前で Scott Adams に新しいライフイベントを作成します。(イベント日付は任意の日付で構いません。)

### アクションプラン
アクションプランを使用すると、金融口座のオンボーディングやケースの解決などのプロセスにおいて、コンプライアンスを確保し、一貫した顧客エンゲージメントを提供することができます。FSC のスペシャリストとして、**Action Plans**、**Document Checklist**、および **Financial Services Cloud Standard** の権限セットが CGB の FSC ユーザに割り当てられていることを確認してください。Wealth Advisor (資産運用アドバイザー) は、テンプレートに変更を加えることはできませんが、アクションプランを取引先または商談に割り当てることはできます。Action Plan Templates (アクションプランテンプレート) のタブが FSC Wealth Management アプリケーションに表示され、**Action Plans List - Financial Services Cloud** コンポーネントがアプリケーションに割り当てられた個人取引先ページで表示されるようにしてください。

Ryan は、Scott の "Boat (ボート)" ライフイベントから直接アクションプランを作成できるようにしたいと考えています。FSC のスペシャリストとして、`Bank Loan Opportunity` という名前のアクションプランテンプレートを作成し、定期的なタスクを設定します。新しいテンプレートには、以下のタスクを含めてください。

|Subject (件名) |Days to Complete (完了までの日数) |Assign to (任命先) |
|-|-|-|
|Create Referral for Bank Loan|1|Action Plan Creator (アクションプラン作成者)|
|Send Bank Loan Paperwork to Customer|3|Hank Burton|
|Schedule Appointment with Customer|5|Hank Burton|

Ryan としてログインし、Scott Adams の個人取引先レコード上にある "Boat" ライフイベントから直接、`Bank Loan Opportunity` という名前の新しいアクションプランを作成します。

### リードと紹介
FSC のスペシャリストとして、あなたはチームが紹介を活用するのを支援します。まず、`Loan Referral Queue` (ローン紹介キュー) と呼ばれるリードのローン紹介割り当てのためのキューを作成し、キューのメンバーとして Hank Burton を追加します。次に、`Assign Loan Referrals` (ローン紹介の割り当て) という名前のリード割り当てルールを作成します。この割り当てルールには、Expressed Interest 項目が Personal Loan であることをチェックするルールのエントリ条件が必要です。作成したキューにエントリを割り当てます。メールテンプレートには、Loan Referral Assignment Template (ローン紹介の割り当てテンプレート) を使用できます。

FSC Lending アプリケーションを使用して、Ryan は Scott の個人ローンの紹介を記録する必要があります。アドバイザーである Ryan Dobson としてログインし、個人ローンへの新しい Expressed Interest の紹介を作成します。Internal Referrer が Ryan Dobson であることを確認してください。

Hank としてログインし、Loan Referral Queue に割り当てられた紹介を確認し、リードを受け入れてください。Hank は、Scott に融資を開始するにあたり詳細を確認するため、彼に連絡を取ります。この会話の情報を記録するために、Scott に活動を記録 (件名を "Call" とする) します。引き続き Hank としてログインし、リードを変換し、既存の Scott Adams の取引先を使用して、`Scott Adams-Boat Loan` という名前の新しい商談を作成します。

### ドキュメントの追跡と承認
ドキュメントタイプは、ビジネスプロセスを完了するために一般的に必要なドキュメントを定義します。個人向け銀行ローンのために、顧客から必要とされる各ファイルをリストアップした Document Checklist Item (ドキュメントチェックリスト項目) を作成します。当社のバンカーである Hank Burton は、ローンを組む顧客のために関連するチェックリストファイルを作成し、承認プロセスを通じてファイルを追跡することができます。Scott Adams のような顧客は、ドキュメントをアップロードし、ドキュメントが受け入れられたか拒否されたかを確認し、アップロードされたドキュメントの提出から承認までの進捗状況を追跡することができます。

商談と個人取引先のページレイアウトに、関連リストとして Document Checklist Item (ドキュメントチェックリスト項目) コンポーネントを追加します。

新しいドキュメントチェックリスト項目をドキュメントタイプに関連付けるために、個人向け銀行ローンに必要なドキュメントタイプを定義します。

次のドキュメントタイプを設定します。

* Employer Tax Form (雇用主負担税申告書)
* Pay Stub (給与明細)
* Driver License (運転免許証)
* Vehicle Title (車両の所有権証明書)

FSC Personal Banker、FSC Mortgage Officer、および FSC Wealth Advisor の各プロファイルに、ドキュメントチェックリスト項目への作成、参照、編集のアクセス権 (だけ) があることを確認してください。

Hank Burton は、Scott Adams のボート購入のための個人ローン申請に対するドキュメントチェックリストを作成する必要があります。Hank としてログインして、Employer Tax Form、Pay Stub、Driver License、Vehicle Title を含むチェックリストを作成してください。

### レポート
最後に、住宅ローンの融資担当達は、紹介活動を追跡したいと考えています。Sue Berry は、成約率の上昇にワクワクしており、トップの紹介者 (Referrer) についてもっと知りたいと思っています。また、彼女は、紹介者がどこから来て、誰が最高の紹介を作成するのかを知りたいと思っています。**WealthHome** の Lightning ページをコピーして、 `FSC Retail Banking Console Home` という名前をつけます。ページに、**[Internal] Referrals Made** と **[Internal] Referrer Score** の 2 つのレポートグラフを追加します。新しく作成したこのホームページをアプリケーションのデフォルトとして割り当てることで、FSC Retail Banking Console アプリケーションでその情報が表示されるようにしてください。

## Challenge

### Challenge 1: クイズ

### Challenge 2: 設定
要件に従い、新しく作成した組織を設定してください。Hank Burton と Sue Berry のユーザを作成し、正しいプロファイルと権限セットを割り当ててください。新しい個人取引先のレコードタイプを作成します。FSC のアプリケーションを作成し、要件に従いそれらを設定してください。

### Challenge 3: リレーション管理
シナリオに表示されているユースケースに従い、世帯と個人取引先レコード、およびそのリレーションを作成してください。

### Challenge 4: ライフイベント
FSC Retail Banking アプリケーションでライフイベントを設定します。Scott Adams に対して Ski Boat のライフイベントを作成してください。

### Challenge 5: アクションプラン
FSC Wealth Management アプリケーションで、アクションプランとアクションプランテンプレートを設定します。新しい "Bank Loan Opportunity" アクションプランテンプレートを作成してください。このテンプレートを使用して、Scott Adams の個人取引先レコード上の "Boat" ライフイベントに新しいアクションプランを作成してください。

### Challenge 6: リードと紹介
"Loan Referral Queue" という名前のキューを使用してリードの割り当てルールを作成します。Ryan Dobson としてログインし、Scott Adams に個人ローンの紹介を作成します。Hank Burton としてログインしこの紹介を商談に変換してください。

### Challenge 7: ドキュメントの追跡と承認
ドキュメントチェックリスト項目の関連リストを商談と取引先のページレイアウトに追加します。新しいドキュメントタイプを作成し、Scott Adams-Boat Loan の商談にドキュメントチェックリスト項目を作成する際に、それらのドキュメントタイプを使用してください。

### Challenge 8: レポート・ダッシュボード
FSC Retail Banking Console Home ページに、"[Internal] Referrals Made" と "[Internal] Referrer Score" の 2 つのレポートグラフを追加してください。

## 補足とヒント
### Challenge 3
* [リレーションの対応付けとグループビルダーで誰に何を表示するかを管理](https://developer.salesforce.com/docs/atlas.ja-jp.224.0.financial_services_cloud_admin_guide.meta/financial_services_cloud_admin_guide/fsc_admin_who_sees_what.htm)

### Challenge 4
* (2020/07/26 時点) Boat の画像をアップロードする箇所がなく、特にチェックされないようです。