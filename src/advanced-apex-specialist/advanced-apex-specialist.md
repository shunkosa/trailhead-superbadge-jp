# Advanced Apex Specialist
* TrailheadのSuperbadge、[Advanced Apex Specialist](https://trailhead.salesforce.com/ja/content/learn/superbadges/superbadge_aap)の日本語訳(**非公式**)です。
* 各カスタマイズ要素のラベル部分には補足として日本語を括弧内に記載している場合がありますが、正解チェックは英語のラベルを元に行われるため、実際のチャレンジには日本語表記を含めず、英語表記のみを使用して行って下さい。また、チャレンジ前にユーザと組織の言語・ロケールを英語に切り替えておくことを推奨します。

---
## このスーパーバッジを取得するためにすること
1. Apexコードのデバッグとトラブルシュート
2. 大規模データセットに対応するApexコードの開発
3. Visualfordeを用いたカスタムインターフェース開発
4. コードの品質を保証するテスト戦略のデザイン

## このスーパーバッジでテストする概念
* Apexコード内のカスタムメタデータ
* Apex共有
* Apexトランザクション実行
* 集計SOQLクエリ
* 複雑なSOQLクエリ
* ConnectAPI名前空間
* Visualforce開発
* VisualforceのApexクラスとのデータバインディング
* Visualforceのパフォーマンス最適化
* コードのリファクタリングと再利用性
* 定数とラベルの使用
* ApexとVisualforceのテスト
* Apexのトラブルシューティング

所要時間 : 推定12時間 - 16時間

## 事前準備とメモ
* Salesforceには2つの異なるデスクトップユーザインターフェースがあります。Lightning ExperienceとSalesforce Classicです。このモジュールはSalesforce Classic向けにデザインされています。このTrailheadの[Lightning Experienceの基本](https://trailhead.salesforce.com/ja/content/learn/modules/lex_migration_introduction)モジュールでは、インタフェース間の切り替え、Lightning Experienceの有効化についてなどを学ぶことができます。
* 要件を読み進める際にメモを取ってください(映像記憶がない限り)。紙とペン(または電子的なものでも)を用意しましょう。
* このスーパーのために新しいTrailhead Playgroundを作成してください。既存の組織を使用するとChallengeを検証する際に問題が発生する場合があります。
* この[未管理スーパーバッジパッケージ](https://login.salesforce.com/packaging/installPackage.apexp?p0=04tf4000001O5si)をインストールしてください。このパッケージにはChallengeを完了するためのスキーマとコードが含まれています。もし管理・未管理パッケージ、またはAppExchangeアプリケーションをインストールする際に問題が発生した場合は、[Trailhead Playgroundの管理](https://trailhead.salesforce.com/ja/content/learn/modules/trailhead_playground_management)モジュールの手順に従ってください。
* [商品オブジェクトとスケジュールオブジェクト](https://developer.salesforce.com/docs/atlas.ja-jp.object_reference.meta/object_reference/sforce_api_erd_products.htm)のドキュメントを参照してください。   
* 商品オブジェクト(Product2)の商品ファミリ(Product Family)項目を以下の値だけが表示されるように設定してください。
  * Entree
  * Side
  * Dessert
  * Beverage
* 商品のページレイアウトにQuantity OrderedとQuantity Remaining項目を含めてください。
* 取引先のページレイアウトを注文の関連リストが表示されるように更新してください。
* 注文のページレイアウトから、もしあればContract Number(契約番号)項目を取り除いてください。
* 未管理パッケージで提供されるメソッドは名前やシグネチャを変更することなく使用してください。

## ユースケース
Renee LaFleurが料理学校に通っていたとき、彼女は屋外の折りたたみ式の座席を備えたグルメフードトラックで有名な、世界で最も尊敬されているシェフの一人にインターンとして働きました。この経験はReneeが卒業後に自分のフードトラックビジネスを始めるきっかけになりました。New Millennium Delivery - 小さなフードオペレーションで大きな味を提供します。

数年間の努力と長い時間をかけて、Reneeは1台から5台のフードトラックにビジネスを拡大しました。この成功により彼女は、情熱のプロジェクトを追求するための資金を調達しました。「ペイフォワード」<sup>[1](#footnote1)</sup>モデルのビジネスです。ビジネスは始めることが大変だったことを思い出して、彼女は自身の新しいビジネスで、新しいシェフに顧客基盤を確立するより簡単な方法を提供したいと思っています。

Reneeは、New Millennium Deliveryを創設して、食事を一般に広く販売するための低価格なプラットフォームを新人や新進のシェフに提供することで、彼らが名を成せるようにしました。代わりに顧客は、電話で食事を注文できます。その後、New Millennium Deliveryの担当者が注文を配達し、幸せな顧客の写真を撮ります。その写真は、ソーシャルメディア投稿のためにシェフに提供されます。

ApexやVisualforceを含むSalesforceのプラットフォームは、New Millennium Deliveryのビジネスを推進するテクノロジです。以前、Reneeは自分のSalesforceアプリケーションの構築を手伝うために開発者を雇いました。今、あなたは前任の開発者が中断したところからまた始める幸運な開発者です。

地元のフード＆ワインフェスティバルで初公開できるようにするために、Reneeは、前任の開発者へほんの数週間でアプリケーションの初期バージョンを作成することを依頼しました。彼女は、開発者がこのような厳しいスケジュールに陥ると、速さを理由に品質が失われることを知っていました。時間を優先した結果、ベストプラクティスは無視されることがありました。ベストプラクティスを無視すると、残りの開発プロセスにも影響がありました。Reneeはあなたにこれを修正してほしいと思っています。

現在のアプリケーションのレガシーコードを確認して理解してから、プログラミングとアプリケーション設計のベストプラクティスを使用してコードの修正と新しい機能を実装するように彼女から依頼されました。

### 標準オブジェクト
New Millennium Deliveryはそのデータを以下のSalesforce標準オブジェクトで管理しています。

* **Accounts** (取引先) - 食料を注文するNew Millennium Deliveryの顧客
* **Products** (商品) - 購入可能な様々な食品
* **Pricebook Entries** (価格表エントリ) - 食品の価格
* **Orders** (注文) - 配達される食事の注文  
* **Order Items** (注文商品) - 顧客の注文に含まれる商品 

もし商品に関連する標準オブジェクトのデータモデルに馴染みがない場合は、[このドキュメント]((https://developer.salesforce.com/docs/atlas.en-us.api.meta/api/sforce_api_erd_products.htm).)を参照してください。

New Millennium Deliveryの新しいビジネスロジックには、カスタム項目、リレーション、カスタムオブジェクトを新しく必要としないことに注意してください。

## ビジネス要件

### 事前テストデータ
Challenge 1を完了したら、Playground組織に作成されている次のNew Millennium Deliveryの新しい商品を確認してください。

| Product Name<br>(商品名) | Product Family<br>(商品ファミリ) | Initial Inventory | Quantity Ordered | Active<br>(有効) | Standard Price<br>(標準価格) |
|-|-|-|-|-|-|
|Pizza|Entree|25|0|true|$20.00|
|Garlic Bread|Side|20|0|TRUE|$6.00|
|Chocolate Cake|Dessert|15|0|TRUE|$5.00|
|Coconut Water|Beverage|10|0|TRUE|$3.00|
|Hamburger|Entree|25|0|TRUE|$20.00|
|French Fries|Side|20|0|TRUE|$6.00|
|Carrot Cake|Dessert|15|0|TRUE|$5.00|
|Lemonade|Beverage|10|0|TRUE|$3.00|
|Hot Dog|Entree|25|0|TRUE|$10.00|
|Onion Rings|Side|20|0|TRUE|$6.00|
|Jello|Dessert|15|0|TRUE|$2.50|
|Iced Tea|Beverage|10|0|TRUE|$3.00|

### 定数を使用してデータを格納する
値は何度も変わる可能性があるが目的は変わらないようなデータを格納するには、定数を利用するベストプラクティスに従うと、アプリケーションをより効率的にできることをDreamforceで学びました。あなたは定数を作成することによってこのベストプラクティスを実装したいと思います。これらの定数のいくつかにはカスタムラベルを利用します。

念のため、事前準備のセクションで、以下の有効値のみを持つように商品ファミリ項目の選択リストを変更しているはずです。
* Entree
* Side
* Dessert
* Beverage

まず2つのカスタム表示ラベルを作成し、以下の属性を設定してください。

|簡単な説明|名前|カテゴリ|値|保護コンポーネント|
|-|-|-|-|-|
|Select One|Select_One|constants|Select one|チェックなし|
|Inventory Level Low|Inventory_Level_Low|constants|Has a low inventory|チェックなし|

注意: もし間違えてラベルを設定してしまった場合は、削除して最初から作り直すことを推奨します。

`Constants`という名前のApexクラスを作成し、以下の定数を定義してください。

|変数名|値|目的|
|-|-|-|
|DEFAULT_ROWS|5|Visualforceページに表示する行数を制御するための整数|
|SELECT_ONE|対応するカスタム表示ラベルの値を設定|Visualforceページで選択リスト値を表示するために使用する文字列|
|INVENTORY_LEVEL_LOW|対応するカスタム表示ラベルの値を設定|在庫数が少ない場合にアラートを発生させるしきい値を決定するために使用する文字列|
|PRODUCT_FAMILY|商品(Product2)オブジェクトの商品ファミリ項目に対するSchema.PicklistEntry型のリスト。このリストは動的であり、常に設定された値を反映している必要があります。|Visualforceページで選択リスト値を表示するために使用するリスト|
|DRAFT_ORDER_STATUS|Draft|注文がドラフト(処理中の注文)であることを示すために用いる文字列。ドラフトの注文レコードは、注文品目が無い限り有効化できません。また、注文がシステム上で保存されない限り品目を追加することはできません。|
|ACTIVATED_ORDER_STATUS|Activated|注文が有効化(Activated)されているかどうかを評価するために用いる文字列|
|INVENTORY_ANNOUNCEMENTS|Inventory Announcements|Chatterグループを名称でクエリするために用いる文字列|
|ERROR_MESSAGE|An error has occurred, please take a screenshot with the URL and send it to IT.|Visualforceページ上でユーザフレンドリーなエラーメッセージを表示するために用いる文字列|
|STANDARD_PRICEBOOK_ID|標準価格表レコードIdをハードコーディングした値|注文や価格表エントリを業務およびテストコードで作成するために用いるId<br><br>**参考情報** : 通常、標準価格表のIdを取得するには、クエリと`Test.getStandardPricebookId()`の利用を推奨します。しかしこのコードは業務とテストロジックの両方で使用されるため、その方法は利用できません。実際、テストメソッドの外から`Test.getStandardPricebookId()`を呼び出すとシステム例外がスローされます。それによりこのステップを正しく完了させることが困難になるでしょう。<sup>[2](#footnote2)</sup>|


### カスタムメタデータ型を利用する
在庫管理社はReneeに在庫が少なくなってきたらそのことを知らせてほしいと伝えています。例えば、在庫に残っているデザートの種類が15種類しかない場合に、アラートが表示されてほしいと思っています。つまり、特定の商品の在庫レベルがその商品に関連付けられている商品ファミリのしきい値まで低下した場合、通知が必要になります。

過去数ヶ月間の注文データの分析に基づいて、Reneeは各商品ファミリの在庫しきい値を決定しました。彼女は各商品ファミリの在庫しきい値を保存したいのですが、売上が伸び続けるのに従って、これらのしきい値を簡単に変更したいと考えています。慎重に検討した後、カスタムメタデータ型がこれらの要件を満たすためにぴったりだと判断しました。

以下の属性を使用してカスタムメタデータ型を作成します。

|項目|値|
|-|-|
|表示ラベル|Inventory Setting|
|表示ラベル(複数形)|Inventory Settings|
|オブジェクト名|Inventory_Setting|

次に、その新しいカスタムメタデータ型に新しいカスタム項目を作成してください。

|項目|値|
|-|-|
|データ型|数値|
|項目の表示ラベル|Low Quantity Alert|
|桁数|18|
|小数点の位置|0|
|項目名|Low_Quantity_Alert|

Manage Inventory Settings(レコードの管理)から、以下のカスタムメタデータレコードを作成してください。

|表示ラベル|Low Quantity Alert|
|-|-|
|Entree|20|
|Side|10|
|Dessert|15|
|Beverage|5|

### 在庫数を正確に計算する
営業担当者のSamと話したことから、Reneeは新しい顧客の注文を入力する際に​​問題があることを知りました。サムは次の問題に言及しました：

1. Quantity Ordered項目の値が正確ではない
2. システムエラーが原因で新しい注文を保存することができない場合が多い
3. ドラフトの注文(処理中であるがまだ有効化されていない注文)が利用可能な在庫を早くに減らしてしまう

Samが提起した問題を調査した後、あなたはこれらの問題の解決に向けたメモを残しました。
* Quantity Ordered項目の値を導き出すためのビジネスロジックは、誤っているだけでなく、非効率的です。システムは、無駄のないコードを使用して効率的に計算を行い、正しくQuantity Ordered項目を集計する必要があります。
* Samは、ドラフトの注文が早くに在庫数を減らしてしまうことを正しく識別しました。前任の開発者がこれを修正しようとしましたが、決して終わらなかったことが分かりました。今度は、正常に有効化された注文だけが在庫数に影響を与えるように、ビジネスロジックを修正する必要があります。
* Quantity Ordered項目の値を決定するためのロジックを、1人の営業担当者に表示される注文だけに基づくのではなく、システム内にあるすべての有効化された注文を考慮に入れるように更新する必要があります。
* `OrderTrigger`は、Apex Triggerのベストプラクティスに従うように更新する必要があります。これにより、ビジネスロジックがモジュール化されて再利用可能になります。さらに、トリガー定義には必要なトリガーイベントのみを列挙する必要があります。

**参考情報** : 通常、このロジックはUpdate、Delete、Undeleteのトリガコンテキストに適用され、ステータスをドラフトに戻しますが、時間の都合上、そしてこのスーパーバッジで同じ作業を繰り返し行わないようにするため、ここではUpdateコンテキストだけに注力します。

### 商品と価格表エントリを追加できるVisualforceページを正しくする
前任のプログラマーは`Product2New`というVisualforceページを作成しました。このページの目的は、在庫管理者が一度に複数の新商品と関連する価格表エントリのレコードを迅速に入力できるようにすることです。ただし、在庫管理者は、このページではデータ入力が遅くなり、必要な情報がすべて提供されていないというフィードバックを寄せています。

これを解決するには、商品オブジェクトの標準の**Add** および**New** ボタンをアップデートされたバージョンの`Product2New`で上書きすることを実装する必要があります。

アップデートされたページでは、在庫管理者が一度に複数の商品を作成し、各商品に関連付けられたUnit Price(単価)を入力できるようになります。次に、在庫管理者が**Save** (保存)ボタンをクリックすると、システム内の結果として、入力された各商品に対して、標準価格表に関連する価格表エントリが作成されます。ページ上では、すべての項目が入力されているエントリのみを保存する必要があります。他のエントリは保存しないでください。保存中にエラーが発生した場合は、セーブポイントをロールバックし、わかりやすいエラーメッセージを画面に表示する必要があります。在庫管理者は必要なだけ商品を入力でき、ページのAdd (追加)ボタンをクリックするたびに複数の行をテーブルに追加できるようにする必要があります。

将来ビジネス要件が変化したときに、Reneeは`Product2New`のページや`Product2Extension`のクラスを修正したくないと思っています。このニーズを満たすために、

 * 各列のヘッダーに現在の項目ラベルが表示されるようにVisualforceページを更新します。 
 * `AddRows`メソッドがDEFAULT_ROWS定数を使用するようにApexクラスを更新します。  
 * ページ上の**Family**選択リストで使用するための`GetFamilyOptions`という名前の新しいメソッドを作成します。`GetFamilyOptions`メソッドは選択リストの選択肢を生成するためにSELECT_ONEとPRODUCT_FAMILYの両方の定数を使用する必要があります。

商品レコードと価格表エントリレコードを互いに関連付ける必要があるため、次の属性を持つ`ProductWrapper`という名前のインナークラスを実装して使用します。

 * **Product2**型の**productRecord**
 * **PriceBookEntry**型の**pricebookEntryRecord**

現在の商品オブジェクトのリストへの参照を`ProductWrapper`のリストへの参照に置き換えるようにしてください。

在庫管理者は、New Millennium Deliveryの商品の需要と供給のバランスを取ろうとしています。彼らは、横棒グラフをVisualforceページに追加するよう求めました。彼らはグラフに製品ファミリー毎のQuantity Remaining項目の値を表示することを望んでいます。在庫管理者が**Add**をボタンをクリックしたとき、グラグは正しく再描画される必要があります。

このグラフデータは他の目的にも役立つので、`ChartHelper`という名前の独自のApexクラスから生成されます。内部のコードが常にシステムとして実行されるように`ChartHelper`を更新してください。`ChartHelper`の`GetInventory`メソッドを完成させると、Quantity Remaining項目の値が正で有効な商品の集計が正しく計算され、結果がすべてのユーザーにとって正しくなるようにしてください。Reneeは、このメソッドがLightningコンポーネントでも使用できるようにしたいと考えています。

### テストデータファクトリーを作成する
いくつかの調査の結果、前任のプログラマが`TestDataFactory`クラスを使って単体テストのためのテストデータをモジュール的かつ効率的に生成することに決めたと分かりました。しかし、そのクラスはまだ完成していないことにも気付きました。メソッド名はありますが、実際のロジックはありません。アプリケーションの単体テストに適用できるサンプルビジネスデータをモデル化する効率的な方法を提供するために、`TestDataFactory`クラスを完成させてください。各メソッドがテストクラスのユーティリティメソッドとして使用できるように、そしてそれらがインスタンスメンバ変数の値に依存しないようにしてください。

**参考情報** : 通常、`TestDataFactory`クラスに`@isTest`アノテーションを使用しますが、ビジネスロジックからメソッドを呼び出すことはできず、Challengeの検証時にそれらを呼び出すこともできません。

### OrderTriggerとProduct2Extensionの単体テストを作成する
前任の開発者によって実装された最新のApexおよびVisualforceコードは、必要最小限のテストカバー率がないため、リリースできません。あなたは熟練した開発者です、そしてあなたはすべてのコードが十分にテストされなければならないことを知っています。各メソッドがリリースに必要となる最低75％のコードカバー率を持ち、新規および既存の単体テストが実際の顧客データを使用しないようにすることをReneeから依頼されました。レガシーの単体テストを確認しした後、既存の`Product2Tests`のApexクラスを使用して`Product2Extension`をテストでき、そして既存の `OrderTests`のApexクラスを使用して`OrderTrigger`とそのヘルパークラスをテストできることが分かりました。

#### OrderTriggerのロジックを検証する
まず、注文が有効化されたときに**Quantity Ordered**項目が商品で正しく更新されることを検証するためのテストメソッドで使用できるメソッドを作成します。`TestDataFactory`のApexクラスに戻り、以下のシグネチャを持つ新しいメソッドを作成してください。

```java
VerifyQuantityOrdered(Product2 originalProduct, Product2 updatedProduct, Integer qtyOrdered)
```

このメソッドは、updatedProductの**Quantity_Ordered__c**項目が、originalProductの**Quantity_Ordered__c**項目とqtyOrderedの値の合計に等しいことを検証するアサーションを実行する必要があります。

次に、orderTestsクラスに戻り、そのテストメソッドが実際のデータを使用していない(そして使用できない)ことを確認します。`OrderTests`のすべての単体テストのテストデータを生成するために使用される`SetupTestData`という名前の新しいメソッドを作成します。このメソッドは`TestDataFactory`クラスの`InsertTestData`メソッドを呼び出すだけにしてください。

最後に、`OrderTests`に`OrderUpdate_UnitTest`という名前の新しいテストメソッドを作成します。このメソッドは、`SetupTestData`メソッドで作成されたOrderをACTIVATED_ORDER_STATUS定数を使用して有効化してから、`verifyQuantityOrdered`メソッドを使用して商品のQuantity Ordered項目がトリガーによって増加したことを検証する必要があります。

**参考情報** : **VerifyQuantityOrdered**のようなメソッドは、すべての単体テストにわたって一貫してロジックがテストされるようにするのに役立ちます。また、このChallengeを適切に完了しているかの検証もずっと簡単になります！コードベースが大きくなるにつれて、これらの種類のメソッドをもっと作成することができます。もしそうなら、あなたはそれらを`TestDataFactory`とは異なるクラスに移動したいと思うでしょう。

#### Product2Newページのロジックを検証する
`Product2Tests`クラスの`Product2Extension_UnitTest`メソッドを完成させてください。この単体テストは、ユーザーが`Product2New`ページにアクセスして対話するのをシミュレートし、それが予想通りに動作することをテストする必要があります。ユーザーが最初にそのページにアクセスすると、画面に複数の行が表示されます。
**productsToInsert**リストのサイズがDEFAULT_ROWSの定数と等しいことをassertしてください。Add (追加)ボタンをクリックすると、行セットが追加されるので、ボタンを1回クリックした後の**productsToInsert**リストのサイズは**DEFAULT_ROWS**の2倍になることをassertしてください。テストメソッドが実際のデータを使用しない(使用できない)ようにすることを忘れないでください。

次に、Save (保存)ボタンをテストしてください。入力された行が保存され、入力されていない行が保存されていないことを確認してください。**productsToInsert**リストの行をループして最初の5レコードの値を入力してから、Saveボタンのクリックをシミュレートします。5つの商品だけが保存されたことをassertして、ボタンが機能していることを確認します。

テストクラスの作成が完了したら必ずテストを実行して、テストが失敗せず合格することを確認してください。

### 在庫が少ない場合の社内通知を自動化する
New Millennium Deliveryのスタッフは、不足している在庫を把握しておく必要があります。前任の開発者はこれを行おうとしましたが不成功に終わりました。Reneeは、前任の開発者のロジックの問題を修正し、特定の商品をフォローしている従業員だけでなく、適切なすべての従業員に通知することを選択できるようにしたいと考えています。

Chatterグループは従業員がこれらの通知を受け取ることをオプトインするための簡単な方法であると判断しました。**Inventory Announcements**という名前のChatterグループを作成し、このグループに次の説明を入力します。**This group is for New Millennium Delivery employees to receive inventory announcements.** (このグループは、New Millennium Deliveryの従業員が在庫に関するお知らせを受け取るためのものです)。グループは、自動的にアーカイブされず、すべてのユーザーがアクセスできるように作成してください。

**ConnectAPI**について読んだ後、ChatterのAnnouncement(お知らせ機能)は通常のフィード投稿よりも適していることがわかります。これは、お知らせ機能はタイムリーで期限切れになるという点で、アラートのように機能するためです。在庫の値が低いと、そのお知らせがInventory AnnouncementsのChatterグループに投稿されるようにするため、Apexトリガを使用する必要があります。レガシーコードを確認した後、前任のプログラマがこのビジネスロジックを`Product2Trigger`に書こうとしたことに気づきましたが、そのロジックは間違っています。

投稿はDML操作としてカウントされるため、大量のお知らせを投稿する必要がある場合を含め、一括操作によってすべてのお知らせが投稿されるようにするには、Queueableインターフェイスを実装する必要があります。あなたの前任者はSalesforceの開発者フォーラムでいくつかのコードを見つけて、レガシーの`AnnouncementQueueable`というApexクラスを作成しました。このクラスを使って始めましょう。`AnnouncementQueueable`クラスと`Product2Helper`クラスは**ConnectAPI**名前空間を使用して商品レベルが所定のしきい値を下回ったときにChatterのお知らせを自動的に投稿するようにしてください。

Queueableインターフェースを実装するように`AnnouncementQueueable`を修正し、そのpostAnnouncementsメソッドを呼び出します。制限を超えて投稿するお知らせがある場合は、必ず自分自身を再度キューに入れます。

product2Helperクラスの既存のコードを確認した後、それも定数クラスの恩恵を受けられることがわかります。アプリケーション内の一貫性を保証するために、"group name"の代わりにINVENTORY_ANNOUNCEMENTS定数を使用するように`Product2Helper`を修正します。

Chatterグループ用の新しいAnnouncementInputを構築し、`AnnouncementQueuable`のApexクラスで使用するには、`Product2Helper`の`PostAlerts`メソッドを完成させます。

次に、商品のQuantity_Remaining__c項目が、以前に作成したカスタムメタデータレコードに記録されているしきい値を下回ったと判断したときに`PostAlerts`メソッドを使用するように、`AfterUpdate`メソッドを完成させます。

ベストプラクティスでは、ビジネスロジックコードを再利用可能にし、テストを容易にし、デバッグを容易にするために、Apexクラスに格納する必要があります。After Updateのイベントでのみ実行され、`Product2Helper`のロジックを呼び出すように`Product2Trigger`を修正してください。

**参考情報** : 多くの開発者(私たちTrailheadチームを含む)はテスト駆動開発を使用することを好み、最初にテストから始めます。現実の世界ではうまく機能しますが、プログラムによりあなたのChallengeを評価することはそれほど簡単ではありません。したがって、これらのChallengeを示された順序で実行することをしっかりと守ってください。

### 迅速に注文の登録が可能となるVisualforceページのコントローラ拡張を完成させる
New Millennium Deliveryの顧客には大好きな食品があるため、そのような商品はすぐに売り切れます。パーソナライズされた顧客メニューを提供できるように、各顧客が最も注文した食品を在庫管理者が簡単に判断できるようにするのがあなたの仕事です。

New Millennium Deliveryで注文を受けた従業員には、注文と注文商品を保存するための合理化されたプロセスを提供するページが必要です。前任の開発者はこれを容易にするためにVisualforceページ`OrderEdit`を作成しましたが、そのコントローラ拡張を完成させることができませんでした。

![OrderEdit Visualforce page showing a list of products, Order Pricing Summery pie chart and the order details.](adv-apex-sb-new-order.png)
図1.1：OrderEditのVisualforceページ

在庫管理者が注文を作成または編集するときにこのページが使用されるようにする必要があります。`OrderExtension`クラスを完成させて、ページに注文の詳細、注文商品と注文金額を要約した円グラフ、および有効なな商品のリストを表示できるようにしましょう。

1. 円グラフには、注文内の各商品がパイとして表示されます。パイの値は、Quantity(数量)にUnit Price(単価)を掛けた値に等しくなります。`OnFieldChange`メソッドを完成させて、QuantityまたはUnit Price項目に対する値の変更を追跡します。この方法でも、円グラフと注文合計のデータにこれらの変更が反映され、画面上で更新されるようになります。
2. このページで使用できる商品は、Millennium Deliveryが販売するすべての有効な商品の全セットです。**DEFAULT_ROWS**定数を使用して、商品リストに一度に表示される行数を制限します。在庫管理者がより早く商品を見つけられるようにするため、`SelectFamily`メソッドを完成させて、表示される商品を、選択された商品ファミリだけに制限します。ユーザーが商品を商品ファミリでフィルタするときに、入力した数量と単価の値が保持されるようにします。  
3. **StandardSetController**のメソッドを使用して、提供されているページネーションのためのメソッドを完成させ、ユーザーが入力可能な商品の複数ページを移動できるようにします。ユーザーがページ遷移したときにも、入力された数量と単価の値が保持されるようにします。
    
Reneeがproduct2Newページでリクエストしたように、彼女は将来ビジネス要件が変わったときに`OrderEdit`ページや`OrderExtension`クラスを修正したくはありません。`Product2Extension`クラスで使われている`GetFamilyOptions`メソッドをコピーして`GetFamilyOptions`メソッドを完成させてください。

ユーザーが**Cancel** (キャンセル)ボタンをクリックした場合は常に、変更内容は保存されません。

ユーザーがSave (保存)をクリックすると、注文と注文商品が保存されます。数量が0より大きい注文商品のみを保存する必要があります。他の商品は保存しないでください。既存の注文を編集するときは、数量が0になるように変更された注文商品をすべて削除する必要があります。保存中にエラーが発生した場合は、セーブポイントをロールバックし、わかりやすいエラーメッセージを画面に表示する必要があります。

### 単体テストを作成する
テストは長期間の開発を成功させる鍵であり、開発プロセスの重要な要素であることを[Apexテストのモジュール](https://trailhead.salesforce.com/ja/content/learn/modules/apex_testing)から思い出してください。品質保証に不可欠であることに加えて、Apex単体テストはApexをリリースおよび配布するための要件でもあります。Reneeから新しい単体テストを作成するように依頼しました。

* `OrderTests`クラスに `OrderExtension_UnitTest`という名前のメソッドを作成し、`OrderExtension`クラスのすべてのメソッドをテストしてください。`Product2Tests`クラスのコードをテンプレートとして使用してください。
* `Product2Tests`クラスに、`Product2Trigger_UnitTest`という名前のメソッドを作成し、商品のQuantity Ordered項目の値が更新されたときのロジックをテストしてください。
* 開発者コンソールで、すべてのテストデータをクリアし、すべてのテストを実行してください。
* `Product2Trigger`および`OrderTrigger`のトリガについて、テストカバー率が75%以上になるようにしてください。
* `Product2Extension`クラスおよび`OrderExtension`クラスについて、テストカバー率が75%以上になるようにしてください。
* `Constants`クラス、`ChartHelper`クラス、`Product2Helper`クラス、`OrderHelper`クラス、`TestDataFactory`クラスについて、カバー率が90%以上になるようにしてください。
    
**参考情報** : テストカバー率はリリースの要件であり、コードが失敗しないようにするための優れた方法です。前提条件となるのバッジで説明されているように、単体テストの目的は一定のカバー率を達成することそのものではなく、ビジネスロジックが期待どおりに動作することを確認することです。

## Challenge
### Challenge 1: ベストプラクティスを用いてコードベースを更新する
**PackageTests**という名前のApexクラスを削除します。

新しいカスタム表示ラベル、定数、カスタムメタデータ型、カスタムメタデータレコードを作成してください。

### Challenge 2: Orderトリガを更新する
* 在庫レベルを計算するビジネスロジックを正して、関連するコードが無駄なく効率的であるようにしてください。
* ベストプラクティスを用い、関連する必要なトリガーイベントに基づいてのみ実行するように**OrderTrigger**を修正してください。
* **OrderHelper**内のコードを更新してください。

### Challenge 3: 新しい商品のVisualforceページを更新する
**Product2New**のVisualforceページと**Product2Extension**のApexクラスをビジネスを要件を満たすように更新してください。

### Challenge 4: テストデータファクトリーを作成する
**TestDataFactory**のApexクラスを完成さてください。クラス内のメソッドは単体テストのためのサンプルデータを生成します。メソッドをインスタンスメソッドにしないでください。

### Challenge 5: 単体テストでテストカバー率を増加させる
* **TestDataFactory**クラスに、シグネチャに従って新しい**VerifyQuantityOrdered**メソッドを作成してください。
* **OrderTrigger**および、**OrderHelper**のロジックを検証するために**OrderTests**を更新してください。
* **Product2Extension_UnitTest**クラスの、**Product2Tests**メソッドを完成させてください。.

### Challenge 6: 在庫が少ない場合の社内通知を自動化する
* 「Inventory Announcements」のChatterグループを作成し、正しい説明を設定してください。
* **AnnouncementQueueable**を完成させQueueableインタフェースを実装してください。
* **Product2Trigger**と**Product2Helper**をビジネス要件を満たすように修正してください。

### Challenge 7: 迅速に注文の登録が可能となるVisualforceページのコントローラ拡張を完成させる
ビジネス要件を満たすように**OrderExtension**の構築を完了させてください。このChallengeのために**OrderEdit**のVisualforceページは修正しないでください。**OrderExtension**に記載されているメソッドや変数は、リネームしたりシグネチャを変更したりすることなく使用してください。

### Challenge 8: 単体テストを作成する
リリースのためにテストカバー率が十分であることを確認し、すべてのテストを実行してください。

## 訳注
* <a name="footnote1">[1]</a> : 原文はPay it Forwardで、これはある人物から受けた親切を、また別の人物への新しい親切でつないでいくことを意味する英語です。
* <a name="footnote2">[2]</a> : レコードIdは環境によって値が異なる可能性があり、これをハードコーディングすることは一般的には推奨されません。このスーパーバッジでは、簡便のためにこれを行っていますが、実際には、`isRunningTest()`を用いて、テストメソッドから実行された場合に限り、`getStandardPricebookId()`を呼び出すといった考慮が必要になります。

## ヒント
### Challenge 1
* [Help - カスタム表示ラベル](https://help.salesforce.com/articleView?id=cl_about.htm&type=5)