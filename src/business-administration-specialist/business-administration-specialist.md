# Business Administration Specialist
[![](https://img.shields.io/badge/-view%20on%20gitbook-blue?logo=markdown)](https://shunkosa.gitbook.io/trailhead-superbadge-jp/business-administration-specialist) [![](https://img.shields.io/badge/-view%20on%20github-black?logo=github)](https://github.com/shunkosa/trailhead-superbadge-jp/blob/master/src/business-administration-specialist/business-administration-specialist.md)
* Trailhead のスーパーバッジ、[Business Administration Specialist](https://trailhead.salesforce.com/content/learn/superbadges/superbadge_business_specialist) の日本語訳(**非公式**)です。
* 各カスタマイズ要素のラベル部分には補足として日本語を括弧内に記載している場合がありますが、正解チェックは英語のラベルを元に行われるため、実際のチャレンジには日本語表記を含めず、英語表記のみを使用して行って下さい。また、チャレンジ前にユーザと組織の言語・ロケールを英語に切り替えておくことを推奨します。

---
## このスーパーバッジを取得するためにすること
1. 取引先のデータをクリーニングしインポートする
2. ユーザを作成しアクセス権を管理する
3. 新しいマーケティングのニーズのためにメールテンプレートを作成する
4. 新しい製品タイプのための UI ツールを設定する
5. レポートとダッシュボードを作成する
6. Chatter のツールを管理し適用する

## このスーパーバッジでテストする概念
* データのインポート
* ユーザ権限とユーザ管理
* メールテンプレート
* ユーザインタフェースの設定
* Lightning Experience のレポート・ダッシュボード
* Chatter の機能

## 事前準備とメモ
* ペンと紙を準備して、要件を読み進める際にメモを取ってください。
* このスーパーバッジ用に、新しい Trailhead Playground を作成してください。この組織をほかの目的で使用すると、課題について検証する際に問題を引き起こす可能性があります。
* Residential Sales の資産を実装するために[未管理パッケージ](https://login.salesforce.com/packaging/installPackage.apexp?p0=04t34000001IqqV)をインストールしてください。(パッケージ ID: 04t34000001IqqV) 管理パッケージ、未管理パッケージ、アプリケーションを AppExchangeからインストールする際に問題が発生した場合は、[この記事](https://force.desk.com/customer/en/portal/articles/2710899-installing-a-package-or-app-to-complete-a-trailhead-challenge?b_id=13478)に示す手順に従ってください。
* このスーパーバッジで利用される用語のいくつかは、UI に表示される設定上の名称名と完全に一致しない場合があります。これは、Salesforce の機能に関する知識と、ビジネス上のニーズを満たす正しい機能を選択する能力をテストするためです。

## ユースケース
Ursa Major Solar, Inc. は、太陽エネルギー部品およびシステムの大手サプライヤです。そして宇宙と同じように、事業を拡大しています。効率的で費用対効果の高い太陽エネルギーシステムが大きな関心と定着を招いたため、米国の太陽エネルギー生産量は 2016 年にほぼ倍増しました。Ursa Major Solar は公益事業市場で非常に成功しているため、専用の住宅向けセールスチーム (Residential Sales) と一緒に熱い住宅市場に進出しています。あなたは、Salesforce を好調に維持するためにチームのビジネススペシャリストとして選ばれました。

新しく成長しているチームのビジネススペシャリストとして、あなたはたくさんの役割で働くことになります。新しいチームメイトを追加します。マーケティングからの要求に対応して、チームをブランド要件に沿ったものにします。住宅向けセールスチームの成功を支援するために、UI コンポーネントを追加して設定します。Chatter でのコラボレーションのためにチームを設定します。あなたは楽しんでいます！

### 主要なステークホルダ
Chatter フィードに対して、さまざまな部署から住宅向けセールスチームへのフィードバックがたくさんあります。主要なステークホルダは以下の通りです。

- April Hansen (マーケティングマネージャ)
- Gabriela Livingston (セールスオペレーション)
- Maria Jimenez (システム管理者)
- Shinje Tashi (セールスデータ品質スペシャリスト)
- Ada Balewa (製品サポートスペシャリスト)
- Lincoln Ulrich (アカウントエグゼクティブ)
- Lance Park (営業担当)
- Erin Donaghue (営業担当)

### 標準オブジェクト
Ursa Major Solar は以下の標準オブジェクトを利用しています。
- Account (取引先) - Ursa Major Solar から購入する顧客
- Contact (取引先責任者) - Usra Major Solar の見込みまたは既存顧客の連絡先
- Opportunity (商談) - 顧客またはリードの潜在的な取引
- Leads (リード) - プロスペクトまたは潜在的な商談
- Cases (ケース) - 顧客のサポートの問題

## ビジネス要件
### データ管理
April Hansen から、パイロットプロジェクトに参加した古い住宅顧客のデータベースからマーケティングチームが取得した[取引先のリスト](https://developer.salesforce.com/files/bsx-accounts.csv)が送信されました。データベースは、Ursa Major Solar がデータ品質基準のない小さな企業だったときに作成されました。新しいチームがこれらの顧客に電話を掛けられるように、このデータをクリーンアップしてからインポートする必要があります。

#### データ品質標準
取引先の命名規則は、ユーザが探しているものをすばやく見つけさせたり、フィルタを適切に機能させるために重要です。Ursa Major のシステム管理者は次のルールを設定しました。

1. 各取引先の名称が、すべて大文字になっていないこと
2. すべての取引先の Type (種別) の項目に値があること
3. すべての Billing State (都道府県(請求先)) 項目は、フルネームではなく、2文字の州の略語を使用していること

#### 取引先の種別にResidentialを追加
普段は Maria Jimenez が選択リスト項目に新しい値を追加しますが、彼女は今日ボランティアで外出中です。取引先オブジェクトの項目の Type (種別) 項目に **Residential** という値を追加するように依頼されました。

### ユーザ管理
あなたはデータ品質のヒーローで、太陽光発電のロケットベルトを身につけている若手実業家のように、重複を取り除きコンプライアンス違反のレコードを修正します。そして他のスーパーヒーローと同じように、チームでより強くなります。データ品質の維持に専念してもらうために Shinje Tashi をユーザに追加します。また、Mariaが提供した以下のユーザリストの残りの部分も同様に追加します。

#### 注意
Trailhead Playground では、有効な Salesforce ライセンスユーザを 1人だけ追加できます。このチャレンジを完了するには、ユーザを作成して保存してください。ユーザを有効にしない場合は、[Edit(編集)] を選択して [Active(有効)] の横にあるチェックを外し、もう一度保存します。新しいユーザのメールアドレスに入力した値で、そのユーザのユーザ名が自動入力されます。各ユーザ名は Salesforce 内で一意である必要がありますが、メールアドレスの場合は異なります。このスーパーバッジでは、新しいユーザのためにあなた自身のメールアドレスを記入してください。ユーザ名の欄にそのメールアドレスが自動入力されたら、次の式に従って一意のユーザ名に置き換えてください。

``ユーザの名の最初の1文字 + ユーザの姓 @ あなたのイニシャル + 今日の日付(YYMMDD) + .com``

例：abalewa@DK081517.com

その一意のユーザ名をニックネームにもコピーします。

| Name (名前) | Title (役職) | 設定内容 | Active (有効) |
|--|--|--|--|
|Ada Balewa|Product Support Specialist <br>(製品サポートスペシャリスト)| この製品サポートスペシャリストは有料のライセンス無しで、Chatterの投稿やコメントを削除する権限が必要です。|はい|
|Lincoln Ulrich|Account Executive<br>(アカウントエグゼクティブ)|このアカウント・エグゼクティブは Standard User(標準ユーザ)のプロファイルと Customer Support, North America のロールを利用する必要があります。Lincolnは、彼の取引先に対してマーケティングキャンペーンを設定し実施できる必要があります。|いいえ|
|Lance Park|Sales Representative<br>(営業担当者)|この営業担当者は Western Sales Team のロールと Custom: Sales Profile のプロファイルを利用する必要があります。Lance は Mexico で生まれ育ちスペイン語が堪能であるため、その言語での Salesforce の UI を好んでいます。(しかし他の全員は Salesforce は英語で見えるようにしてください。) |いいえ|
|Erin Donaghue|Sales Representative<br>(営業担当者) |この営業担当者は Eastern Sales Team のロールと Custom: Sales Profileのプロファイルを利用する必要があります。|いいえ|
|Shinje Tashi|Sales Data Quality Specialist<br>(セールスデータ品質スペシャリスト)| このセールスデータ品質スペシャリストは会社全体をサポートし、会社全体のすべての取引先、取引先責任者、商談レコードが参照できるロールが割り当てられる必要があります。また、Standard User プロファイルを使用してください。|はい|

#### 特別なプロジェクト
Ursa Major は、バイリンガルサービスプログラムを通じて、カスタマーサポートを改善し、リピーター率を高めるプログラムを試験的に進めています。このパイロットプログラムが成功した場合、Ursa Majorはバイリンガルのアカウント、セールス、サポートの各チームを雇う予定です。Maria Jimenezは、取引先オブジェクトに Language Preference (言語設定) の選択リスト項目を追加しました。このパイロットプログラムのために、プロフィールを変更せずに Shinje Tashi に Language Preference 項目へのアクセス権を提供してください。アクセス権を拡張するために作成したソリューションに **Bilingual Pilot** という名前をつけてください。Lincoln、Lance、Erin のユーザを作成したら、この要件を完了するために Shinje Tashi のユーザを有効にしてください。

### 取引先のレポート・ダッシュボード
住宅向けセールスチーム全員がオンラインになるのに備えて、Gabriela はチームと営業担当者のスコアボードを示すダッシュボードと、ダッシュボードの元となるレポートを作成するよう依頼しています。どの顧客に追加の商談や契約の更新を提供するかを決定するために、セールスオペレーションチームはこれらのレポートとダッシュボードから得た洞察を活用することができます。

#### Residential Reports
**Residential Reports** という名前でレポートフォルダを作成し、関連するレポートを保存します。特に指示がない限り、すべての取引先とすべての期間の作成日でレコード表示するようにレポートを設定します。

#### Accounts by Market
最初に、Gabriela は、公益事業の取引先と新しくインポートされた住宅の取引先との間で、取引先の業種内訳を必要としています。取引先の Type(種別)で行を集計(**Market** という項目名)し、取引先の Rating (評価) で列を集計する、**Accounts by Market** という名前のマトリックスレポートを作成してください。Gabriela は、次の通り取引先を分類するように求めています。(他のすべて種別は Other と分類してください。)

* Utility
  * 取引先の種別が **Customer - Direct** と **Customer - Channel**
* Residential
  * 取引先の種別が **Residential**

Gabriela は、取引先の分類と評価ごとにレコード件数も表示したいと思っています。レコードの詳細は表示しないでください。

#### High Value Residential
Gabriela が求めている 2番目のレポートは、セールスオペレーションチームが最も価値の高い住宅顧客に注意を払うために役に立ちます。種別が Residential の取引先だけを含めてください。

取引先名でグルーピングし、年間売上 (Annual Revenue) を集計 (合計) する **High Value Residential** というサマリーレポートを作成してください。

#### Rated Accounts by State
Ursa Major の住宅向け事業が十分に大きくなるとすぐに、住宅向けセールスチームは担当する地域で取引先を分け合うことを計画します。それまでは、どの州に最も高く評価された取引先があるかを把握する必要があります。どの地域に焦点を当てるべきかについて住宅向けセールスチームにわかりやすくするために、Gabriela は、列を Rating (評価) で、行を Billing State/Province (請求先(都道府県) ※ここでは州)でグルーピングする **Rated Accounts by State** という住宅顧客のマトリックスレポートを作成するように求めています。彼女は、どの州に最も評価の高い取引先があるかを知りたいだけなので、詳細を隠します。

州および取引先の評価ごとにレコード件数を表示してください。

#### Open Support Cases
Ursa Major Solar の住宅向けセールスチームは顧客を愛し、顧客がサポート問題を解決することを助けるよう努めています。街中の家庭がコンバータの故障を経験している場合でも、砂漠にいる研究者が風にぶつかって緩んだパネルといる場合でも、チームは助けるためにいます。最も緊急のケースに最初に注力するために、チームは、はじめに取引先名、次に優先度の順にグループ化された、すべての取引先のオープンのケースを表示するレポートが必要です。

**Open Support Cases** というサマリーレポートを作成してください。レポートは詳細を表示し、ケースの所有者、件名、ケースの原因だけを含みます。

#### Residential Dashboards
ダッシュボードは、新しい住宅向けセールスチームが、どの取引先が成長していて、どれに注意を向けるべきなのかを理解するのに役立ちます。ステークホルダーは 2つのダッシュボードに関するいくつかのガイドラインを考え出しました。**Residential Dashboards** という名前のダッシュボードフォルダを作成し、以下のダッシュボードをそこに格納します。

#### Team Score Dashboard
ハイレベルのダッシュボードは、セールスリーダーが大きな決断を下すのに役立ちます。**Team Scoreboard** というこのダッシュボードには、どれだけの取引先が住宅顧客なのかの内訳、最高評価の住宅顧客のリスト、および最も評価の高い取引先を持つ州のビューが含まれます。営業チームが優先順位を付けるために、以下の 3つのパワフルなコンポーネントを Team Scoreboard ダッシュボードに含めます。

|タイトル|サブタイトル|ソースレポート|グラフの詳細|
|-|-|-|-|
|Account Distribution|Number of Accounts by Industry Type|Accounts by Market|<ul><li>ドーナツグラフ</li><li>スライスの基準: Market</li><li>表示ラベルの昇順でソート</li><li>表示する最大件数: 2</li><li>グラフのサイズ:幅 6、高さ 11</li></ul>|
|Top Accounts|Top 10 High Value Residential Accounts|High Value Residential|<ul><li>Lightningテーブル</li><li>値の降順でソート</li><li>表示する値の最大数: 10</li><li>グラフのサイズ: 幅 6、高さ 11</li></ul>|
|Ratings by State|Rated Distribution of Accounts by State|Rated Accounts by State|<ul><li>積み上げ縦棒グラフ</li><li>表示する値の最大数: 15</li><li>グラフのサイズ: 幅 12、高さ 8</li></ul>|

#### Rep Scoreboard Dashboard
「チーム (Team)」という言葉の中には「私 (I)」の文字はありませんが、「個人の責任 (Individual Responsibility)」の中には 6 つあります。**Rep Scoreboard**というこのダッシュボードには、評価の高い取引先のリスト、州ごとの評価の分布、オープンのサポートケースのリストがあります。このダッシュボードを表示しているユーザは、以下の 3 つのコンポーネントに関する自分自身のデータだけが見えている必要があります。

|タイトル|サブタイトル|ソースレポート|グラフの詳細|
|-|-|-|-|
|My Top Accounts|Top 5 High Value Residential Accounts|High Value Residential|<ul><li>Lightning テーブル</li><li>値の降順でソート</li><li>表示する値の最大数: 5</li><li>グラフのサイズ: 幅 4、高さ 7</li></ul>|
|Open Support Cases|My Customers’ Open Support Cases|Open Support Cases|<ul><li>Lightning テーブル</li><li>表示する値の最大数: 15</li><li>グラフのサイズ: 幅 4、高さ 7</li></ul>|
|My Accounts by State|Distribution of My Accounts by State|Rated Accounts by State|<ul><li>積み上げ縦棒グラフ</li><li>表示する値の最大数: 10</li><li>グラフのサイズ: 幅 4、高さ 7</li></ul>|

### マーケティングの使命
1996年に Sita Nagappan-Alvarez と夫の Roberto が会社を設立して以来、Ursa Major Solar は誇り高いブランドを築いてきました。使命は変わっていませんが、会社の戦略とロゴは長年にわたって進化してきました。April とマーケティングチームは、住宅向けセールスチームのメールのやりとりに関する現在のグラフィックとメッセージングの要件を送ってきました。潜在的な顧客と現在の顧客の受信トレイを照らし出すために、メールの署名を設定し、チームのために 2つの事前設定済みのメールを設定します。

#### メールの署名
<table>
<tr>
<td><b>メールの署名</b></td>
<td>Residential Sales Team<br>
Ursa Major Solar, Inc.<br>
We take a bite out of your energy bill.</td>
</tr>
</table>

#### レターヘッドとウェルカムメール
<table>
<tr>
<td><b>レターヘッドの名前</b></td>
<td>Residential Sales Letterhead</td>
</tr>
<tr>
<td><b>レターヘッドのヘッダーのロゴ</b></td>
<td>Branding folderのフォルダからUsra Major Solar Logoを選択</td>
</tr>
<tr>
<td><b>レターヘッドの上部・中央・下部の区切り線の色</b></td>
<td>#106935</td>
</tr>
<tr>
<td><b>事前設定されたメールの名前</b></td>
<td>Residential Sales Welcome Email</td>
</tr>
<tr>
<td><b>事前設定されたメールの件名</b></td>
<td>Welcome from Ursa Major Solar!</td>
</tr>
<tr>
<td><b>事前設定されたメールの本文</b></td>
<td>Hey there [ここに取引先責任者名の差し込み項目],<br> 
Did you know enough sunlight hits the earth in one hour to power the entire world economy for a year? <br>
Did you know solar energy growth doubled last year? <br>
Do you know why the electron crossed the road? <br>
Contact your Ursa Major Solar Residential Sales Team to learn how you can save money on your monthly power bill while saving the planet!</td>
</tr>
<tr>
<td><b>事前設定されたメールの保存場所</b></td>
<td>Residential Sales Emails</td>
</tr>
<tr>
<td><b>メールへのアクセス</b></td>
<td>すべてのユーザには、メールを送信する前にそれを使用し、カスタマイズするためのアクセス権を付与する必要がありますが、基本のバージョンを変更するためのアクセス権を付与してはいけません。</td>
</tr>
</table>

#### 標準的なメールのやりとり
<table>
<tr>
<td><b>レターヘッド</b></td>
<td>Residential Sales Letterhead</td>
</tr>
<tr>
<td><b>事前設定されたメールの名前</b></td>
<td>Residential Sales Correspondence</td>
</tr>
<tr>
<td><b>事前設定されたメールの件名</b></td>
<td>**REPLACE WITH YOUR SUBJECT**</td>
</tr>
<tr>
<td><b>事前設定されたメールの本文</b></td>
<td>Hello [ここに取引先責任者名の差し込み項目],</td>
</tr>
<tr>
<td><b>事前設定されたメールの保存場所</b></td>
<td>Residential Sales Emails</td>
</tr>
</table>

### プラットフォームの機能
110 V と 220 V のコンセントを同じように扱わない(さもなくば花火大会の危険があります！)ように、Ursa Major Solar は住宅事業を公益事業とは異なる方法で扱います。住宅顧客には、地域の公益事業者とは異なる優先順位、設備、設置プロセス、スケジュールがあるため、独自のビジネスアプローチが理にかなっています。住宅向けセールスチームは、注目する顧客情報の一部、商談オブジェクトに構築された特定のビジネスライフサイクル、その商談が住宅事業か公益事業かを識別する方法を必要としています。

<table>
<tr>
<td>
ビジネスライフサイクルの名前</td>
<td>Residential Opportunities</td>
<tr>
<td>ビジネスライフサイクルのフェーズ</td>
<td>Prospecting
<br>Value Proposition
<br>Proposal/Price Quote
<br>Negotiation/Review
<br>Closed Won
<br>Closed Lost</td>
</tr>
<tr>
<td>顧客情報を表示するページの名前</td>
<td>Residential Opportunity Page</td>
</tr>
<tr>
<td>
表示したい顧客情報</td>
<td>
Utility Opportunity Page と同様ですが以下の項目を取り除いてください。
<ul>
<li>Lead Source (リードソース)</li>
<li>Primary Campaign Source (主キャンペーンソース)</li>
<li>Delivery/Installation Status</li>
<li>Main Competitor(s)</li>
<li>Current Generator(s)</li>
</ul>
そして以下の項目を追加してください。
<ul>
<li>Quantity</li>
</ul>
</td>
</tr>
<tr>
<td>
顧客情報を表示するコンパクトビューのラベル名 (name autopopulates)</td>
<td>Residential Opportunity Compact View</td>
<tr>
<td>
コンパクトビューに表示する顧客情報</td>
<td>Account Name (取引先名)
<br>Probability (確度)
<br>Stage (フェーズ)
<br>Amount (金額)</td>
</tr>
<tr>
<td>レコードの種類のラベル (name autopopulates)</td>
<td>Residential Opportunity</td>
</tr>
<tr>
<td>レコードの種類の説明</td>
<td>For residential sales opportunities requiring that special Residential Sales touch</td>
</tr><tr><td>レコードの種類の設定</td><td>ここで住宅向けの商談のために作成したビジネスプロセスと顧客情報を表示するページを使用するよう選択してください。
</td>
</tr>
<tr><td>Residential Opportunityにアクセスするプロファイル</td><td>Custom: Sales ProfileとSystem Administrator(システム管理者)</td>
</tr>
</table>

### コラボレーション
住宅向けセールスチームは立ち上がって稼働していますが、製品に関する質問が多数抱えています。ソーラーパネルのパズルを解決するための製品サポートスペシャリストがいますが、より幅広い組織から守られているチームのメンバー間での問い合わせや会話のためのフォーラムがありません。このチームは、価格戦略、製品の問題解決方法、内輪話といった慎重に扱うべきトピックについて話し合うための独自のコラボレーションスペースを必要としています。

1. このスペースの名前を **Residential Sales Product Collaboration** としてください。
2. コラボレーションを促進できると思う写真をスペースに割り当ててください。
3. Ada Balewa に投稿とコメントを削除でき、Residentail Sales Product Collaboration スペースへの新規メンバーを承認できる権限を付与してください。
4. 質問が投稿できるよう Shinje Tashi を加えてください。しかし彼には、メンバーを受け入れる権限や他の人々の投稿を削除する権限はありません。
5. このスペースへの参加状況に関わらず全員に見えるようなスペースの説明を以下の通り記載してください。**This collaboration space is for Residential Sales team members to ask product questions of one another and the Product Support Specialist team.**
6. このスペースへアクセスできるメンバーに対して、追加の詳細を以下の通り記載してください。**As a reminder, monthly webinars with the Product Support Specialist team are on the second Tuesday at 3:00 PM MT. Ask Lincoln Ulrich for the invite. For more information about using Salesforce, check out the Trailhead CRM Basics module.** 
7. コラボレーションスペース内で、多岐選択式の質問を作成して住宅向け市場の製品に対する精通度合いを計りましょう。**Which product are you most comfortable selling?** と質問し、選択肢は**Home Array**、**Home Battery**、**Home Starter Kit**、**Home Starter Kit Deluxe** としてください。
8. コラボレーションスペース内で、Ada Balewa に @ メンションし、**Thank you so much for helping the team out like this. Without your brains, we couldn’t shine so brightly!** と投稿してください。

## Challenge
### Challenge 1: データの修正とインポート
もしまだであれば、事前準備に記載のある未管理パッケージをインストールしてください。そして取引先の Type(種別) に Residential を追加します。April Hansen の取引先データを、インポート前にデータ品質標準に準拠するよう修正してからインポートしてください。

### Challenge 2: ユーザの作成
記載されているビジネス目標を達成するために、Maria が名前、役割、ユーザライセンス、プロファイル、およびロケールとともに送ってきたユーザのリストを追加します。Shinje に Language Preference 項目へのアクセス権を提供するソリューションを作成して割り当ててください。

### Challenge 3: レポートとダッシュボードの作成
住宅向けセールスチームが取引先の価値をより理解しやすくするために、4つのレポートと 2つのダッシュボードとそれらの保存場所を作成してください。Challenge を検証する直前に両方のダッシュボードを更新してください。

### Challenge 4: 再利用可能なメールを設定する
住宅向けセールスチームが自己紹介するために、メールの署名を設定し、レターヘッド、事前に設定された 2つのメール、それらの保存場所を作成してください。

### Challenge 5: ビジネスプロセスを構築する
住宅向けセールスチームがその固有のビジネス要求に専念できるよう、新しいビジネスライフサイクル、顧客情報を表示するページ、顧客情報を表示するコンパクトビュー、レコードの種類を新しく設定してください。

### Challenge 6: コラボレーションのためのスペースを構築する
ビジネス要求に基づいてコラボレーションスペースを作成し設定してください。記載された 2つの投稿を作成するためのコラボレーション機能を利用してください。