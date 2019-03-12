# Security Specialist
* TrailheadのSuperbadge、[Security Specialist](https://trailhead.salesforce.com/ja/content/learn/superbadges/superbadge_security)の日本語訳(**非公式**)です。
* 各カスタマイズ要素のラベル部分には補足として日本語を括弧内に記載している場合がありますが、正解チェックは英語のラベルを元に行われるため、実際のチャレンジには日本語表記を含めず、英語表記のみを使用して行って下さい。また、チャレンジ前にユーザと組織の言語・ロケールを英語に切り替えておくことを推奨します。

---
## このスーパーバッジを取得するためにすること
1. オブジェクトレベルのセキュリティ設定を設定して、どのユーザーがどのオブジェクトにアクセスできるかを制御する
2. レコードレベルのセキュリティ設定を設定して、特定のレコードを作成および編集できるユーザーを制御する
3. セキュリティのベストプラクティスに準拠するように適切なパスワードポリシーを設定する
4. データ保持要件を満たすために項目レベルの変更を追跡する
5. レポート、ダッシュボード、および公開リストビューのセキュリティ設定を設定してユーザーに適切な権限を付与する
6. ユーザーログインのセキュリティを強化するために2要素認証を設定する
7. Salesforce設定への変更を追跡する機能を説明する

## このスーパーバッジでテストする概念
* データセキュリティ
* ユーザ認証
* ユーザ権限

## 事前準備とメモ
* ペンと紙を準備して、要件を読み進める際にメモを取ってください。
* このスーパーバッジ用に、新しいTrailhead Playgroundを作成してください。この組織をほかの目的で使用すると、課題について検証する際に問題を引き起こす可能性があります。
* Lightning Experienceを利用してください。
* [Securityスーパーバッジの未管理パッケージ](https://login.salesforce.com/packaging/installPackage.apexp?p0=04t36000000jWht)をインストールしてください。管理パッケージ、未管理パッケージ、アプリケーションをAppExchangeからインストールする際に問題が発生した場合は、[この記事](https://force.desk.com/customer/en/portal/articles/2710899-installing-a-package-or-app-to-complete-a-trailhead-challenge?b_id=13478)に示す手順に従ってください。
* Trailhead Playground組織では1人のユーザしか新規作成できませんが、このスーパーバッジのチャレンジを完了するために、多くの権限(プロファイル、ロール、公開グループ、等)を作成することができます。様々なセキュリティ設定をテストするためのユーザを作成することをお勧めします。Samantha Corderoという名前のユーザをこの目的のために作成してください。

## ユースケース
GenZ Capitalは顧客に金融サービスを提供するスタートアップ企業です。彼らはソーシャルメディアを通して全てのサービスを提供しています。GenZのIT部門は素晴らしい(絵文字をサポートするシステムは最先端です)一方で、チームは、金融サービス界の大物であるOldGuard Financeに買収される準備があまり出来ていませんでした。OldGuardはGenZのシステムに徹底的なセキュリティ監査を実施しており、現在、変更が必要です。

あなたは、Salesforceの最高レベルのセキュリティコンサルタントとして、ソーシャルメディアのダイレクトメッセージを通して主要なステークホルダと会い、包括的なセキュリティの変更要件をまとめました。

### 標準オブジェクト
取引に関連する全てのデータを保存するため、GenZは以下の標準オブジェクトを利用しています。

- Account (取引先) - GenZ Capitalから金融サービスパッケージを購入する法人
- Contact (取引先責任者) - GenZ Capictalの見込みまたは既存の顧客の担当者
- Opportunity (商談) - GenZ Capitalの金融パッケージに関する取引

### カスタムオブジェクト
このスーパーバッジのために、GenZはカスタムオブジェクトを利用していません。

## ビジネス要件
### システムとデータセキュリティの要件
政府の財務規制を遵守するには、GenZはデータ保持と暗号化の両方のポリシーを実装する必要があり、買収会社OldGuard Financeは、リモートワーカーとモバイルデバイスに対する厳格なアクセスポリシーを持っています。OldGuard Financeはまた、GenZにパスワードのベストプラクティスの実装を求めています。

あなたは一連の会話を通してステークホルダーとこれらのニーズを詳細に探究しました。そして以下の短い要件リストを考え出しました。

- データ保持 - データは180日間保持され、180日が経過した後に報告される必要があります。これはSalesforceの外部のシステムで発生する可能性があります。
- リモート/モバイルユーザのセキュリティ - リモートワーカーは、SalesforceにアクセスするためにVPNを使用する必要があります。すべてのモバイルユーザは2要素認証(2FA)を使用する必要があります。すべてのモバイルユーザは、管理者によって個別に承認される必要があります。
注：使いやすさのために、単独の認証ではなく2FAを管理することにしました。
- 項目レベルのセキュリティ - 取引先責任者レコードのCustomer SSN(Customer SSN)およびBank Account(銀行口座)項目は暗号化する必要があります。商談レコードの[金額]項目の変更はすべて記録する必要があります。
- パスワードポリシー - パスワードは90日ごとにリセットする必要があります。パスワードは8文字以上で、アルファベットと数字の両方を含める必要があります。

### 組織のセキュリティ要件
#### 組織の概要
GenZの営業組織構造には3つのコアチームがあります。Field Sales、Inside Sales、Sales Executiveです。GenZには、最も複雑な取引の実装をしやすくするため、プロジェクトマネージャとして行動する個人もいます。
![](security_superbadge.png)

#### 一般的なレコードレベルのセキュリティ要件
組織のデフォルトのレコードアクセスを以下の通り設定してください。

* 商談を所有するユーザ(とそのマネージャ)だけに、**商談レコードへのアクセスを制限してください**
* 誰が所有しているかにかかわらず、一般に取引先への参照権限のあるプロファイルが割り当たっていれば、組織の誰にでも**取引先レコードへのアクセスを許可してください** (注: 取引先責任者に対してはデフォルトの設定のままにしてください。)

注: これらの一般的なレコードレベルのセキュリティ要件は、以降のより詳細な要件によって上書きされる可能性があります。

#### フィールドセールスユーザに対する要件
フィールドセールスのユーザは自身のリストビューを作成できますが、他の人のリストビューの作成・管理はできません。また、レポート・ダッシュボードを作成できますが、レポート・ダッシュボードフォルダの作成・管理はできません。必要に応じてシステム管理者から権限を付与することで、モバイルアクセスが可能です。Salesforceへのログイン時間帯の制限はありません。所有する商談に対する参照・作成・編集権限があります(削除はありません)。また、すべての取引先を参照・編集できます。

注: フィールドセールスユーザにすべての取引先の参照・編集権限を付与するとき、プロファイルの[すべてのデータの参照]や[すべてのデータの編集]権限は利用しないでください。

#### インサイドセールスユーザに対する要件
インサイドセールスユーザはSalesforceにメインオフィスからのみアクセスでき(IPアドレスは0.0.0.0)、営業時間の間のみアクセスできます(8:00AM～6:00PM、太平洋標準時(PST)、月～金)。モバイルアクセスはできません。レポート・ダッシュボードを作成でき、レポート・ダッシュボードフォルダを作成・管理できます。自身または他の人のためのリストビューを作成・管理できます。インサイドセールスユーザは、取引先と商談を作成でき、すべての取引先と商談を参照・編集できます(削除はありません)。

注: インサイドセールスユーザにすべての取引先と商談の参照・編集権限を付与するとき、プロファイルの[すべてのデータの参照]や[すべてのデータの編集]権限は利用しないでください。

#### セールスエグゼクティブユーザに対する要件
セールスエグゼクティブユーザは、(他の共有設定に関わらず)すべての取引先と商談を参照できます。しかし、取引先と商談の作成・編集・削除はできません。レポート・ダッシュボードを作成できますが、レポート・ダッシュボードフォルダは作成・管理できません。自身のリストビューは作成できますが、他の人のリストビューの作成・管理はできません。必要に応じてシステム管理者から権限を付与することで、モバイルアクセスが可能です。Salesforceへのログイン時間帯の制限はありません。

#### プロジェクトマネージャでもあるユーザに対する特別な要件
社内で他のすべての責任を負うため、プロジェクトマネージャの権限は、他のさまざまなユーザ権限で設定されます。たとえば、Carla Rodriquezの主な仕事はシニアフィールドセールスアソシエイトですが、彼女はプロジェクトマネージャも務めています。このため、プロファイルを使用してレコードレベルの権限を設定することはできません。また、プロジェクトマネージャとレコードを共有するためにロールを使用しないでください。 プロジェクトマネージャは、種別がExisting Customer - UpgradeでフェーズがClosed Wonであるすべての商談を参照できますが、他のユーザが所有する他の商談は参照できません。プロジェクトマネージャは、必要に応じてシステム管理者から権限を付与することで、モバイルアクセスが可能です。プロジェクトマネージャに関連するセキュリティの設定に名前を付けるときは、**Project Managers**という名前を使用します。

## Challenge
### Challenge 1: オブジェクトレベルのセキュリティを設定する
ビジネス要件を満たすプロファイルを作成してください。チーム名をプロファイルに含めて、以下の名前でプロファイルを作成してください。**Field Sales User**、**Inside Sales User**、**Sales Executive User**

### Challenge 2: レコードレベルのセキュリティを設定する
ビジネス要件を満たすようレコードレベルに関連したSalesforceの他の設定を行ってください。Samantha Corderoのユーザを作成し、彼女に**Field Sales User**のプロファイルと**Field Sales**のロールを割り当てます。Samanthaが所有者の商談を作成し、フェーズを**Needs Analysis**に設定します。また、フェーズが**Closed Won**で種別が**Existing Customer - Upgrade**でSamanthaが所有する商談も作成してください。

このSecurityスーパーバッジの未管理パッケージをインストール後、以下の手順で全てのApexテストを実行してください。
1. 設定のクイック検索ボックスで`Apex テスト実行`と検索します。
2. [テストを選択...]ボタンをクリックします。
3. ドロップダウンメニューから[すべての名前空間]を選択します。
4. sb_security.BeAwesomeを選択します。
5. [実行]ボタンをクリックします。

このChallengeをチェックする前に、すべての単体テストが合格していることを確認してください。(テスト名の隣、[状況]に緑色のチェックがつきます)

### Challenge 3: クイズ - 適切なパスワードポリシーを設定する
1. Which password practice creates the most risk for compromising an account? (アカウントを危険にさらすリスクが最も大きいパスワードの習慣はどれですか？)
    - A. Password reuse (パスワードの使いまわし)
    - B. Requiring a minimum password length of 8 characters (パスワードに最低8文字を要求する)
    - C. Using an English-language word or series of words in the password (英単語または連続した英単語をパスワードに用いる)
    - D. Using a mix of upper and lower characters and numbers (大文字小文字と数字を組み合わせて用いる)

2. When is it appropriate to share your Salesforce credentials with another person? (他の人にSalesforceの認証情報を共有するのに最も適しているのはいつですか？)
    - A. When working with your company's internal IT Help Desk (社内のITヘルプデスクと一緒に働いているとき)
    - B. When talking to someone from Salesforce Support (Salesforceのサポートの誰かと話しているとき)
    - C. When you have an assistant or executive admin (アシスタントまたはエグゼクティブのシステム管理者がいるとき)
    - D. All of the above (上記のすべて)
    - E. Never (決して共有しない)

3. Which of the following isn't a best practice for password user requirements? (パスワードのユーザ要件のベストプラクティスでないのは次のうちどれですか？)
    - A. Minimum password length of 8-10 characters (最低8～10文字の文字数)
    - B. Using a mix of alpha and numberic characters (英数字を組みわせて用いること)
    - C. Requiring users to reset their password at least once a year (最低1年に1回パスワードのリセットをユーザに要求すること)
    - D. Users not reusing their Salesforce password on other website and services (他のウェブサイトやサービスにSalesforceのパスワードを使いまわさないこと)

### Challenge 4: 項目レベルの変更をトラッキングする
要件の中で特定された項目の変更をトラッキングするよう設定を見直して更新してください。

### Challenge 5: レポート、ダッシュボード、公開リストビューのセキュリティを設定する
従業員が適切なデータだけを見られるようにし、レポートのための他のセキュリティ要件を設定してください。

### Challenge 6: 2要素認証を設定する
要件に応じて2要素認証を適切に設定してください。2要素認証をSamantha Corderoに割り当ててください。

### Challenge 7: クイズ - Salesforce設定の変更を追跡する
1. What feature would you use to track changes to settings in Salesforce? (Salesforceの設定の変更をトラッキングするにはどの機能を利用しますか？)
    - A. Setup History Tracking (設定変更履歴管理)
    - B. Field Audit Trail (項目監査履歴)
    - C. Setup Audit Trail (設定変更履歴)
    - D. Field History Tracking (項目履歴管理)

2. How many days worth of changes to settings you can download? (何日分の設定変更をダウンロードできますか？)
    - A. 90 days (90日)
    - B. 180 days (180日)
    - C. 370 days (370日)
    - D. 365 days (365日)

3. How many settings changes can you view directly within Setup (without downloading history)? (設定画面から直接、何件の設定変更を確認できますか？(ダウンロードの履歴は除く))
    - A. The 20 most recent changes (最近の20件の変更)
    - B. The past 5-180 days of changes (過去5～180日間の変更)
    - C. The 20-180 most recent changes (最近の20～180件の変更)
    - D. The past 180 days of changes (過去180日間の変更)

4. If a settings change was made by a delegate acting on behalf of an end user, what data is logged within settings change tracking? (もし、代理ユーザ(システム管理者やカスタマーサポート担当者など)がエンドユーザに代わって設定変更を行った場合、何のデータが設定変更履歴に記録されますか？)
    - A. The username of the delegated user (代理ユーザのユーザ名)
    - B. The full name of the delegated user (代理ユーザの氏名)
    - C. The Salesforce IDs of both end and delegated users (エンドユーザ、代理ユーザ両方のSalesforce ID)
    - D. The usernames both the end and delegated users (エンドユーザ、代理ユーザ両方のユーザ名)
