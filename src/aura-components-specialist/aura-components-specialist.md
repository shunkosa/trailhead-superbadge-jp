# Aura Components Specialist
[![](https://img.shields.io/badge/-view%20on%20gitbook-blue?logo=markdown)](https://shunkosa.gitbook.io/trailhead-superbadge-jp/aura-components-specialist) [![](https://img.shields.io/badge/-view%20on%20github-black?logo=github)](https://github.com/shunkosa/trailhead-superbadge-jp/blob/master/src/aura-components-specialist/aura-components-specialist.md)
- Trailhead のスーパーバッジ、[Aura Components Specialist](https://trailhead.salesforce.com/content/learn/superbadges/superbadge_lcf) の日本語訳(**非公式**)です。
- 各カスタマイズ要素のラベル部分には補足として日本語を括弧内に記載している場合がありますが、正解チェックは英語のラベルを元に行われるため、実際のチャレンジには日本語表記を含めず、英語表記のみを使用して行って下さい。また、チャレンジ前にユーザと組織の言語・ロケールを英語に切り替えておくことを推奨します。 

---
## このスーパーバッジを取得するためにすること
1. Salesforce Lightning Design System のマークアップを、完全に機能する Aura コンポーネントに変換します。
2. Lightning Design System とカスタム CSS を使用して Aura コンポーネントをテーマに合わせて構成します。
3. Lightning アプリケーションビルダー、Lightning Experience、Salesforce アプリケーション、および Lightning アプリケーションで、Aura コンポーネントを表示します。
4. カスタムオブジェクトからデータを読み取るための Apex コントローラメソッドを作成して呼び出します。
5. 密結合コンポーネント間の通信を可能にするために、コンポーネントイベントと public メソッドを使用します。
6. 疎結合コンポーネント間の通信を可能にするためにアプリケーションイベントを作成して発生させます。
7. アプリケーションイベントを発生させて、Salesforce のネイティブ機能を呼び出します。
8. 機能がリリース環境で利用可能かどうかに応じて、アプリケーション機能を動的に有効化または無効化します。
9. Lightning Data Service を使用してカスタムオブジェクトのデータを読み書きします。
10. Aura コンポーネント内で外部の JavaScript を作成して使用します。
11. JavaScript と CSS をトラブルシューティングします。

## このスーパーバッジでテストする概念
* Lightning アプリケーションビルダーで使用するための Aura コンポーネントの開発
* コンポーネントのテーマに合わせた構成
* JavaScript を使用したユーザインタラクションの処理
* コンポーネントのトラブルシューティング
* UX コントロールの動的な表示と非表示
* カスタムオブジェクトのデータの読み書き
* コンポーネント間の通信
* ネイティブの Salesforce機能の活用
* Aura コンポーネント内での外部 JavaScript の使用

所用時間 : 推定 10 時間 - 12 時間  

## 事前準備とメモ
- 紙とペンを用意して、要件を読み進める際にメモを取ってください。
- このスーパーバッジのために新しい Trailhead Playground を作成してください。この組織を他のモジュールやタスクに利用すると Challenge の検証のために問題を引き起こす可能性があります。Trailhead Playground では既に私のドメインが有効になっていることに注意してください。私のドメインの設定は編集しないでください。Trailhead Playground にログインできなくなる可能性があります。
<!-- textlint-disable jtf-style/4.3.7.山かっこ<> -->
-  **設定 > セキュリティ > セッションの設定** セクションで、**パフォーマンスを向上させるためにブラウザの安全で永続的なキャッシュを有効にする** のチェックをオフにすることで、コンポーネントのキャッシュを無効化してください。
<!-- textlint-enable jtf-style/4.3.7.山かっこ<> -->
-  [この未管理パッケージ](https://login.salesforce.com/packaging/installPackage.apexp?p0=04tB0000000Q3CM)をインストールしてください。(パッケージ ID: 04tB0000000Q3CM) このパッケージには、チャレンジを完了するために必要となる Apex ロジックに対する全てのスキーマが含まれます。未管理パッケージのインストールに問題が発生した場合は [Trailhead Playground Management](https://trailhead.salesforce.com/modules/trailhead_playground_management) の手順に従ってください。
- Challenge 1 で未管理パッケージのインストールを検証した後、サンプルデータが自動的に組織に追加されます。最初の Challenge を検証後、何らかの理由で組織を変更する場合は、`GenerateData.apxc` の静的メソッド`initData()` を実行してください。
- リリースを確実に成功させるため、要件ドキュメントに指定される命名規則を利用してください。
- 以下の詳細な要件を読みながら、設定された組織のデータスキーマを確認してください。
- コントローラ関数をコーディングする際、**function foo(cmp, evt, hlp)** ではなく、**function foo(component, event, helper)** という命名規則に従ってください。
- イベントを実装する際には、ベストプラクティスとアプリケーションでのイベントの利用用途に応じて適切なイベントタイプを選択する必要があります。
- このスーパーバッジを完了させるにあたり、アナウンスがあるまで、[Lightning Web Component](https://trailhead.salesforce.com/en/content/learn/projects/quick-start-lightning-web-components) ではなく [Aura コンポーネント](https://trailhead.salesforce.com/en/content/learn/modules/lex_dev_lc_basics)を使用・作成してください。

## ユースケース
世界最大のレクリエーショナル・ビークル (RV) のレンタル企業である HowWeRoll Rentals は、この数年間で、RV 車のレンタル市場を独占するようになりました。彼らのキャッチフレーズは、「私たちは素晴らしいサービスを提供します、なぜならそれが How We Roll だから！」です。彼らは、広大なトレーラーハウスから、伝統的なクロムめっきのエアストリーム<sup>[*1](#footnote1)</sup>まで、あらゆるスタイルのキャンピングカーを取り揃えています。もしあなたが旅行熱に悩まされているなら、彼らには治療法があります！

あなたは HowWeRoll の Salesforce の主任開発者として、会社を大成功させるために尽力してきました。RV 車で旅行する人の大部分がボートを所有していることが調査によって明らかになったため、収益を拡大し続けるために、同社の経営陣は彼らのコアである RV車市場を超えて拡大し、レクリエーションボート業界に参入することを決めました。HowWeRoll は、自社のボートの獲得に多額の投資をするのではなく、ボートのシェアリングプログラムを開始し、それによって同社が顧客のボートのリース代理店として機能することを計画しています。HowWeRoll はこの新しいサービスを Friends with Boats と呼んでいます。

あなたは、Lightning Experience、Salesforce アプリケーション、および Lightning アプリケーションで公開されたカスタム Lightning ページを実装するために 1週間与えられました。それにより、営業担当者が顧客のボートに関する情報を入力できるようになります。また、チームメンバーが各ボートを調べるときに、彼らの経験についてのコメントや評価を投稿できるようにします。

あなたが開発するカスタム検索エンジンを使用すると、HowWeRoll の営業担当者は、ボートの在庫と顧客のリクエストをマッチングさせるために、ボート種別(漁船、遊覧船、パーティーボートなど)に基づいてボートの一覧をフィルタできます。

### 標準オブジェクト
以下の標準オブジェクトを扱います。

* **Contact** (取引先責任者) - 組織の連絡先とボートのオーナー
* **User** (ユーザ) - ボートにレビューやコメントを投稿する人

### カスタムオブジェクト
* **Boat** (ボート) - 取引先責任者が所有するボートに関する情報。このオブジェクトには、ボートがいつも利用する波止場を地図上にプロットするための地理位置情報項目があります。このオブジェクトは、標準の取引先責任者オブジェクトと主従関係にあり、BoatType (ボート種別) オブジェクトへの参照関係項目があります。
* **BoatType** (ボート種別) - 漁船、モーターボード、ヨット、パーティボートのような、様々なボートの種類。
* **BoatReview** (ボートレビュー) - ボートのコメントと評価。

### エンティティ図
設定から、クイック検索ボックスに`スキーマビルダー`と入力し、**スキーマビルダー**を選択し、インタラクティブなバージョンの画像を表示します。詳しくは、[データモデリング](https://trailhead.salesforce.com/ja/modules/data_modeling) モジュールの「スキーマビルダーの使用」単元を参照してください。

![](prework_entity_diagram.jpg)
 
### アプリケーション設計
HowWeRoll の主要なステークホルダとのミーティングに費やした時間はあなたにとって価値がありました。次のような Lightning ページの設計図を考え出しました。

![](prework_final_product.jpg)

これからのタスクの大きさを見積した後、あなたは一杯のコーヒーを飲み、そして大きなタスクを乗り越えるための最良の方法はそれをより小さな部品に分割することであると判断します。次の 9つのフェーズを計画します。それらが完了すると、確かな完成品となります。
  
## 検索フォームを構築する
100 万海里の旅は、1 行のコードから始まりますよね？

Search (検索) ボタンと New (新規) ボタンとともに、ボート種別を一覧表示するドロップダウンリスト付きのフォームを表示して、あなたの旅のエンジンを稼働させましょう。フォームのコンポーネントには、ドロップダウンリストとボタンが含まれています。

![](figure1_1.jpg)<br>図 1.1 : 例示による問い合わせインタフェースの構築

フォームを構築するには、次のコンポーネントを作成してください。図 1.1 では、各コンポーネントが対応する番号で強調表示されています。

1. **BoatSearchForm.cmp** - ユーザがドロップダウンメニューを使用してボート種別で結果をフィルタするためのフォーム。最初のデフォルト値として空の文字列を使用し、**All Types** (すべての種別) というラベルを付けます。`<lightning:layout>` コンポーネントと `horizontalAlign` 属性を使用してドロップダウンメニューと中央揃えになる、青いバリアントの `Search` (検索) ボタンと、白いバリアントの `New` (新規) ボタンを含めてください。ユーザが新規ボタンをクリックすると、コントローラ関数が適切なイベントを発生させて新しいボートのレコードを作成します。ボート種別が選択されている場合は、新しいボートのレコードはデフォルトで選択されたボート種別が設定されます。フォームのコントローラは、ベストプラクティスに従って、`e.force:createRecord` イベントがスタンドアロンアプリケーションでサポートされているかどうかを確認し、新規ボタンを表示または非表示にします。ユーザが検索ボタンをクリックしても、「**検索フィルタを実装する**」のフェーズまで機能が実装されていないため、何も起こりません。
2. **BoatSearchResults.cmp** - このコンポーネントは、最終的にはマッチするボートをレスポンシブレイアウトで表示しますが、ここでは空のままにします。
3. **BoatSearch.cmp** - `BoatSearchForm.cmp`と`BoatSearchResults.cmp`の両方を呼び出し、Lightningカードコンポーネントでそれぞれをラップし、タイトルがそれぞれ **Find a Boat** (ボートの検索)と **Matching Boat** (マッチするボート)となるコンテナコンポーネント。BoatSearchFormコンポーネントと BoatSearchResultsコンポーネントを視覚的に区別するために、Find a Boatのカードに**10px**の余白(margin-bottom)を追加します。

「メインの範囲と右サイドバー」のレイアウトを使用する**Friends with Boats**という名前の Lightningページを作成します。`BoatSearch`コンポーネントをメインの列に配置します。Lightning Experienceおよび Salesforceアプリケーションで、その Lightningページを新しいタブとして有効化します。最後に、その Lightningページと同様のレイアウトで、URLから直接アクセスできる`FriendswithBoats.app`という名前の Lightningアプリケーションを作成します。`<lightning:layout>`を使用してアプリケーションのレイアウトを生成し、Lightning Design Systemのスタイルがアプリ内のコンポーネントに適用されるようにしてください。

![](figure1_2.jpg)<br>図 1.2 : 検索フォームの始まり
  
次に、フィルタされていない検索結果をレスポンシブレイアウトで表示することを始めましょう。

## 検索結果を追加する
ボート種別の一覧を見るのは楽しいことで、私たちの美しいボートの写真を披露する時が来ました！このフェーズの終わりには、HowWeRoll の在庫のうち、すべてのボートのフィルタされていないリストが、あなたが作成しているページに表示されているでしょう。

![](figure2.jpg)<br>図 2 : `BoatSearchResults` コンポーネント(1) は、Apex メソッドによって返されたデータをループ処理し、`BoatTile` コンポーネント(2) を生成する

Lightning コンポーネント `BoatTile.cmp` を作成してください。コンポーネントには `boat` という名前で  Boat__c 型の属性があり、貸し出すボートが表示されます。テーマ化された `lightning:button` でタイルを実装します。`lightning:button` の `class` 属性に `tile` を割り当てます。BoatTile.cmp 内にボートの写真を表示する方法のガイドとして、次のマークアップと CSSを使用してください。

**マークアップ**
```HTML
<lightning:button [more code here] >
<div style="[set image as background here]" class="innertile">
  <div class="lower-third">
   <h1 class="slds-truncate">[output contact name here]</h1>
  </div>
</div>
</lightning:button
```

**CSS**
```CSS
.tile {
    position:relative;
    display: inline-block;
    width: 100%;
    height: 220px;
    padding: 1px !important;
}
.innertile {
    background-size: cover;
    background-position: center;
    background-repeat: no-repeat;
    width: 100%;
    height: 100%;
}
.lower-third {
    position: absolute;
    bottom: 0;
    left: 0;
    right: 0;
    color: #FFFFFF;
    background-color: rgba(0, 0, 0, .4);
    padding: 6px 8px;
}
```

検索結果を取得するには、Apexクラスの`BoatSearchResults`を使用します。このクラスは、`String`型の`boatTypeId`を引数として受け取り、その Idでフィルタされたボートのリストを返すメソッド`getBoats()`を使用します。ユーザが「All Types (すべての種別)」を選択すると、空の文字列がこのメソッドに渡され、すべてのボートが返されます。

`BoatSearchResults.cmp`は、`onSearch()`という名前のヘルパーメソッドを使用して BoatSearchResultsによって返されたデータを取得します。このメソッドは、検索結果を`boats`というコンポーネントの属性に格納します。次に、`BoatSearchResults.cmp`は結果をループし、それぞれのボートを`BoatTile.cmp`として表示します。図 2に示すように、複数行がレスポンシブなグリッドに配置されます。`<lightning:layout>`を使用して、複数行のレイアウトを作成してください。

Apexクラスが結果を返さない場合は、`BoatSearchResults.cmp`の縦横中央に「No boats found」というメッセージを表示してください。

次のセクションで、検索フィルタを機能させます。

## 検索フィルタを実装する
セーリングをしたい人、釣りをしたい人、そして単に楽しんでいる人もいます。検索フォームから結果コンポーネントまでをつなげることで、担当者が顧客の望むボートを見つけやすくします。

![](figure3.jpg)<br>図 3 : 検索フィルタの実装。ボート種別を選択して検索ボタンをクリックすると、結果が絞り込まれる

続いて、3つのコンポーネントを修正して、boatTypeIdが次のパスをたどるようにします。

 `BoatSearchForm -> BoatSearch -> BoatSearchResults -> Apex`

`formData`という名前で`Object`型の属性を持つ新しいイベント`c:FormSubmit`を作成して、`formsubmit`というイベント名で、選択された`boatTypeId`を`formData`のプロパティとして`BoatSearchForm`から、その親コンポーネント`BoatSearch`に渡します。これを行うには、検索ボタンに付属する`onFormSubmit()`というコントローラメソッドを使用します。

`BoatSearch`コンポーネントでは、`onFormSubmit`という名前のコントローラアクションを使用して`FormSubmit`イベントを処理します。`formData.boatTypeId`をコントローラから`BoatSearchResults`コンポーネント上の`search`という publicメソッドに渡します。

`search`メソッドからコントローラメソッド`doSearch`を呼び出します。このメソッドは、メソッドの引数から`boatTypeId`パラメータを取得し、コンポーネントの`boatTypeId`属性にその値を設定します。次に、ヘルパーメソッド`onSearch()`を呼び出します。これは、新しく更新された`boatTypeId`コンポーネント属性を取得し、それをサーバに渡してボートのリストを要求します。これで、ボートのリストを表示し、ボートのカテゴリを選択して**Search**をクリックすることでそれをフィルタできます。

## 選択されたボートを強調表示する
ボートのリース契約を締結してもらうには、HowWeRollのセールスチームは単に美しい写真をいくつか表示する以上のことをする必要があります。彼らはこれらすべてのボートの詳細にすばやくアクセスする必要があります。しかし最初に、彼らは自身が見ているボートを知る必要があります。

コンポーネント間の通信によって切り替えられるコンポーネント属性に連動して、単純な CSSルールを使用してユーザがどのボートを選択しているかを明確にします。これを達成するには、もう 1つイベントを作成し、`BoatTile`と`BoatSearchResults`コンポーネントを修正します。

![](figure4.jpg)<br>図 4 : ボートをクリックすると、ボートタイルの周囲に青い枠線(1)が配置される

まず、`BoatTile`コンポーネントを修正します。デフォルト値 `false`を持つ`selected`という名前の Boolean型属性を追加します。タイルの `lightning:button`で、三項演算子を用いて、`class`属性に、`v.selected`が trueなら `tile selected`を、`v.selected`が falseなら `tile`を設定します。コンポーネント CSSの`selected`クラスセレクタで、borderプロパティに次の値を指定します。`3px solid rgb(0、112、210); `

続けて、`BoatTile`の`lightning:button`にコントローラ関数`onBoatClick`を呼び出すクリックハンドラを定義します。`onBoatClick`の中で、`BoatTile`に登録された`BoatSelect`と呼ばれる新しいイベントを発生させ、そのイベントを使って`boatId`を `BoatSearchResults`コンポーネントに送ります。

`BoatSearchResults`は `onBoatSelect`という名前のコントローラ関数を呼び出すことで`BoatSelect`イベントを処理しなければなりません。それはイベントを通して渡された`boatId`を、コンポーネント属性の`selectedBoatId`に格納します。`boat`という名前の繰り返し変数を使い、`BoatTile`の `BoatSearchResults`呼び出しで、三項演算子を用いて、現在出力されている`boat.Id`がコンポーネントの`selectedBoatId`属性に格納されている値と同じかどうかに基づいて、`selected`属性に`true`または `false`の値を設定します。

## ボートの詳細を表示する
どのボートを見ているのかが明確になったので、選択したボートの詳細を表示しましょう。タブセットを持つ親コンポーネント`BoatDetails`を作成します。詳細タブ内で新しい子コンポーネント`BoatDetail`をインスタンス化します。Lightning Data Serviceを使用して、情報が正しくロードされ、アプリケーションの残りの部分と同期していることを確認します。

![](figure5_1.jpg)<br>図 5.1 : `BoatTile`コンポーネント(1)は、`BoatDetails`コンポーネント(2)が処理するイベントを起動し、`BoatDetail`コンポーネント(3)の表示が更新される

`BoatDetails`コンポーネントは Lightningページの右上のサイドバーに配置されています(図 5.1参照)。これには 2つの public属性があります。`boat`(Boat__c型)と`id`(Id型)です。コンポーネントは**Details** (詳細)、**Reviews** (レビュー)、**Add Review** (レビューを追加)というラベルの付いた 3つのタブを出力しますが、コンポーネントの `boat`属性が`undefined`の場合はタブセットを非表示にします。

`BoatTile`コンポーネントの`onBoatClick`ハンドラを更新して`BoatSelected`と呼ばれる新しいイベントを発生させ、`Boat__c`型の選択された`boat`を渡します。

`BoatSelected`イベントがアプリケーション内の他の場所から発生したとき、`BoatDetails`コンポーネントは `onBoatSelected`という名前のコントローラ関数を実行しなければなりません。`onBoatSelected`は`BoatDetails`コンポーネントの `id`属性をイベントと共に送信されたボートの idに設定します。

`BoatDetails`コンポーネントは`force:recordData`の`targetFields`構文を`aura:id="service"`とともに使用して、`BoatDetails`コンポーネントの`id`属性に基づいて、以下の項目を `Boat__c`オブジェクトからコンポーネントの`boat`属性にロードします。

- Id
- Name
- Description__c
- Price__c
- Length__c
- Contact__r.Name
- Contact__r.Email
- Contact__r.HomePhone
- BoatType__r.Name
- Picture__c
  
`force:recordData`は、後のフェーズで使われる`onRecordUpdated`という名前の空のコントローラ関数を呼び出します。`BoatDetails`の`onBoatSelected`関数は Lightningデータサービスに指定されたレコードを強制的にリロードさせます。

`BoatDetail`コンポーネントは`BoatDetails`コンポーネントの Detailsタブ内で使用され、Boat__c型の属性 `boat`を付けて呼び出されます。それは `utility:anchor`アイコンと`<lightning:layout>`を使って作られた 2列のレイアウトを持つ`lightning:card`を使います。左側の列にはボートに関するテキスト情報が表示され、右側の列にはボートの画像が表示されます。コンポーネントは、次のマークアップと CSSを使用して、Price(価格)項目に米国の通貨形式を使用してボート情報を表示し、Description(説明)項目では埋め込み HTMLが許可してください。

**マークアップ (左側の列)**
```HTML
<div class="slds-p-horizontal--small">
    <div class="boatproperty">
        <span class="label">Boat Name:</span>
        <span></span>
    </div>
    <div class="boatproperty">
        <span class="label">Type:</span>
        <span></span>
    </div>
    <div class="boatproperty">
        <span class="label">Length:</span>
        <span> ft</span>
    </div>
    <div class="boatproperty">
        <span class="label">Est. Price:</span>
        <span></span>
    </div>
    <div class="boatproperty">
        <span class="label">Description:</span>
        <span></span>
    </div>
</div>
```

**マークアップ (右側の列)**
```HTML
 <div class="imageview" style="[set image as background here]" />
```

**CSS**
```CSS
.label {
    font-weight: bold;
    display: block;
}
.boatproperty {
    margin-bottom: 3px;
}
.imageview {
    background-repeat: no-repeat;
    background-size: contain;
    height: 200px;
    margin: 2px;   
}
```
カードのヘッダには、ボートの取引先責任者の名前と「's Boat」の文字列を連結して表示します。カードの actionsセクションは**Full Details** (完全な詳細を表示)のラベルで`lightning:button`を出力します。このボタンは`onFullDetails`という名前のコントローラメソッドを呼び出して、ユーザをボートのデフォルトの詳細ページにリダイレクトするための適切なイベントを発生させます。ただし、Full Detailsボタンは、イベントがデプロイメントプラットフォームで利用可能な場合にのみ表示してください。

![](figure5_2.jpg)<br>図 5.2 : タブセットを作成し、タブの 1つにボートの詳細表示を実装する

この時点で、ボートをブラウズしたりフィルタしたり、ボートの詳細を表示したりできます。次に、レビューを追加して表示し、セキュアな JavaScriptを書いて、ボートを地図にプロットします。

## ボートのレビューを追加する
HowWeRoll自身がすべてのボートを所有しているわけではないので、役に立たないものを取り除くことができるように、顧客にボートを貸し出すとき、ポジティブな体験とネガティブな体験を追跡することは重要です。各ボートのレビューを送信する機能を追加してこの目的を達成します。

**Submit** (送信) をクリックすると、以下のアクションが実行されます。
* BoatReview__cオブジェクトの新しいレコードを作成します (Lightning Data Serviceを使用) 。
* 送信が成功したことを示すトーストメッセージを表示します。
* まだ何も表示されませんが、Reviewsタブをアクティブにします。

![](figure6.jpg)<br>図 6 : Add Reviewタブのフォーム

### フォームを構築する
`BoatDetails` コンポーネントの Add Reviews (レビューの追加) タブでは、新しいコンポーネント `AddBoatReview` をインスタンス化し、コンポーネントの Boat__c 型の public 属性 `boat` を使用してボートのデータを渡します。コンポーネントは SLDS を使用してすべてのフォーム項目が垂直に配置されるようにフォームレイアウトを定義します。Title 項目と Description 項目は適切な Aura コンポーネントを使用し、コンポーネントの `BoatReview__c` 型の private 属性 `boatReview` の `Name` プロパティと `Comment__c` プロパティにバインドされます。Description 項目のリッチテキストエディタでは、フォント選択オプションは表示されないようにしてください。送信ボタンは `utility:save` アイコンを使用してコントローラメソッド `onSave` を呼び出します。Rating (評価) 項目は、「**サードパーティスクリプトの統合**」フェーズまで追加しません。

### 新しいBoatReviewレコードを作成する
このコンポーネントは、Lightning Data Serviceを利用して BoatReview__cレコードを作成します。データサービスの呼び出しには`force:recordData`の targetFields構文を使用し、aura:idに`service`と設定し、`boatReview`属性を参照します。boatReview属性の対象の項目は Id、Name、Comment__c、Boat__cです。レコードが更新されると、このセクションの後半で詳しく説明するように`onRecordUpdated`という名前のコントローラ関数が呼び出され、`recordError`という名前の privateコンポーネント属性を使用してデータサービスのエラーを書き込みます。

コンポーネントの初期化時に、`AddBoatReview`は、コンポーネント、イベント、およびヘルパーを引数として、コントローラー関数`doInit()`を介して`onInit()`という名前のヘルパー関数を呼び出します。`onInit()`関数は Lightning Data Serviceの適切なメソッドを呼び出して、新しい BoatReview__cのレコードテンプレートを取得します。その結果が boatReviewコンポーネント属性に格納されます。そのレコードの Boat__cプロパティを、コンポーネントに渡されたボートの Idに設定します。`console.log()`コマンドを使用して、エラーデータをブラウザの JavaScriptコンソールに書き込みます。

`onSave()`コントローラ関数は、Lightning Data Serviceを使用してレコードを保存します。レコードが保存された後、`force:showToast`イベントがサポートされていれば、トーストメッセージが表示されます。`force:showToast`がサポートされていない場合は、JavaScriptの`alert()`メソッドを使用してメッセージを表示します。最後に、`helper.onInit()`を呼び出してコンポーネントをリセットし、ユーザが別のレビューを追加できるようにします。`onSave()`コントローラ関数と同様に、`onRecordUpdated()`コントローラ関数は、トーストメッセージまたは JavaScriptアラートを使用して、レコードが更新されたことをユーザに通知します。

### タブフォーカスをレビュータブに変更する
レビューが正常に保存されると、`BoatReviewAdded`という新しいイベントが親コンポーネントの BoatDetailsに返されます。親コンポーネントは、このイベントをリスンし、`onBoatReviewAdded`という名前のコントローラ関数を呼び出し、現在選択されているタブを Reviewsタブ(id属性が boatreviewtab)に設定します。

## ボートのレビューを表示する
ユーザがレビューを追加できるようになりました。次はそれを表示しましょう。
![](figure7.jpg)<br>図 7: ボートのレビュー


### コンポーネントを定義する
`BoatDetails`コンポーネントの Reviewsタブは新しいコンポーネントである`BoatReviews`をインスタンス化し、選択されたボートの情報を`boat`という名前の Boat__c型の public属性に渡します。

### 選択されたボートのレビューを読み込む
Apexクラスの`BoatReviews`は、`Id`型の**boatId**という名前の引数を受け入れ、BoatReviewカスタムオブジェクトからの以下のフィールドを含むボートレビューのリストを返す**getAll()** という名前の関数を定義します。

- Id
- Name
- Comment__c
- Rating__c
- LastModifiedDate
- CreatedDate
- CreatedBy.Name
- CreatedBy.SmallPhotoUrl
- CreatedBy.CompanyName

`BoatReviews`の Lightningコンポーネントは BoatReview__cの配列として`boatReviews`という名前の privateコンポーネント属性を含みます。コンポーネントの initハンドラはコントローラ関数 `doInit()`を通してヘルパー関数 `onInit()`を呼び出します`onInit()`関数は Apexと通信し、結果をコンポーネントの `boatReviews`配列属性に入れ、Apexエラーを適切に処理します。

### ボートのレビューを出力する
ボートのレビューの出力は、Lightning Design Systemの[フィードコンポーネント](https://lightningdesignsystem.com/components/feeds/)に基づいています。`BoatReviews`コンポーネントで、Salesforceアプリケーションでネイティブスクロールを可能にする Lightningコンポーネントを使用して、最大高さ 250ピクセルの独立したスクロール領域を定義します。レビューが見つからない場合は、スクロール可能領域内の縦横中央位置に「No reviews available」というテキストが出力されます。ボートのレビューが見つかった場合は、`boatReview`という名前の繰り返し変数を使用し、図 7で示すように、`BoatReview.getAll()`関数で指定されたすべての項目を、Lightning Design Systemのフィードコンポーネントに記述されているものと同様のマークアップで出力します。
  
レビューを残した人についてもっと知りたいときがあるため、CreatedBy名はハイパーリンクされ、 `onUserInfoClick()`と名付けられたコントローラ関数を呼び出します。リンクは`boatReview.CreatedBy.Id`の値を保持する`data-userid`属性を含みます。`onUserInfoClick()`関数はハイパーリンクにエンコードされた `data-userid`属性から値を取得し、ユーザにレビューの作成者の詳細ページを表示させるイベントを発生させます。
  
### プログラムで出力を更新する
ユーザが別のボートを選択したり、新しいレビューを追加したりするたびに、コンポーネントの出力を更新する必要があります。コンポーネントには、コンポーネントの`boat`属性の値が変更されたときはいつでも Apexからデータをリロードするイベントハンドラがあります。コンポーネントの `doInit()`コントローラメソッドを呼び出す publicメソッド`refresh`を定義します。`refresh()`メソッドは `BoatDetails.onBoatReviewAdded()`メソッドと `BoatDetails.onRecordUpdated()`メソッドから呼び出されます。

## サードパーティのスクリプトを統合する
あなたは前向きな思考の持ち主です。HowWeRollの在庫が何千ものボートまで増えたとき(ちょっと、悲観主義者であるとあなたを非難する人は誰もいません！)、あなたは一目であなたの最高のボートのリストを見ることができる必要があります。最初から始めるのではなく、仲間によって開発されたスクリプトから始めます。ご存知のように、優れたプログラマは優れたコードを書きますが、優れたプログラマは優れたプログラマのコードを再利用します。このスクリプトは 5つ星の評価尺度を実装しています。残念なことに、あなたの仲間はスクリプトを完全に終えていなかったので、あなたはいくつかの詳細を埋めなればなりません。

![](figure8_1.jpg)<br>図 8.1 : AddBoatReviewコンポーネントの**edit**(編集) モードの`FiveStarRating`コンポーネント

このフェーズでは、`FiveStarRating`コンポーネントを作成します。これにより、ユーザは金色の星をクリックして評価を割り当てることができます(図 8.1を参照) 

![](figure8_2.jpg)<br>図 8.2 : `BoatReview`コンポーネントの読み込み専用モードの`FiveStarRating`

図 8.2に示すように、コンポーネントには評価を出力しますがクリックはできない、読み取り専用モードもあります。

### コンポーネントを作成する

最新のコンポーネントである FiveStarRatingには、`read-only`属性(Boolean型でデフォルト値は false)と`value`属性(Integer型でデフォルト値は 0)があります。静的リソースの`fivestar`から rating.cssファイルおよび rating.jsファイルをその中にロードします。スクリプトがロードされたら、`afterScriptsLoaded`という名前のコントローラ関数を呼び出します。

`onValueChange`という名前のコントローラ関数を呼び出す changeイベントリスナを追加します。これは、コンポーネントの`value`属性が変更されたときに発生します。aura:idが`ratingarea`であり、三項演算子を使用して readonly属性の値に応じてその class属性を`c-rating`または`readonly c-rating`に設定する`<ul>`タグをコンポーネントに追加します。

コントローラロジックの基礎として次のコードを使用してください。プレースホルダを適切なコードに置き換えてください。

```Javascript
afterScriptsLoaded : function(component, event, helper) {
    // var domEl = [get dom element of rating area]
    // var currentRating = [get value attribute of component]
    // var readOnly = [get readonly attribute of component]
    var maxRating = 5;
    var callback = function(rating) {
    component.set('v.value',rating);
    }
    component.ratingObj = rating(domEl,currentRating,maxRating,callback,readOnly); 
},
onValueChange: function(component,event,helper) {
     if (component.ratingObj) {
        var value = component.get('v.value');
        component.ratingObj.setRating(value,false);
    }
}
```

### コンポーネントを配置する
`AddBoatReview`コンポーネントと`BoatReviews`コンポーネント内で作成したコンポーネントをインスタンス化します。コンポーネントの valueは、BoatReviewカスタムオブジェクトの Rating__c項目にバインドされます。

## 地図にマーカーをプロットする
リース契約を締結すると、HowWeRollのクライアントは、リースしているボートをピックアップする場所を知る必要があります。あなたの開発のグランドフィナーレに向けて、ボートがどこに停泊するかを示すために地図プロットコンポーネントを開発し、そしてアプリケーションのどこからでも `PlotMapMarker`イベントをリスンするためにコンポーネントを更新します。

![](figure9.jpg)<br>図 9 : BoatTileコンポーネントをクリックすると(1)、PlotMapMarkerイベントが発生し、緯度と経度が渡されます。Mapコンポーネント(2)は PlotMapMarkerイベントをリスンし、指定された緯度と経度にマーカーを配置する

Mapコンポーネントとそのコントローラは、このスーパーバージの事前準備の一部としてインストールした未管理パッケージに含まれているので、いくつか変更を加えるだけで済みます。始める前に、コンポーネントに付属している各ファイルを調べて、それがどのように機能するかを理解してください。

ビジネスユーザがマップコンポーネントの幅と高さを設定できるようにするデザインリソースを作成します。次に、図 9に示すように、右サイドバーの BoatDetailsコンポーネントの下に、Mapコンポーネントを Lightningページに追加します。aura:idをmap、タイトルを**Current Boat Location** とした<lightning:card>で<div>をラップすることにより、Mapコンポーネントを更新します。UIをページ上の他の要素と一致させるため。地図の 1ピクセルの点線枠を削除します。次に、sObjectId、lat、long、および labelの4つの String型の属性を含む、新しい`PlotMapMarker`イベントを作成します。ユーザが BoatTileコンポーネントからボートをクリックしたときにイベントが発生しますが、このコンポーネントはアプリケーション内の他のコンポーネントからのイベントもリスンします。PlotMapMarkerのイベントリスナで、イベントによって渡された緯度と経度を使用してボートの位置を更新します。

## Challenge
### Challenge 1: はじめる前に
未管理パッケージのインストールを含めた全ての事前準備を完了してください。

### Challenge 2: 例示による問合せフォームを作成する
ビジネス要件で説明されているように、**BoatSearchForm.cmp**、**BoatSearchResults.cmp**、および**BoatSearch.cmp**を使用して、**Search**ボタンと**New**ボタンと共に各ボート種別を一覧表示するドロップダウンを表示するフォームを作成します。

これらの Lightningコンポーネントを**Friends with Boats**という名前の Lightningページに追加し、そのページを Lightning Experienceおよび Salesforceアプリケーションの新しいタブとしてアクティブにします。最後に、Lightningページに似たレイアウトを持つ**FriendswithBoats.app**という名前の Lightningアプリケーションを作成します。

### Challenge 3: BoatTileおよびBoatSearchResultsコンポーネントを実装する
新しい**BoatTile**コンポーネントを作成し、コンテナコンポーネントである**BoatSearchResults**を更新して、Apexコントローラの**BoatSearchResults**から返されたすべての結果をループ処理して、HowWeRollがリースするすべてのボートのフィルタされていないリストを表示します。

ビジネス要件で説明されているように検索結果を返すには、**BoatSearchResults**クラスでメソッド**getBoats()** を定義します。**BoatSearchResults.cmp**は、検索結果をヘルパーメソッドの**onSearch()** で表示し、各結果を**BoatTile**コンポーネントとして表示します。

### Challenge 4: 検索フィルタを実装する
選択されたボート種別を**BoatSearchForm**から**BoatSearchResults**コンポーネントに渡すことができるように**FormSubmit**イベントを作成します。BoatSearchResultsコンポーネントは、Apexに問い合わせて結果を保存します。
  
**FormSubmit**をコントローラアクション**onFormSubmit**で処理し、**formData.boatTypeId**をコントローラから、**BoatSearchResults**コンポーネントの publicメソッドである**search**に渡します。search関数は、ボートのリストを取得するために、ヘルパー関数**onSearch()** とコントローラー関数**doSearch()** を使用します。

### Challenge 5: 選択されたボートを強調表示する
**BoatTile**がクリックされたときに新しい**BoatSelect**イベントを発生させます。これは**BoatSearchResults**に**selectedBoatId**を設定し、要件に示されているように、選択されたボートの周囲に濃い青の境界線を表示する CSSクラスの追加をトリガすることで、正しい**BoatTile**の**selected**属性を切り替えます。

これを行うには、BoatTileの**lightning:button**にクリックハンドラを定義し、コントローラー関数**onBoatClick**を呼び出して、ビジネス要件に示されているように**BoatSelect**イベントを発生させます。

### Challenge 6: ボートの詳細を表示する
**BoatDetails**と**BoatDetail**の 2つの新しいコンポーネントと、新しいイベント**BoatSelected**を作成します。BoatTileから新しいイベントを発生させ、Lightning Data Serviceを利用してボートの詳細を出力します Lightningページの右上隅に**BoatDetails**コンポーネントを配置します。

### Challenge 7: ボートのレビューを追加する
Add Reviewsタブで**AddBoatReview**コンポーネントをインスタンス化してフォームを表示します。ユーザが**Submit**をクリックしたら、Lightning Data Serviceを使用してレコードを保存し、**BoatReviewAdded**イベントを発生させます。このイベントは、**BoatDetails**親コンポーネントでリスンされ、アクティブなタブを Reviewsタブに切り替えることができます。レビューを表示することについてはこの時点では心配する必要がありません。

### Challenge 8: ボートのレビューを表示する
Reviewsタブ内で、ビジネス要件に示すように、Apexに問い合わせて、Lightning Design Systemの**Feeds**コンポーネントに基づいて結果を出力する**BoatReviews**コンポーネントを呼び出します。可能な場合は、ユーザの名前に、Salesforceのユーザレコードの詳細ページへのハイパーリンク作成します。

### Challenge 9: サードパーティのスクリプトを統合する  
同僚が修正した JavaScriptを使用して**FiveStarRating**コンポーネントを作成し、担当者が 1〜5つ星の評価をボートに付与できるようにします。formとoutputで使用されているコンポーネントにそれぞれ、**edit**と**read**モードを与えます。

### Challenge 10: 地図にマーカーをプロットする
ボートがどこに停泊するかを示すためにマップのコンポーネントを配置します。**Map**コンポーネントとそのコントローラは、このスーパーバッジの一部としてインストールした未管理パッケージに含まれていました。コンポーネントは**PlotMapMarker**イベントをリスンします。これは、ユーザがボートをクリックしたときに**BoatTile**コンポーネントから発生します。

## 訳注
* <a name="footnote1">[1]</a> : [エアストリーム (Wikipedia日本語版)](https://ja.wikipedia.org/wiki/%E3%82%A8%E3%82%A2%E3%82%B9%E3%83%88%E3%83%AA%E3%83%BC%E3%83%A0)

## ヒント

### Challenge 2
* [Lightning 基本コンポーネントの使用](https://developer.salesforce.com/docs/atlas.ja-jp.lightning.meta/lightning/lightning_overview.htm)
* [Salesforce モバイルアプリケーションと Lightning Experience で処理されるイベント](https://developer.salesforce.com/docs/atlas.ja-jp.lightning.meta/lightning/events_one.htm)

### Challenge 3
* [Alignment - Lightning Design System](https://www.lightningdesignsystem.com/utilities/alignment/)
