# Lightning Experience Rollout Specialist
[![](https://img.shields.io/badge/-view%20on%20gitbook-blue?logo=markdown)](https://shunkosa.gitbook.io/trailhead-superbadge-jp/lex-rollout-specialist) [![](https://img.shields.io/badge/-view%20on%20github-black?logo=github)](https://github.com/shunkosa/trailhead-superbadge-jp/blob/master/src/lex-rollout-specialist/lex-rollout-specialist.md)
* Trailhead のスーパーバッジ、[Lightning Experience Rollout Specialist](https://trailhead.salesforce.com/content/learn/superbadges/superbadge_lex_rollout) の日本語訳(**非公式**)です。
* 各カスタマイズ要素のラベル部分には補足として日本語を括弧内に記載している場合がありますが、正解チェックは英語のラベルを元に行われるため、実際のチャレンジには日本語表記を含めず、英語表記のみを使用して行って下さい。また、チャレンジ前にユーザと組織の言語・ロケールを英語に切り替えておくことを推奨します。

---
## このスーパーバッジを取得するためにすること
1. 開発者、管理者、およびユーザに対する Lightning Experience の価値提案を明確にする
2. Lightning Experience 準備状態チェックのレポートおよび Salesforce オプティマイザレポートを解釈する
3. Lightning Experience をロールアウトする
4. Lightning アプリケーションのナビゲーションスタイルをカスタマイズして、重要なデータにすばやくアクセスできるようにする
5. Lightning のレポートとダッシュボードを設定する
6. ホームページ、レコードページ、およびアプリケーションページをカスタマイズする
7. ドキュメントをファイルに移行する
8. Lightning ナレッジを設定する

## このスーパーバッジでテストする概念
* Lightning Experience のユーザインタフェース
* Lightning Experience のロールアウトのベストプラクティス
* Lightning Experience のレポートとダッシュボード
* Lightning Experience のセールスとサービスの機能
* Lightning Experience のホームページ・レコードページ・アプリケーションページのカスタマイズ

## 事前準備とメモ
* 要件を読み進める際にメモを取ってください(映像記憶がない限り)。紙とペン(または電子的なものでも)を用意しましょう。
* このスーパーバッジ用に、新しい Trailhead Playground を作成してください。既存の組織を利用すると、Challenge について検証する際に問題を引き起こす可能性があります。Trailhead Playground では既に私のドメインが有効化されていることに注意してください。私のドメインの設定は変更しないでください。
* [この未管理パッケージ](https://login.salesforce.com/packaging/installPackage.apexp?p0=04t0Y0000025Nb3)をインストールしてください。(パッケージ ID: 04t0Y0000025Nb3) パッケージには、課題を完了するためのスキーマが含まれています。管理パッケージ、未管理パッケージ、アプリケーションを  AppExchange からインストールする際に問題が発生した場合は、[この記事](https://force.desk.com/customer/en/portal/articles/2710899-installing-a-package-or-app-to-complete-a-trailhead-challenge?b_id=13478)に示す手順に従ってください。
* Trailhead Playground は Lightning Experience で開きますが、事前準備の設定作業のため、Salesforce Classic に切り替える必要があります。課題で指定された機能を設定・テストするため、Lightning Experience と Salesforce Classic を行ったり来たりする必要があるでしょう。
* このスーパーバッジの課題のために、Trailhead Playground を準備してください。
  1. Salesforce Classic の設定から、取引先のタブを、先ほどインストールしたスーパーバッジのパッケージに含まれている、Accounts Tab Visualforce ページで上書きします。
  2. Salesforce Classic の設定で、TrailheaDX コンポーネントを DE Default ホームページレイアウトに追加してください。
  3. Salesforce Classic または Lightning Experience の設定で、John Wiseman という名前のユーザを作成し、Salesforceユーザライセンスと Custom: Sales Profile プロファイルを割り当ててください。
  4. Paloma Espinoza という名前で 2人目のユーザを作成し、Salesforce Platform ユーザライセンスと Standard Platform User プロファイルを割り当ててください。
* 課題をうまく完了するため、ビジネス要件および技術要件の章に記載されている命名規則を適用してください。

## ユースケース
点 A から点 B へ移動するのに靴を履く人もいれば、点 A・点 B・点 Cで見られるために靴を履く人もいます。Lusso Scarpe (ルッソ スカルペ)の顧客は最も確実に 2番目のカテゴリに分類されます。Lusso は、厳選されたブランドのデザイナーフットウェアをオンラインおよび高級ブティックで販売しており、そのすべてのセールスおよびサービス業務に Salesforce を使用しています。

Lusso Scarpe は、卸売事業部門も成功しています。しかし、いくつかの主要セグメントを特にターゲットとした多数の新しい競合企業がいます。一般消費者向けオンラインビジネスは、ロイヤリティの高い顧客グループを抱えていますが、市場全体よりもゆっくり成長しています。

生産性を向上させる新機能が満載の Salesforce Lightning Experience は、これらの課題を乗り越えるための Lusso Scarpe の戦略の重要な要素です。

あなたは、Salesforce のすべてのニーズについて Lusso Scarpe にコンサルティングをする幸運なスペシャリストです(そして、非常に人気のある従業員割引を受けられます)。今回の任務は<sup>[*1](#footnote1)</sup>、会社の組織を Salesforce Classic から Lightning Experience に移行することです。

会社ができるだけスムーズにロールアウトできるようにするだけでなく、営業担当者とサービス担当者が生産性を向上させる新機能を使用して迅速に対応できるようにします。

Lusso の人々は贅沢に慣れています。彼らに最高のサービスを提供しましょう。

### 標準オブジェクト
Lusso Scarpe はデータを保管するため Salesforce の標準オブジェクトを利用しています。以下が取り組むことになるオブジェクトです。

- Account (取引先) - 再販業者や供給元を含む、Lusso Scarpe がビジネスを行う企業
- Contact (取引先責任者) - Lusso Scarpe の取引先における直接の顧客または従業員
- Opportunity (商談) - 潜在的な卸売取引
- Campaigns (キャンペーン) - 主にオンラインの顧客を対象としたターゲットマーケティング活動
- Cases (ケース) - 取引先からの問い合わせや苦情

Lightning Experience のロールアウト戦略には、リレーションまたはオブジェクトをスキーマに追加するための計画は含まれていません。わざわざ複雑にはしませんよね？

### Lightning Experience の評価
Lusso Scarpe に Lightning Experience をロールアウトするための要件を定義するために、現在の実装が新しいインターフェイスでどのように機能するかを評価し、機能のギャップや対処する必要のある問題があるかどうかを確認しましょう。
#### Lusso Scarpe がどれくらい準備できているか確認する
有能な Lightning Experience のロールアウトスペシャリストの最初の作業の 1つは、[Lightning Experience の準備状態チェック](https://help.salesforce.com/articleView?id=lex_readiness_check_kick_off.htm&type=5)を実施することです。まさにそれを実施するために設計された自動化ツールがあるとき、問題を探すために手作業で組織を綿密にチェックする人はいませんよね？

結果のレポートを確認して、切り替えの準備ができているユーザ、行ってもよい機能とカスタマイズ、および解決する必要がある可能性のある技術的な問題を把握しましょう。

#### 大掃除にあわせてロールアウトを簡略化する
[Salesforce Optimizer](https://help.salesforce.com/articleView?id=optimizer_kick_off.htm&type=5)は、すべて複雑さの軽減に関係しているため、ロールアウトのためのもう 1つの優れたツールです。そして、ユーザに合理化された効率的なエクスペリエンスを提供します。(それに加えて、あなたにはあまり仕事がないので、ボーナスです。)
Optimizer を実行し、Optimizer レポートを確認して、項目、ページレイアウト、レコードタイプ、入力規則など、Lusso に未使用の機能があるかどうかを確認します。

#### チャンピオンユーザのために Lightning Experience を有効化する
実際に使用することは、Lusso Scarpe にとって Lightning Experience が「そのまますぐに使用」できること、または Lusso の従業員に新しいインターフェイスの利用を依頼する前にどの機能とカスタマイズに対処する必要があるかを知るための最良のガイドです。評価の一環として、最も熱心で信頼できるユーザ(つまりチャンピオンユーザ！)に対して Lightning Experience をそのまま有効にして、迅速で実用的なフィードバックを得ましょう。

準備状況レポートの「Which Users Are Ready? (どのユーザが準備ができているか)」セクションによると、Lusso のどのユーザプロファイルもまだ Lightning Experience に対応する準備ができていないことがわかります。しかし、John Wiseman は Lusso の最大の Salesforce ファンであり、Lightning Experience に飛び込むことを楽しみにしています。さらに、顧客の問題のトラブルシューティングを頻繁に行うセールスマネージャとして、セールスチームとサポートチームの両方のニーズに精通しています。彼は、実態を把握するための短期間パイロットプログラムの理想的なチャンピオンです。John に Lightning Experience へのアクセス権を与えて、彼の考えを確認してください。

Lusso のコミュニケーションがセールスチームをリードしているので、Paloma Espinoza は会社の Chatter グループを管理し、Lusso のトップ取引先とコミュニケーションを取ります。パイロットに Paloma を含めて、彼女の観点とフィードバックも得られるようにしましょう。彼女は完全に Lightning Experience にしたいと思っているので、彼女の Salesforce Classic へのアクセス権限を取り除きましょう。

### Lusso Scarpe の Lightning Experience のロールアウト計画
Lusso Scarpe の全員が Lightning Experience を使用する必要があり、先のアクションに加わりたいと思っていました。しかし、初期の熱意を心からの定着化に変える最善の方法は、新しいインターフェイスを段階的に展開することです。Lightning Experience によってビジネスニーズが十分に満たされている小さなグループから始めます。それからフィードバックを集め、物事を微調整し、そして別の小さなグループにロールアウトします。すすいで繰り返します。すべての Lusso Scarpe ユーザが初日から生産的で成功するようにするための最善の方法です。

Lusso のビジネス上の優先事項、さらに Lightning Experience 準備状況レポートからのガイダンス、および 2 人のパイロットユーザである John と Paloma からのフィードバックに基づいて、Lightning Experience を 2 段階で展開することが最善の戦略であると判断しました。最初に、Lusso のセールスチームを移行します。それから、サポートチームを移行します。

## ビジネス要件および技術要件
Lusso Scarpe の Salesforce 組織における Lightning Experience の評価、チャンピオンユーザからのフィードバック、および必要な業務プロセスに関する Lusso のステークホルダの意見に基づいて、ロールアウト計画には以下の要件が含まれます。
### フェーズ 1 の要件
Lusso Scarpe が実現したいことは何ですか？もちろん、その驚くほど豪華な靴をもっと早く売ることです。Lightning Experience を準備して、Lusso のセールスチームに展開できるようにします。
#### 優先度の高い技術的問題を解決する
Lightning Experience の準備状況レポートでは、Salesforce は Lightning Experience でドキュメントオブジェクトのサポートを計画していないことがわかります。しかし、Lusso Scarpe のセールスチームはドキュメントを定期的に使用しているため、ロールアウトの最初のフェーズを開始する前にこのギャップに対処することが重要です。Salesforce Classic のドキュメントライブラリに格納されているリソースを Lightning Experience から使用可能にする方法を見つけ出す必要があります。

パイロットプログラムからのフィードバックを考慮すると、準備状況レポートに記載されている他の問題への対処は、ロールアウトの後の段階まで遅らせることができます。しかし、John と Paloma は、Lightning Experience の取引先オブジェクトホームページでの作業は、Salesforce Classic のように見えるため混乱を招くと指摘しました。Lusso は、取引先のレコードホームを Visualforce ページで上書きしています。このページは Lightning Experience では正しく機能しますが、Lightning Experience 風の見た目で表示されるように、スタイルを変更する必要があります。

#### ビジネス要件を満たし、最適なユーザ生産性を確保する
セールスチームが幸先の良いスタートを来られるように、Lightning Experience がロールアウトのフェーズ 1で以下のユースケースに対応していることを確認してください。
##### セールスの成功のために商談のワークスペースを最適化する
Lusso の新シーズンのコレクションが発表され、特に生活の中でキラキラとした靴が足りていない人々の間では、大ヒットでした。ミラノのファッションウィークに参加したことは確かに成果を上げました。特に卸売事業部門での問い合わせが大量に発生しているため、セールスマネージャは、営業担当者が重要なタスクに集中して取引を迅速に完了できるようにする必要があります。

営業担当が販売をうまく完了できるように、パイプラインの各段階で適切なガイダンスを提供してください。商談オブジェクトに次のガイダンスを含めてください。

| フェーズ | 項目 | 成功へのガイダンス |
|-|-|-|
| Qualification | Account Name, Opportunity Name, Description |- Ask the buyer about their favorite footwear.<br>- Share the most appropriate sections of our catalog.<br>- Share testimonials from fashionistas.<br>- Present our most popular ranges to the buyer.|
| Needs Analysis | Expected Revenue, Main Competitor(s), Next Step, Probability(%) |- Ask about the maximum price that the buyer is willing to spend.<br>- Ask: "Is there anything else you'd like to know or need to proceed with the purchase?"<br>- Set a date for follow-up.
| Negotiation/Review | Amount, Quantity, Stage |- If the buyer seems likely to walk away from the deal, discount 5%.<br>- Follow up on questions or needs from the buyer.
| Closed Lost | Close Date, Next Step | - Create post-mortem notes.<br>- Set a follow-up date for 1 year from today. |
| Closed Won | Close Date, Delivery/Installation Status | - Celebrate in Chatter!<br>- Check with the Accounts team for payment processing. |

##### よく必要とされる詳細情報で取引先のレコードページよりよくする
Lusso Scarpe のほとんどの Salesforce ユーザは、取引先レコードを定期的に使用しています。John および他のセールスチームの関係者からのフィードバックを使用して、営業担当にとって最も重要な取引先の詳細を次のように決めました。

- 取引先の名前
- その取引先で何名の従業員が働いているか
- その取引先へ連絡するために用いる電話番号
- 取引先とのビジネスをするのがどれほど簡単かの評価

しかし、Paloma は、トップ取引先とコミュニケーションするときにいくつかの異なるフィールドが役立つことをあなたに知らせました。取引先を扱う際の Paloma の優先事項は次のとおりです。

- 取引先の名前 The account’s name
- 取引先の種別 The type of account
- その取引先へ連絡するために用いる電話番号
- もしあれば、親取引先の名前

営業担当者が最も気にかけている詳細情報のハイライトが見えるように、一方で、Paloma は彼女が気にかけている詳細情報のハイライトが見えるように、取引先オブジェクトをカスタマイズしましょう。

##### 営業担当者が最も利用するオブジェクトにアクセスしやすくする
パイロットプログラムの間、John は、セールスという名前の Lightning アプリケーションを利用するときに、営業担当者が最も頻繁にアクセスする項目を見つけるために、余計にクリックをしなければいけないと報告しました。セールスチームに対する簡単なアンケートの結果、営業担当は定期的に以下のページやオブジェクト(ホーム、取引先、商談、キャンペーン、リード、取引先責任者、レポート、ダッシュボード)を操作していることがわかりました。セールス Lightning アプリケーションを設定して、営業担当者が余計な操作なしでこれらの重要なアイテムにすばやくアクセスできるようにしましょう。

営業担当者はまた、セールス Lightning アプリケーションで次のことができるページを求めています。

- 最近参照した取引先責任者、商談、およびリードを確認できる。
- 毎週の新しい取引先のリストを確認できる。
- すばやく新しい商談を作成でき、取引先責任者への通話を記録できる。

これらの要件を満たす **Key Sales Data** という Lightning ページを作成し、Sales アプリケーションに含めましょう。

Paloma は他のセールスチームとは異なるニーズを持っています。彼女は、取引先、Chatter、レポート、およびダッシュボードを定期的に使用しています。彼女がこれらの項目だけに集中できるようにする Paloma 用の新しい Lightning アプリケーションを作成します。それが彼女のプロファイルのデフォルトになるように新しいアプリケーションを設定してください。

##### Chatter グループでコラボレーションを促進する
Lusso Scarpe のリーダーシップチームは、常にオープンさと誠実さの文化を育んできました。Chatter よりも優れたツールは何ですか？会社の新しいユーザは、コラボレーションやお知らせを行うために記載、部門やチームのグループに参加します。

**All Lusso Scarpe Employees** と呼ばれる Chatterグループを作成し、以下の通り説明を記載します。**This group is for all Lusso Scarpe employees to collaborate and receive company announcements.** 全従業員がこのグループに参加できます。

グループの詳細ページ右側では、以下の情報が表示されるように設定します。フォローするのにおすすめのグループと個人、現在ディスカッション中の最も人気のあるトピック。
##### セールスマネージャへのレポートを設定する
Lusso が Lightning Experience に移行した主な理由は、優れた分析の機能です。適切なレポートとダッシュボードを作成することで、意思決定から推測を取り除き、セールスマネージャがセールスオペレーションの有効性を評価できるようにしましょう。

Lusso のセールスマネージャは、各取引先の商談のパイプラインを常に把握したいと考えています。取引先を表示するとき、彼らはフェーズごとの商談の数を示す、じょうごグラフを見たいと思っています。また、フェーズごとの商談の確度、成立した商談によって生み出された収益の大きさ、ビジネスの新規性や既存の収益の程度などを表示するダッシュボードも必要です。

セールスマネージャが必要な情報を入手できるように、Lightning Experience でレポートを設定します。最初に、全てのデータを表示し、フェーズごとに商談を表示するレポートを作成します。**Opportunities Pipeline** という名称を設定します。じょうごグラフをレポートに追加します。

次に、レポートグラフを取引先のレコードに追加します。レコード詳細ページに埋め込んだレポートグラフに **Opps by Stage** という名称を設定します。

次に、要求されたコンポーネントを含む **Sales Operations** というダッシュボードを作成します。

- フェーズごとに商談の確度を表示する **Opp Probability by Stage** という横棒グラフ。
- すべての商談から得られる収益の合計を表示する **Sum of Opportunity Ammount** というゲージコンポーネント。
- 新規または既存のビジネスによって生み出された収益の合計を表示する **New and Existing Business** というドーナツグラフ。

ユーザがフェーズごとにダッシュボードをフィルタリングできるようにします。フィルタには **Stage value** という名前を設定します。

Lusso のセールスマネージャは、人々がダッシュボードを見るとき、彼らが通常 Salesforce で見ることができるデータだけが見えるべきである、と知らせました。

最後に、John Wiseman は毎週 Opportunities Pipeline レポートを確認したいと考えています。毎週月曜日の午前 8時に更新されたレポートの結果をメールで受け取るように設定します。

### フェーズ 2 の要件
あなたはセールスチームのための Lightning Experience の展開に成功しました。今度はロールアウトのフェーズ 2 に取り組む時が来ました。

これが、Lusso のサポートチームに Lightning Experience を展開するフェーズです。加えて、セールスチームの成功指標をどれだけ達成できているかをモニタリングしており、営業担当者やマネージャから定期的なフィードバックを集めています。その結果、問題点を取り除き生産性を向上させるのに役立つ一連のアップデートを特定しました。
#### Lusso のサポートチームの Lightning Experience をカスタマイズする
Lusso Scarpe のサポート担当者は、顧客からの問い合わせや苦情に対して迅速かつ効率的なサービスを提供してきた実績を誇りに思っています。Lightning Experience では、Lightning ナレッジで強化された検索機能、コンソールの新しいナレッジサイドバー、およびその他多くの機能強化が提供されています。Lightning Knowledge のホームページには、Knowledge のリストビューもあり(やりましたね！)、営業担当者は記事の検索、表示、作成、管理のすべてを同じ場所から実施できます。

Lusso Scarpe のサポートチームを Lightning Experience に移行することが、ロールアウトのフェーズ 2における最優先事項です。サポート担当者がナレッジベース管理を効率化して顧客のサポートに費やせる時間を増やすために、Lightning Experience で Lightning Knowledge を有効にします。

サポートチームの以下の要件を満たすように Lightning Knowledge を設定しましょう。
- 記事を閲覧するときは、質問とそれに関連する回答が何であるかを明確にする必要があります。このデータを格納するために、**Question** と **Answer** という名前のロングテキストエリア項目を追加します。**Answer** 項目では、サポート担当者がテキストの書式設定と画像の入力ができるようにしてください。
- Lusso のサポートチームは、よく寄せられる質問、製品に関連した記事、コミュニティの記事など、さまざまな種類の記事を作成しています。これらの記事すべてに共通の情報がいくつかありますが、それぞれのタイプには固有の項目、アクション、関連リストがあります。これらの 3種類の記事を含めるように Lightning ナレッジを設定します。
- 記事の種類ごとに、レコードタイプ項目とカスタムの Question および Answer 項目を表示する必要があります。記事を作成または編集するときにナレッジユーザが記事の種類を選択できるようにします。

Lusso のナレッジ記事の準備ができたら、営業担当者に仕事をするための生産的な環境を提供しましょう。他のレコードの作業と並行してリストビューを表示し、さらに同じ画面に複数のレコードとそれらの関連レコードを表示する必要があります。**Lightning Knowledge** という Lightning アプリケーションを設定してこれを実現します。

営業担当者が最近訪問した主タブと、それらの主タブのコンテキスト内のサブタブを表示できるとしたら、それは素晴らしいことではないでしょうか。確かにそうなので、新しい Lightning Knowledge アプリケーションでこの機能にアクセスできることを確認してください。

Lightning Knowledge アプリケーションに Lightning Experience のホームページを含めます。しかし、デフォルトのホームページは Lusso のサポートチームにとって最適ではありません。あなたは Lusso のサポート担当者から彼らの理想的なホームページについての意見を集めました。そしてチームが必要としているものは以下の通りです。
- Chatter フィードを表示できる。
- 毎日の ToDo と予定を表示できる。
- 最近使ったデータにすばやくアクセスできる。
- 最も最近使用した項目の一覧を表示できる。

サポートチームは、アシスタントを必要としておらず、4半期パフォーマンスやトップ取引を確認する必要もありません。以上の要件を満たすように Lightningホームページをアップデートします。これに**Org Home**という名前をつけ、全員のデフォルトにします。
#### 準備状況レポートで特定されたより技術的な課題を解決する
Lusso Scarpe の準備状況に対する、新しい Salesforce リリースとあなたの開発努力の影響を確認するために、Lightning Experience の準備状況チェックをときどき実行しています。Lusso のセールスチームからの継続的なフィードバックに基づいて、フェーズ 2における現在の準備状況レポートで以下の問題に対処する必要があると判断しました。

1. Salesforce Classic のホームページに配置していた TrailheaDX サイドバーコンポーネントは、Lightning Experience では利用できません。このサイドバーコンポーネントを利用するために、営業担当者は頻繁に Salesforce Classic に戻しているというフィードバックを得ています。セールスの Lightning アプリケーションで TraiheaDX を利用できるようにすることで、この非効率を取り除いてください。
2. 準備状況レポートで特定されたカスタムリンクの代替を提供してください。幸いにも、Lusso の Salesforce 開発者は、あなたの生活を楽にするために Apex クラス、テストクラス、Lightning コンポーネントをすでに作成しています。

## 終了！
おめでとうございます。ロールアウトのフェーズ 2 が正常に完了して、Lusso Scarpe の全員が Lightning Experience で稼働し始めています。

## Challenge
### Challenge 1: Lusso の組織の準備状況チェック、Optimizer、短期間パイロットプログラムを評価する
Lightning Experience をロールアウトするための推奨事項とベストプラクティスに基づいて、Lusso Scarpe の本番組織<sup>[*2](#footnote2)</sup>の Lightning Experience 準備状況チェックを実行してから、メールで送信されたレポートを分析します。また、Salesforce Optimizer を実行して、Optimizer レポートでフィードバックを確認します。

それから、実態を把握するための短期間パイロットプログラムをキックオフします。あなたは John Wiseman と Paloma Espinoza をパイロットプログラムのためのチャンピオンユーザだと識別しました。そして 2人が新しいインターフェースで作業するためにトレーニングを実施しました。両名とも Lightning Experience にアクセスできるように設定してください。Lusso Scarpe の組織内の既存のプロファイルを変更しないでください。John はまだ Salesforce Classic へのアクセスを必要としていますが、Paloma を Lightning Experience での作業に限定します。John の場合は、**LightningExperiencePilotSales** という権限セットを使用してください。Paloma の場合は、**LightningExperiencePilotCommunications** という名前の権限セットを使用してください。

### Challenge 2: Lightning Experienceの価値提案 (クイズ)
1. Lightning Experience はなぜ Salesforce Classic よりも生産的なユーザインタフェースなのですか？
    - A. Lightning Experience uses custom JavaScript buttons and links to help users focus on relevant actions. (ユーザが関連するアクションに集中できるようにするため、カスタム Javascript ボタン・リンクを用いるため)
    - B. Lightning Experience uses the Force.com App Menu to switch between applications. (アプリケーション間を切り替えるために、Force.comアプリケーションメニューを用いるため)
    - C. Lightning Experience has buttons and links that launch browser windows. (他のブラウザウィンドウを起動するボタンやリンクがあるため)
    - D. Lightning Experience is a more streamlined user interface to help users focus on relevant actions. (ユーザが関連関連するアクションに集中できるよう、より洗練されたユーザインタフェースであるため)

2. エンドユーザが受けられる、Lightning Experience にしかない恩恵の 1つは何ですか？
    - A. Users can compile a Favorites list. (お気に入りリストを編集できる)
    - B. Users can use custom links. (カスタムリンクを利用できる)
    - C. Users can use email templates. (メールテンプレートを利用できる)
    - D. Users can expand and collapse sections on detail pages. (詳細ページのセクションを展開・折りたたみできる)

3. Lightning Experience の準備状況チェックが生成するレポートの価値は何ですか？
    - A. It provides permission set assignment rollout guidance. (権限セット割り当てのロールアウトのガイダンスを提供する)
    - B. It provides recommendations on how to optimize a Salesforce implementation. (Salesforce の実装をどう最適化するかの推奨事項を提供する)
    - C. It provides solutions to help transition features and customizations to Lightning Experience. (Lightning Experience の機能やカスタマイズを移行しやすくするソリューションを提供する)
    - D. It provides API version compatibility to transition to Lightning Experience. (Lightning Experienceの移行に互換性のある API バージョンを提供する)

4. Lightning Experience の準備状況レポートは、Lightning Experience でサポートされていない機能を特定します。その機能がいつリリースされる予定なのかを知るためには、どのリソースを使用すべきでしょうか？
    - A. trust.salesforce.com
    - B. Trailhead
    - C. Salesforce Release Notes and Lightning Experience Roadmap (リリースノートと Lightning Experience のロードマップ)
    - D. Trailblazer Community

5. 取引先から大量の商談が作成されるため、営業担当者はワンクリックで商談を作成したいと思っています。会社の方針によると、商談のフェーズ項目は常に入力する必要があります。この機能をどのように作成すべきでしょうか？
    - A. Create a JavaScript button that opens the /opp/oppedit.jsp page, then make the Stage field required on the action layout. (/opp/oppedit.jsp ページを開く JavaScript ボタンを作成し、アクションレイアウト上でフェーズ項目を必須にする)
    - B. Create an object-specific action on the Account object with the Standard Label Type of "New [Record]" then make the Stage field required on the action layout. (取引先オブジェクトに[レコードを作成]アクション種別でオブジェクト固有のアクションを作成し、アクションレイアウト上でフェーズ項目を必須にする)
    - C. Add the Stage field to Path on the Account object. (取引先オブジェクトのパスにフェーズ項目を追加する)
    - D. Create a new button with a custom link to create a new opportunity. (商談を新規作成するためのカスタムリンクで新しいボタンを作成する)

6. Lusso のセールスマネージャの 1人が取引先レコードを見ていましたが、関連する商談レコードについての情報を見つけられませんでした。Lightning Experience では、この情報はどこで見つける事ができますか？
    - A. Activity timeline (活動タイムライン)
    - B. Chatter Tab (Chatterタブ)
    - C. Related tab (関連タブ)
    - D. Notes & Attachments related list (メモと添付ファイルの関連リスト)

7. Lusso Scarpe は当初、Lightning Experience を一部の部門にのみロールアウトすることを検討していました。部分的なロールアウト戦略におけるトレーニングおよび改善のための取り組みに対する影響は何ですか？
    - A. It requires maintaining training resources for both user interfaces. (両方のユーザインタフェースのトレーニング資料をメンテナンスする必要がある)
    - B. It allows teams to develop training resources faster. (トレーニング資料をより早く作成できる)
    - C. It allows teams to present consistent training materials to users. (ユーザに一貫したトレーニング資料を提示できる)
    - D. It requires scheduling company-wide training. (全社的なトレーニングをスケジュールする必要がある)

8. ロールアウトの最初のフェーズの間、Lusso Scarpe のセールスチーム内のいくつかのグループだけが Lightning Experience を利用することになります。特定のユーザを移行するためには何を利用スべきでしょうか？
    - A. Sharing rules (共有ルール)
    - B. Standard Profiles (標準プロファイル)
    - C. Permission sets (権限セット)
    - D. Role hierarchy (ロール階層)
    - E. Licenses (ライセンス)

9. Lusso Scarpe は Lightning Experience の実装をテストし、パイロットプログラムを通してそれを改善する方法を見つけたいと考えています。このパイロットプログラムに参加するユーザを選択する必要があります。適切なユーザは誰ですか？
    - A. Leadership teams who are the major stakeholders in the business. (ビジネス上の主要なステークホルダである経営陣)
    - B. End users who use the product on a daily basis. (製品を毎日利用しているエンドユーザ)
    - C. Engaged users who can provide feedback. (フィードバックを提供してくれる積極的なユーザ)
    - D. Team leads and managers who know their team operations well. (チームのオペレーションをよく知っているチームリードとマネージャ)

### Challenge 3: 準備状況レポートで特定された重要な問題を修正する
Lightning Experience のロールアウトの最初のフェーズに備えて、Lusso Scarpeの組織を準備します。要件に記載されているように、ドキュメントオブジェクトが Lightning Experienceでは使用できないという事実に対処するために適切な手順を実行してください。そして、取引先オブジェクトのホームページを上書きする Visualforceページの見た目を修正してください。

### Challenge 4: セールスプロセスのガイダンスを追加し、取引先の主要な詳細をハイライトする
要件に記載されているように、Lusso Scarpe の商談に関するセールスプロセスのガイダンスを追加してください。このガイダンスを商談オブジェクトのパスに含めます。パスには **Opportunity Path** という名前を付けて、有効化してください。

また、要件に記載されている通り、営業担当者が最も気にかけている詳細情報のハイライトが見えるように、一方で、Paloma は彼女が気にかけている詳細情報のハイライトが見えるように、取引先オブジェクトをカスタマイズしてください。実装方法の詳細については以下のヘルプ記事を参照してください。
[https://help.salesforce.com/articleView?id=compact_layout_overview.htm&type=5](https://help.salesforce.com/articleView?id=compact_layout_overview.htm&type=5)

### Challenge 5: Sales Cloud の Lightning Experience (クイズ)
1. Lusso Scarpe のパートナマネージャは、各パートナサイトで連携する取引先責任者を特定するために、取引先責任者の取引先でのロールを使用しています。パートナマネージャは、Lightning Experience でこのデータを収集するために何をする必要がありますか？
    - A. Contact Roles (取引先責任者の役割)
    - B. Contacts to Multiple Accounts (取引先責任者-to-複数取引先)
    - C. Partners related list (パートナの関連リスト)
    - D. Groups (グループ)

2. Lusso Scarpe は、正しい部門の採用マネージャを入力するため、Hiring Manager 項目にルックアップ検索条件を設定しています。ルックアップ検索条件の代わりに、Lightning Experience では何を使用するべきですか？
    - A. Lookup search (ルックアップ検索)
    - B. Grobal search (グローバル検索)
    - C. Dependent lookup (連動ルックアップ)
    - D. Enhanced lookup (高度なルックアップ)
    - E. User-defined lookup filters (ユーザ定義のルックアップ検索条件)

3. ステークホルダと共に、ギャップ分析を実施して Lightning Experience への移行の影響を評価しています。リスクマトリックスを用いて、見つかったギャップを分類します。どのシナリオが正しいですか？
    - A. The Sales teams use several JavaScript buttons that open external web pages. Transitioning the Sales teams to Lightning Experience is LOW RISK. (セールスチームは、外部 Web ページを開くための JavaScript ボタンを使用しています。セールスチームを Lightning Experience に移行するのは低リスクです。)
    - B. The Training and Enablement teams use Work.com. Transitioning these teams to Lightning Experience is HIGH RISK. (トレーニングチームとイネーブルメントチームは Work.com を使用しています。これらのチームを Lightning Experience に移行するのは高リスクです。)
    - C. Sales staff use the Similar Opportunities feature to find Closed/Won opportunities that Match the attributes of an opportunity they’re currently working on, They're excited to Use the Lightning Experience equivalent of this feature. Transitioning this team to Lightning Experience is LOW RISK. (セールススタッフは、類似商談の機能を使用して、現在取り組んでいる商談と属性が一致する、成立した商談を見つけています。チームは Lightning Experience で同等の機能を使用できることを楽しみにしています。このチームを Lightning Experienceへ移行するのは低リスクです。)
    - D. The Support teams wants to use the case feed view. Transitioning this team to Lightning Experience is HIGH RISK. (サポートチームはケースフィードビューを使用したいと考えています。このチームを Lightning Experience に移行するのは高リスクです。)

4. Lusso Scarpe は、Lightning Experience に切り替えることなく、Lightning Experience が実際のデータでどのように見えるかを確認したいと考えています。この機能を提供するのはどれですか？
    - A. Lightning Experience
    - B. Lightning Login
    - C. My Domain (私のドメイン)
    - D. Preview (プレビュー)

5. Jorge Marroquin は Lusso Scarpe のセールスチームのメンバーです。あなたの組織では、彼は定期的に取引先・取引先責任者、リード、および商談を扱います。彼のマネージャである Susan Dempsey は、週に 1回カスタマイザブル売上予測を使用して、彼女のチームの予測パフォーマンスに関する売上予測を作成します。誰が Lightning Experience に移行する必要がありますか。その理由は何ですか？
    - A. Susan Dempsey, because in Lightning Experience, deleting a record type that has a corresponding Sales path also deletes the path (Susan、Lightning Experience では、対応するセールスパスのあるレコードタイプを削除するとパスも削除されるため)
    - B. Jorge Marroquin, because the Salesforce Classic page layouts for custom objects and some standard objects are compatible with Lightning Experience (Jorge、カスタムオブジェクトおよび一部の標準オブジェクトの Salesforce Classic ページレイアウトは Lightning Experience と互換性があるため)
    - C. Susan Dempsey, because the dashboards available on the Salesforce Classic home page layout have enhanced functionality in Lightning Experience (Susan、Classic のホームページレイアウトで利用できるダッシュボードは Lightning Experience で機能が強化されているため)
    - D. Both Susan Dempsey and Jorge Marroquin, because Susan can switch back to Salesforce Classic to forecast (両方、Susan は売上予測のために Salesforce Classic に戻ることができるため)

6. Lusso Scarpeの営業担当者は、商談の金額を商談チームの複数のメンバーに帰属させたいと思っています。どの Lightning Experience機能を使用すべきでしょうか？
    - A. Opportunity splits (商談分割)
    - B. Similar Opportunities (類似商談)
    - C. Groups (グループ)
    - D. Custom Lightning component (カスタム Lightningコンポーネント)

7. Lusso Scarpe の営業担当者は、定期的に活動予定および活動履歴の関連リストを使用しています。Lightning Experience で営業担当者は活動の情報をどのように参照しますか？
    - A. View the Open Activities and Activity History related lists. (活動予定と活動履歴の関連リストを参照する)
    - B. View the activity timeline on the record detail page. (レコード詳細ページ上の活動タイムラインを参照する)
    - C. View the Next Steps field. (次のステップ項目を参照する)
    - D. View the activity timeline in the related list. (関連リストにある活動タイムラインを参照する)

8. Lusso Scarp は、営業担当者が新しい見込み客や重要な取引のフォローアップを見逃さないようにしたいと考えています。営業担当者が参照する必要がある Lighting Experience の機能はどれですか？
    - A. Top Deals (トップ案件)
    - B. Path (パス)
    - C. Assistant (アシスタント)
    - D. Highlights Panel (強調表示パネル)

9. Lusso Scarpe の営業担当者は、関連する取引先を表示するときに特定の項目情報を確認したいと考えています。どの Lightning Experience 機能を使用すべきでしょうか？
    - A. Account Hierarchy (取引先階層)
    - B. Partners (パートナ)
    - C. Account Site ([取引先 部門] 項目)
    - D. Contact Roles (取引先責任者の役割)

### Challenge 6: セールスアプリケーションのナビゲーションを改善し、Chatter グループを作成する
要件に記載されているように、**Sales** (セールス) という Lightning アプリケーションを変更して、営業チームにとって最も重要なアイテムだけを含めます。次に、要件に指定されている情報とアクションを含む **Key Sales Data** というページを作成します。ユーザが Sales アプリケーションから Key Sales Data ページにアクセスできるように設定してください。

Paloma が定期的に使用するアイテムを含む **Communications** という Lightning アプリケーションを作成します。Paloma が新しいアプリケーションにアクセスできるように設定してください。

最後に、要件に示されている Chatter グループを作成し、指定された情報が表示されるようにグループのレコードページをカスタマイズしてください。

### Challenge 7: Lightning Experience でセールスマネージャのためのレポートを設定する
要件に記載されているように、**Oppotunities Pipeline** という名前のレポートを作成し、取引先レコードに**Opps by Stage** のグラフを追加します。レポートは 1つだけ作成し、数式項目は利用しないでください。

以下のコンポーネントを含む **Sales Operations** という名前のダッシュボードを作成してください。**Opp Probability by Stage**、**Sum of Opportunity Amount**、**New and Existing Business** の 3 つです。ユーザがダッシュボードをフェーズでフィルタできるよう設定してください。フィルタに **Stage value** という名前をつけます。そして、人々がダッシュボードを参照するとき、正しいデータが見えるようにしてください。Challenge をチェックする直前にダッシュボードをリフレッシュしてください。

最後に、**John Wiseman** がリフレッシュされた Opportunities Pipeline レポートを毎週受け取れるように設定してください。彼は毎週月曜の午前 8時にレポートをメールで受け取りたいと思っています。

### Challenge 8: Lusso のサポートチームのためにLightning Experience を設定する
Lusso Scarpe サポートチームは、Lightning Experience と Lightning Knowledge に切り替える準備ができています。

Lightning Knowledge を有効にしてください。次に、Lusso Scarpe のナレッジ記事に対する要件に対応するために Lightning Knowledge を設定してください。

**Question** と **Answer** というカスタム項目を作成してください。**Answer** 項目では、サポート担当者は入力したテキストをフォーマットし、画像を含られるようにする必要があります。

Lussoのサポートチームが使用する 3 つの記事の種類を、**FAQ**、**Product**、**Community** という名前で設定します。各種類ごとに、レコードタイプ、Question、Answer項目を含める必要があります。各種類に項目を追加するときには以下の名前を使用します。FAQの記事は **faqpagelayout**、Product の記事は **productpagelayout**、Communityの記事は **communitypagelayout** です。

Lightning Knowledge という名前の Lightning アプリケーションを作成し、要件に記載されているようにカスタマイズします。

最後に、サポートチームの要件を満たすように Lightning Experience のホームページを設定します。

### Challenge 9: Service Cloud の Lightning Experience (クイズ)
1. Salesforce Classic では、カスタマサポートチームは共通的な問題を解決するためにソリューションオブジェクトを利用してステップをたどっています。Lightning Experience ではサポートチームはどの機能を利用できますか？
    - A. Solutions (ソリューション)
    - B. Lightning Knowledge (Lightningナレッジ)
    - C. Files (ファイル)
    - D. Notes & Attachments (メモ＆添付ファイル)

2. Lusso Scarpe のサービスサポートスタッフは、ナレッジを管理するために記事タイプを用いています。記事を社内のサポートスタッフに表示する方法を一意に制御するためのフォーマットと構造を提供するために、どの機能を使用する必要がありますか？
    - A. Object permissions (オブジェクト顕現)
    - B. Record types for Knowledge (ナレッジのレコードタイプ)
    - C. Article types for Knowledge (ナレッジの記事タイプ)
    - D. Profiles (プロファイル)

3. セールスチームはよく、商談レコードに PowerPoint のプレゼンテーションを添付しています。商談上のこれらのプレゼンテーションは Lightning Experience ではどこに保存されますか？
    - A. Salesforce Connect 
    - B. Notes (メモ)
    - C. Attachments (添付ファイル)
    - D. Documents (ドキュメント)
    - E. Files (ファイル)

### Challenge 10: Lightning Experience の準備状況レポートで特定された問題をより修正する
ロールアウトのフェーズ 2で必要であると判断した準備状況レポートの問題を修正しましょう。

Sales (セールス) という Lightningアプリケーションを Salesforce Classic ホームページの TrailheaDX サイドバーコンポーネントの機能を含むように設定してください。Lightning Experience でこの機能を再現するために、**TrailheaDX** という Lightning コンポーネントを作成してください。Trailhead Playground では既に私のドメインが有効になっています。私のドメインの設定は編集しないでください。

カスタムの **UpsellCrosssellOpportunity** リンクを、Lusso の Salesforce 開発者が作成したカスタム Lightning コンポーネントの CreateOppty に置き換えてください。

**View Campaign Influence Report** (キャンペーンインフルエンスのレポートを表示) リンクの代わりに使用する新しいリンクを作成してください。以下の要件を適用してください。
* レポートに **Campaign Influence Lightning** という名前を付けます。
* リンクに **View Lightning Campaign Influence Report** という名前を付けます。
* リンクには相対 URL と動的フィルタ値を使用します。
* キャンペーンのページレイアウトにリンクを含めます。

## 訳注
* <a name="footnote1">[1]</a>  : 原文は "Your mission, should you choose to accept it" で、これは Mission Impossible の有名なセリフです。
* <a name="footnote2">[2]</a>  : 文中では本番組織とありますが、実際にはこのスーパバッジに利用している Trailhead Playground 組織のことです。

## 補足とヒント
### Challenge 3
Visualforce ページへの [Lightning Design System](https://www.lightningdesignsystem.com) の適用については、[開発者ガイド](https://developer.salesforce.com/docs/atlas.ja-jp.pages.meta/pages/vf_dev_best_practices_slds_apply.htm)や[Trailhead の Visualforce と Lightning Experience の単元](https://trailhead.salesforce.com/ja/content/learn/modules/lex_dev_visualforce/lex_dev_visualforce_design)を参照してください。Account TabsのVisualforceページはテーブルを表示していますので、[apex:pageBlockTable の開発者ガイド](https://developer.salesforce.com/docs/atlas.ja-jp.pages.meta/pages/pages_compref_pageBlockTable.htm)や、[Lightning Design System のテーブルコンポーネント](https://www.lightningdesignsystem.com/components/data-tables/)も参考にしてください。

### Challenge 6
グループの Lightning ページを設定する際、その Lightning ページの API 参照名が **Group_Record_Page** となっていることを確認してください。

### Challenge 10
* Campaign Influence Report については、[Lightning Experience での URL パラメータを介したレポートの絞り込み](https://help.salesforce.com/articleView?id=reports_filter_url.htm&type=5)のヘルプ記事が参考になります。
* URL は[新しい形式](https://releasenotes.docs.salesforce.com/ja-jp/summer18/release-notes/rn_general_new_url_format_lex.htm)を利用しましょう。
