# Selling with Sales Cloud Specialist
[![](https://img.shields.io/badge/-view%20on%20gitbook-blue?logo=markdown)](https://shunkosa.gitbook.io/trailhead-superbadge-jp/sales-cloud-specialist) [![](https://img.shields.io/badge/-view%20on%20github-black?logo=github)](https://github.com/shunkosa/trailhead-superbadge-jp/blob/master/src/sales-cloud-specialist/sales-cloud-specialist.md)
* Trailheadのスーパーバッジ、[Selling with Sales Cloud Specialist](https://trailhead.salesforce.com/content/learn/superbadges/superbadge_selling_sales_cloud_specialist) の日本語訳(**非公式**)です。
* 各カスタマイズ要素のラベル部分には補足として日本語を括弧内に記載している場合がありますが、正解チェックは英語のラベルを元に行われるため、実際のチャレンジには日本語表記を含めず、英語表記のみを使用して行って下さい。また、チャレンジ前にユーザと組織の言語・ロケールを英語に切り替えておくことを推奨します。

---
## このスーパーバッジを取得するためにすること
1. Lightning Sales コンソールに対してできる設定の特定
2. パス、レコードタイプ、フェーズの使用
3. Lightning Sync を使用したデータの同期
4. Lightning ダッシュボードビルダーを使用したデータの可視化
5. 商品、価格、見積、注文の管理
6. リードを取引先、取引先責任者、および商談に変換する方法の特定
7. Lightning Experience での取引先階層の管理
8. 重複レコードとデータの完全性の管理

## このスーパーバッジでテストする概念
- Salesforce Sales Cloud
- データの重複除外
- プロセスビルダー
- Lightning レポート

## 特別な Developer Edition 組織にサインアップする
このスーパーバッジを完了するには、Sales Cloud とサンプルデータを含む特別な Developer Edition 組織が必要です。無料の Developer Edition を入手して Trailhead に接続すると、このスーパーバッジの Challenge を完了することができます。この Developer Edition は、このスーパーバッジの Challenge に対応するように設計されており、他のバッジでは機能しない可能性があることに注意してください。Trailhead Playground または、推奨される特別な Developer Edition 組織を使用していることを常に確認してください。

1. [Sales Cloud を備える無料の Developer Edition 組織](https://developer.salesforce.com/promotions/orgs/sellingspecialist)にサインアップします。
2. フォームに入力します。Email の欄には、有効な電子メールアドレスを入力します。Username の欄には、メールアドレス形式の一意のユーザ名を入力しますが、有効な電子メールアカウントと一致している必要はありません。(例: yourname@test.com) 
3. フォームに入力したら、**Sign Me Up**  (サインアップ) をクリックします。確認メッセージが表示されます。
4. ようこそメールを受信 (数分かかる場合があります) したら、それを開き、**Verify Account** (アカウントを確認) をクリックします。
5. パスワードと秘密の質問を設定して、登録を完了します。**ポイント**: 後で簡単にアクセスできるように、ユーザ名、パスワード、およびログイン URLを書き留めます。
6. Developer Edition にログインされた状態になります。

次に、新しい Developer Edition 組織を Trailhead に接続します。

1. Trailhead アカウントにログインしていることを確認してください。
2. このページの下部にある **Challenge** セクションで、選択リストから **Log into a Developer Edition** (Developer Edition にログイン) を選択します。
3. ログイン画面で、先ほど設定した Developer Edition のユーザ名とパスワードを入力します。
4. Allow Access? (アクセスを許可しますか？) の画面で、**Allow** (許可) をクリックします。
5. Want to connect this org for hands-on challenges? (この組織をハンズオンの Challenge 用に保存しますか？) の画面で、**Yes! Save it** (はい、保存します) をクリックします。Challenge のページにリダイレクトされ、新しい Developer Edition を使用してこのスーパーバッジを獲得する準備が整います。

### 重要な注意点
Challenge を始める前に、[Selling With Sales Cloud Specialist: Trailhead Challenge Help](https://trailhead.salesforce.com/help?article=Selling-with-Sales-Cloud-Specialist-Superbadge-Challenge-Help) のナレッジ記事(英語) を確認してください。

## ユースケース
国際的なソーラーパネルメーカおよびサービスプロバイダである Ursa Major Solar は最近、地域企業の SouthernSolar を買収しましたが、彼らが保有するデータは無秩序でした。Ursa Major の北米地域のセールス担当者として、SouthernSolar のデータを確認し、Ursa Major の Salesforce インスタンスにそのデータを入力し、新しいチームメンバーが新しいシステムの定着化に必要となるツール、知識、情報を得られるようにする責務があなたにはあります。注: 将来、Ursa Major の Salesforce システム管理者は自動化プロセスを追加する可能性がありますが、現時点ではこれらの手順はすべて手動です。

最初のステップは、2 社のデータを Ursa Major の Salesforce 組織に統合し、クリーンアップして重複がなく、更新されたすべてのレコードが Ursa Major の確立されたセールスプロセス、レコード階層、および内部プロセスに収まるようにすることです。

買収される前、SouthernSolar のセールスチームは、そのレコードを 1箇所に管理するシステムを持っておらず、個々の取引、取引先、取引先責任者などを、それぞれが快適だと思うやり方で管理していました。それは多くの場合、Excel シート、メールフォルダー、およびオンラインカレンダーでしたが、手書きのメモ、戦略的に貼られた付箋、および Rolodex に依存するものもありました。

SouthernSolar が保有するレコードと、Ursa Major の組織にある既存のレコードとの間に、データの重複がある可能性があります。あなたは、SouthernSolar のさまざまなスタッフメンバーからレコードのリストを集めました。それらの情報をすべて正しく入力する必要があります。重複を避けるため、新しいレコードを作成する前に既存のレコードを検索するようにしてください。

## 主要なステークホルダ
* Solange Pereira (CEO)
* Weimar Williams (データアナリスト)
* James August (セールス品質スペシャリスト)
* Byanca Gallagher (セールス担当)

## 標準オブジェクト
Usra Major Solar は以下の標準オブジェクトを使用しています。

* リード - Ursa Major Solar の商品またはサービスに興味がある可能性のある見込み顧客
* 取引先 - Ursa Major Solar から購入する顧客
* 取引先責任者 - Ursa Major Solar の見込み顧客および既存顧客の連絡先担当者
* 商品 - Ursa Major Solar が販売する商品
* 価格表 - Ursa Major Solar が販売する商品のカタログとその価格
* 商談 - 見込み顧客または既存顧客との間で進行中のセールス
* 商談の取引先責任者の役割 - 商談で重要な役割を持つ顧客の個人
* 見積 - 商談の価格見積り
* 契約 - 顧客と Ursa Major Solar 間の署名済みの契約

## ビジネス要件

### Usra Major Solar の販売プロセス
Ursa Major Solar は、やる気のあるセールスマシンのようです。そのプロセスはよく考えられており、Salesforce 上ですでに設定されています。Ursa Major は、資格のあるリードのみが、取引先と商談に変換されることを望んでいます。取引先がまだ存在しない場合、最終的なリードは変換のために次の基準を満たしている必要があります。

* 完了予定日が 12 か月以内であること
* 取引の金額が入力されていること
* 担当者の名前、電話、メールアドレスが特定できていること

### セールスパスのフェーズ

1. Qualified
2. On-Site Evaluation
3. Quote Generation
4. Quote Approved
5. Negotiation
6. Signing
7. Closed Won
8. Closed Lost

### セールスプロセスにおける追加のルールと要件
Ursa Major Solar のセールス担当者は、販売プロセスの早い段階で現地訪問評価を実施します。その現地訪問をスケジュールすると、各セールス担当者は、On-Site Evaluations キューへのメンションを含む Chatter 投稿を商談レコードに作成し、現地訪問評価の日付と時刻を入力し、関連する行動を、`On-site evaluation for (取引先名) `という件名で、`Demo`  公開カレンダーに追加します。

重要な注意点: このスーパーバッジを完了するには、取引先レコードにも Chatter の投稿を作成する必要がありますが、要件が少し異なります。

商談が Quote Generation フェーズに達すると、セールス担当者は商談から新しい見積を作成し、見積 PDF を生成して商談レコードに見積を保存します。

商談が Negotiation フェーズに入ると、セールス担当者は商談に自動的に作成される「Send Term Sheet for Signature」という件名の ToDo に完了マークをつける必要があります。

商談が Signing フェーズに入ると、セールス担当者は商談、取引先、および取引先責任者に紐付いた新しい契約を作成します。その後、担当者はその契約から承認申請を送信する必要があります。

商談が成立すると、セールス担当者は `Notification of Signed Contract` のメールテンプレートを使用して請求部門にメールを送信します。(請求部門のメールアドレスは Challenge では確認されないため、宛先には任意のメールアドレスを使用してください)

### 現在の顧客と連絡先担当者
SouthernSolar のセールスマネージャーが、SouthernSolar の顧客である現在の企業とその主な連絡先担当者が印刷された紙を手渡してきました。Ursa Major Solar の既存の Salesforce 組織にデータを適切に入力してください。顧客のメモに Maintanance (メンテナンス) が必要であると記載されている場合は、表示された日程でメンテナンスをフォローアップする ToDo をスケジュールします。メモにその他の役立つ情報が記載されている場合は、その取引先レコードの Chatter 投稿でメモの内容を共有してください。

電話番号については、標準の電話項目を使用してください。

注: 表内のすべての列を表示するには、左右にスクロールします。

<table style="display: block !important; overflow-x: auto !important; white-space: nowrap !important;">
    <tbody><tr>
        <td nowrap>会社名</td>
        <td nowrap>種別</td>
        <td nowrap>親会社名</td>
        <td nowrap>本部所在地 (市)</td>
        <td nowrap>本部所在地 (州)</td>
        <td nowrap>従業員数</td>
        <td nowrap>連絡先名</td>
        <td nowrap>連絡先電話番号</td>
        <td nowrap>連絡先メールアドレス</td>
        <td nowrap>メモ</td>
    </tr>
    <tr>
        <td>Monsoon Electric</td>
        <td>Maintenance</td>
        <td>Veristcorp</td>
        <td>Jacksonville</td>
        <td>FL</td>
        <td>45</td>
        <td>Mark Storm</td>
        <td>484-555-2625</td>
        <td>mstorm@mselectric.com</td>
        <td>Annual Maintenance Scheduled for July 22nd of next year</td>
    </tr>
    <tr>
        <td>Tri Mall</td>
        <td>Equipment</td>
        <td> </td>
        <td>Collierville</td>
        <td>TN</td>
        <td>310</td>
        <td>Dana Ruber</td>
        <td>389-555-1384</td>
        <td>druber@trimall.com</td>
        <td>Dana left company – need new Point of Contact</td>
    </tr>
    <tr>
        <td>Splashdown Pools</td>
        <td>Equipment + Maintenance</td>
        <td> </td>
        <td>Durham</td>
        <td>NC</td>
        <td>21</td>
        <td>Jennifer Flotes</td>
        <td></td>
        <td>jennyflotes@splashdownpools.com</td>
        <td>Acquired by SunPool Heating in April of next year</td>
    </tr>
    <tr>
        <td>Sunshine Power Solutions</td>
        <td>Maintenance</td>
        <td> </td>
        <td>Macon</td>
        <td>GA</td>
        <td>125</td>
        <td>Sarah Shock</td>
        <td>635-555-8965</td>
        <td>sarah@sunshineps.com</td>
        <td>Annual Maintenance Scheduled for February 15th of next year</td>
    </tr>
    <tr>
        <td>Hamm n Fam Auto</td>
        <td>Equipment</td>
        <td> </td>
        <td>Lafayette</td>
        <td>LA</td>
        <td>14</td>
        <td>Pam Hamm</td>
        <td>220-555-3200</td>
        <td> </td>  
        <td> </td>
    </tr>
    <tr>
        <td>Vale Cleaners</td>
        <td>Equipment + Maintenance</td>
        <td> </td>
        <td>River Falls</td>
        <td>AL</td>
        <td>10</td>
        <td>Dorothy Vale</td>
        <td>784-555-7090</td>
        <td>dorothy@valecleaners.com</td>
        <td>Annual Maintenance Scheduled for November 11th of next year</td>
    </tr>
    <tr>
        <td>Flutopia</td>
        <td>Equipment</td>
        <td>Fireplaces Etc</td>
        <td>Jackson</td>
        <td>GA</td>
        <td>50</td>
        <td>Sylvia Perrer</td>
        <td>499-555-3736</td>
        <td>sperrer@flutopia.com</td>
        <td> </td>
    </tr>
</tbody>
</table>

この表は CSV ファイルで[ダウンロード](https://developer.salesforce.com/files/001_CurrentCustomers_PointsOfContact.csv)することができます。

### 現在の進行中の契約と将来の潜在的な契約
SouthernSolar のセールスチームは、既存の取引と将来のセールスの可能性を楽しみにしています。以下は、SouthernSolar のセールス担当者が Ursa Major に報告したリストです。Ursa Major Solar の既存の Salesforce 組織で、リードの評価基準に従いデータを適切に入力してください。

見積に関する注意: 実際、税金と送料は場所によって異なります。ここでは複雑さが入り込むことを避けるために、税額には合計価格の 10％ を使用し、送料と手数料に 250 ドルの均一料金を使用してください。

注: 表内のすべての列を表示するには、左右にスクロールします。

<table style="display: block !important; overflow-x: auto !important; white-space: nowrap !important;"> 
    <tbody>
        <tr>
            <td nowrap>会社名</td>
            <td nowrap>親会社</td>
            <td nowrap>子会社</td>
            <td nowrap>本部所在地 (市)</td>
            <td nowrap>本部所在地 (州)</td>
            <td nowrap>従業員数</td>
            <td nowrap>担当者氏名</td>
            <td nowrap>担当者電話番号</td>
            <td nowrap>担当者メールアドレス</td>
            <td nowrap>取引の大きさ</td>
            <td nowrap>完了予定日</td>
            <td nowrap>メモ</td>
        </tr>
        <tr> 
            <td nowrap>La Z Tag</td>
            <td>Funpop</td>
            <td> </td>
            <td>Tuscaloosa</td>
            <td>AL</td>
            <td>30</td>
            <td nowrap>Mary Zapps</td>
            <td>415-623-1962</td>
            <td>maryzapps@laztag.com</td>
            <td>$10,950</td>
            <td>Two months from now</td>
            <td>
                <br>
                <br>
                Next step: on-site eval at 10 a.m. on the 15th of next month
            </td>
        </tr>
        <tr>
            <td nowrap>Veristcorp</td>
            <td> </td>
            <td>Monsoon Electric</td>
            <td>Miami</td>
            <td>FL</td>
            <td>715</td>
            <td nowrap>Janis Winchester</td>
            <td>698-555-3366</td>
            <td>jwinchester@veristcorp.com</td>
            <td>$150,000</td>
            <td>Three months from now</td>
            <td>Previous Step: Call, no answer, no VM box
                <br>
                <br>
                Next Step: Try Again
            </td>
        </tr>
        <tr>
            <td nowrap>JobSwell</td>
            <td> </td>
            <td> </td>
            <td>Newport News</td>
            <td>VA</td>
            <td>35</td>
            <td nowrap>Mannon Mirth</td>
            <td>388-555-4679</td>
            <td>Mannon@Jobswell.com</td>
            <td>$85,000</td>
            <td>Four months from now</td>
            <td>
                <br>
                            Status: Quote gen + send 
                            Product: Installation: Industrial - High
            </td>
        </tr>
        <tr>
            <td nowrap>MakeMore</td>
            <td>LienBank</td>
            <td> </td>
            <td>Clemson</td>
            <td>SC</td>
            <td>164</td>
            <td nowrap>Jonathan Frieze</td>
            <td>969-555-2514</td>
            <td>jonfrieze@yahoo.com</td>
            <td>$98,900</td>
            <td>Two months from now</td>
            <td>Status: Starting Negotiation
            </td>
        </tr>
        <tr>
            <td nowrap>WattAge</td>
            <td>TYW Industries</td>
            <td> </td>
            <td>Gulfport</td>
            <td>MS</td>
            <td>62</td>
            <td nowrap>Lara Portis</td>
            <td>911-555-7382</td>
            <td>lportis@wattageco.com</td>
            <td>$10,000</td>
            <td>Two months from now</td>
            <td>Status: Ready to start Signing, 12 month contract from close date
            </td>
        </tr>
        <tr>
            <td nowrap>Fiberwear</td>
            <td> </td>
            <td> </td>
            <td>Manassas</td>
            <td>VA</td>
            <td>150</td>
            <td nowrap>Polly Esther</td>
            <td>809-555-1142</td>
            <td>Polly@fiberwear.com</td>
            <td> </td>
            <td>six months from now</td>
            <td>Previous Step: Web Form
                <br>
                <br>
                Next Step: Info Call
            </td>
        </tr>
        <tr>
            <td nowrap>Bien Venues</td>
            <td></td>
            <td> </td>
            <td>Beechgrove</td>
            <td>TN</td>
            <td>40</td>
            <td nowrap>Martin Allo</td>
            <td>212-555-8825</td>
            <td>mallo@bienvenues.com</td>
            <td> </td>
            <td> </td>
            <td>Previous Step: Got business card
                <br>
                <br>
                Next Step: Info Call
            </td>
        </tr>
        <tr>
            <td nowrap>Fenomeno Shine</td>
            <td></td>
            <td> </td>
            <td>Seattle</td>
            <td>WA</td>
            <td>9</td>
            <td nowrap>Ronaldo Leema</td>
            <td>200-900-2011</td>
            <td>rleema@fenomenoshine.com</td>
            <td> </td>
            <td>18 months from now</td>
            <td>Previous Step: Got business card
                <br>
                <br>
                Next Step: Info Call
            </td>
        </tr>
    </tbody>
</table>

この表は CSV ファイルで[ダウンロード](https://developer.salesforce.com/files/002_CurrentlyPendingDeals.csv)することができます。

### 様々な人々: 名刺
SouthernSolar のセールスアシスタントは、名刺の束で、以下の様々な人々のリストを提供してきました。Ursa Major Solar の既存の Salesforce 組織にデータを適切に入力してください。 Solar Resale Solutions の Harry Hawker はディストリビュータであることに注意してください。このレコードが Distributor/Wholesale Team によって所有されるようにしてください。

<table>
<tr>
<td width="250">表</td>
<td width="250">裏</td>
</tr>
<tr>
<td>
Felicity Dunn</br>
Facilities Mgr</br>
Tri Mall</br>
</br>
389-555-1388</br>
fdunn@trimall.com
</td>
<td>
Wait for new manager to decide whose account this is.
</td>
</tr>
<tr>
<td>
Dex Bannon</br>
CEO</br>
MakeMore</br>
</br>
969-555-2520</br>
dexbannon@makemore.com
</td>
<td>
Met him on flight, directed me to Jon Frieze
</td>
</tr>
<tr>
<td>
Harry Hawker</br>
Vendor Services</br>
Solar Resale Solutions</br>
</br>
915-555-1880</br>
harry@solarsale.com
</td>
<td>
Distributor, HQ in Tampa, Florida, 15 employees
</td>
  </tr>
<tr>
<td>
Travis Stott</br>
Manager</br>
Carewell Homes</br>
</br>
469-555-7278</br>
tstott@carewellhomes.com
</td>
<td>
Trade show - Wants Demo
</td>
</tr>
<tr>
<td>
Lance Roth</br>
Associate</br>
Lunchador Kitchens</br>
</br>
377-555-4138</br>
lroth@lunchador.com
</td>
<td>
Whitepaper Lead - Needs to be Qualified
</td>
</tr>
<tr>
<td>
Sam Steel</br>
Operations Mgr</br>
JobSwell</br>
</br>
(388) 555-4678</br>
ssteel@Jobswell.com
</td>
<td></td>
</tr>
</table>


### 付箋のメモ
フロントの受付係から付箋を渡されました。Ursa Major Solar の既存の Salesforce 組織にデータを適切に入力してください。

```
2019/6/25
Splashdown Pools の Jen Floats からアカウントサービスについて
留守電あり
413-555-7615 
```

### 電話の呼び出し音
<!-- textlint-disable jtf-style/4.3.3.かぎかっこ「」 -->
「こんにちは、フロントのジョンです。昼食時にあなたへの伝言をいくつか受け取ったので、準備ができたら教えてください。いいですか？では始めます。

まず、経営陣から。Ursa Major と SouthernSolar がデータを結合したため、経営陣はセールスパイプラインに対して少し『バランス』を取っています。Daily Bakery 社の取引があなたに割り当てられ、フェーズは『Closed Won』になります。Long John's Socks 社の取引があなたにに割り当てられ、確度は 75％ になります。そして、Enerplus 社の取引があなたに割り当てられました。この取引のフェーズは、『Quote Approved』に更新する必要があります。ディストリビュータとの取引であるため、確度は 80％ に更新する必要があります。私達はディストリビュータとの取引用に個別の価格表ができたことを本当に気に入っています！

そしてさらに素晴らしいニュースがあります。Fiberwear 社の Polly は、今から 6 か月の間に、取引を進めたいと考えています。(彼女は 100,000 ドルと言いました！)

Mannon Mirth という名前の人から、会社の名前は先よく理解できませんでしたが、同じ商談を使って、Installation Industrial - High という名前の商品に対して、別の見積を作成してほしいと依頼がありました。この新しい見積では、数量は 1 ではなく 10 になります。彼は、この見積に対して 5％ の割引を約束してもらえたと言っているので、これに従い調整を行ってください。あっ、そういえば、彼は見積を比較したいと思っているので、元の見積はそのままにしておいてくださいね。

さて、最後に。Sally Helios から電話がありましたが、その情報に一致していると思われる取引先責任者が 2つ見つかったため、どこにログを記録すればよいかわかりませんでした。それらのレコードを適切に重複排除し、今日電話をかけ、コールバックを望んでいたメモを追加してください。(そして、折り返し電話してください。)

ありがとう。以上です！あなたの最初の週がうまくいくことを願っています！」
<!-- textlint-enable jtf-style/4.3.3.かぎかっこ「」 -->

### レポート
すべてのデータをクリーンアップして入力しておくのは良いことです。CEO の Solange Pereira は、東部のセールスチームと西部のセールスチームの両方の概要を示すレポートを求めています。要件に従って次のレポートを作成してください。`12 Month Pipeline` など、表示されている通りにレポートに名前を設定してください。

* **12 Month Pipeline**  - 現在の四半期と次の 3 四半期の、各チームのパイプライン予測に関するレポートであり、四半期ごとに期待収益が合計されて表示されます。
* **Pipeline Type**   - 現在の四半期と次の 3 四半期の、既存顧客のパイプライン取引と新規顧客の取引を比較するレポートです。
* **Pipeline Products** - 現在の四半期および次の 3 四半期の、商品名ごとにグループ化された商品価格を合計して表示するレポートです。
* **Sales Rep Scoreboard** - 今年会計年度に成立した取引の金額で、セールス担当者をランク付けするレポートです。
* **Closed Won by Month** - 月ごとに、成立した (Closed Won フェーズ) の商談の数を表示するレポートです。
* **Activities To Close** - 会計四半期ごとにグループ化された、成立した商談に紐づく行動の数を示すレポートです。

## Challenge

### Challenge 1 - Sales Cloud でセールスを始める
ここから始めましょう！すべての事前準備を完了して、特別な Developer Edition 組織にサインアップし、Trailhead に接続して、魔法を起こしましょう。このステップの後、組織の準備が整い、他の課題に取り組むことができます

### Challenge 2 - 現在の顧客を入力する
Salesforce 上に現在の顧客のリストが正しく入力していることを確認してください。

### Challenge 3 - 連絡先担当者を入力する
連絡先担当者のリストを正しく入力していることを確認してください。

### Challenge 4 - 取引を入力する
取引のリストを正しく入力していることを確認してください。

### Challenge 5 - 様々な人々
様々な連絡先を正しく入力していることを確認してください。

### Challenge 6 - 電話の呼び出し音
フロントデスクのジョンからの電話で説明されているすべての要件を満たすために、必要な変更を行ってください。

### Challenge 7 - レポート
要件に従ってレポートを作成してください。

### Challenge 8 - 多岐選択クイズ
Lightning Sales コンソール、Lightning Sync、取引先の活動、入力されていない必須項目、売上予測に関する質問に回答してください。
