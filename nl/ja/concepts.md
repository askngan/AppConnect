---

copyright:
  years: 2017
lastupdated: "2018-07-20"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip} 
{:download: .download}


# IBM App Connect の概念
{: #concepts}

{{site.data.keyword.appconservicefull}} は、クラウド・ベースのアプリケーションやオンプレミス・アプリケーションを統合して退屈な繰り返し作業を自動化するために使用できるビジネス・フレンドリーなツールです。

ここでは、{{site.data.keyword.appconserviceshort}} の以下の機能と用語について説明します。

-   [フロー](#flows)
-   [アプリケーション](#apps)
-   [アクション](#actions)
-   [データ・マッピング](#transforms)
-   [BAR ファイルと統合サーバー](#barfiles)

## フロー
{: #flows}

{{site.data.keyword.appconserviceshort}} で作成できるフローには、イベント・ドリブン・フローと API 用のフローの 2 つのタイプがあります。

イベント・ドリブン・フローでは、最初のアプリケーション (ソース・アプリケーション) で発生する可能性のある 1 つのイベントと、1 つ以上のターゲット・アプリケーションで実行できるアクションを特定します。フローではそのイベントがそれらのアクションにリンクされます。これにより、ソース・アプリケーションでイベントが発生すると必ず、ターゲット・アプリケーションでアクションが自動的にトリガーされるようになります。正常に完了した各アクションは月次割り当て量にカウントされます。フローを作成するときは、アプリケーションを追加し、アクションを選択します。次に、アプリケーション間で転送するデータをマップします。

例えば、誰かが新規参加者として Eventbrite (イベント) に登録されるたびに、{{site.data.keyword.appconserviceshort}} が自動的にその参加者の詳細を Salesforce から取得して Asana (アクション) に新しいタスクを作成するようにフローを作成することもできます。

![ソース・アプリケーションと 2 つのターゲット・アプリケーションで構成されたマルチノード・フロー](images/multi_node_flow2.jpg)

詳しくは、[Creating an event-driven flow ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/creating-event-driven-flow/) を参照してください。

API 用のフローには、1 つの要求、1 つ以上のターゲット・アプリケーション・アクション、1 つの応答が含まれます。要求では、アプリケーション内のデータ・オブジェクトの作成、置換、または取得を要求するために定義したモデルが使用されます。要求が実行依頼されると、各ターゲット・アプリケーションはそのアクションを実行し、その後フローは、アクションが正常に完了したことを確認する応答を返すか、要求されたデータを返します。

![Salesforce に製品を作成する API 用のフロー](images/APIFlow2.jpg)

詳しくは、[Creating flows for an API ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/creating-flows-api/) を参照してください。

フローへのアプリケーションの追加と同様に、データの処理方法を構成するためのノードを**「ロジック (Logic)」**タブから追加することもできます。例えば、If ノードを使用して何らかの条件付き処理を追加することで、受け取ったデータに応じて異なるアクションを実行します ([Adding conditional logic to a flow ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/adding-conditional-logic-flow/) を参照)。また、取得アクションによって返されるレコードごとにアクションを実行するときは For each ノードを使用します ([Retrieving items from your applications ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/using-ibm-app-connect-retrieve-items-applications/) を参照)。

IBM Integration Bus または App Connect Enterprise 開発者であれば、Integration Toolkit でメッセージ・フローを作成して BAR ファイルにパッケージすることによって、複合統合ソリューションを作成することもできます。

フローと統合サーバーは App Connect ダッシュボードでタイルで表されます。タイルには、フロー、API、または統合サーバーに関する要約情報が表示されます (例えば、フローが実行中であるか停止しているか、正常に実行されたかエラーになったかなど)。フローの実行が最後にいつ正常に完了したか、あるいはどのようなエラーが発生したかを調べるには、チェック・マーク・アイコンに続いて感嘆符アイコンをクリックします。3 つのドット ![縦 3 ドットのアイコンをクリックすると、フローを開始、停止、編集、削除するためのメニューが開きます](images/Menu.jpg) をクリックすると、リソースを開始、停止、編集、削除するためのメニューが開きます。フローは編集するためには停止しておく必要があります。

![ダッシュボード上のタイル (イベント・ドリブン・フロー、API 用のフロー、統合サーバー) を示すスクリーン・ショット](images/Dashboard.jpg)

## アプリケーション
{: #apps}

イベント・ドリブン・フローまたは API 用のフローを作成する場合、_アプリケーション_ は、接続するクラウド・ベースのソフトウェア・アプリケーションです。{{site.data.keyword.appconserviceshort}} と接続できるアプリケーションのリストが**「アプリケーション」**ページに表示されます。アプリケーションに関する詳細を確認したり、サポートされているイベントとアクションを調べたり、お客様自身のアカウントに接続したりするには、アプリケーションをクリックします。「アプリケーション」ページで各アプリケーションに複数のアカウントを接続して、アカウントを切り替えることができます。アカウントに接続した後、このページでアカウントを更新したり削除したりすることもできます。

![「アプリケーション」ページのアプリケーションのうちの 1 つのスクリーン・ショット](images/Magento2.jpg)

「アプリケーション」ページでアプリケーションに接続しなければならないわけではありません。フローにアプリケーションを追加するときにフロー・エディターで接続することもできます。多くのアプリケーションはユーザー名とパスワードだけを必要としますが、さらに情報を必要とするものもあります。この情報を見つける方法は、[How-to guides for apps ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://developer.ibm.com/integration/docs/app-connect/how-to-guides-for-apps/) に記載されています。

クラウドで {{site.data.keyword.appconservicefull}} を使用して Integration Bus または App Connect Enterprise ソリューションを実行する場合、_アプリケーション_ は、メッセージ・フローやライブラリーなど、ソリューションが必要とするリソースを保持するコンテナーです。 

## アクション
{: #actions}

いくつかのタイプのアクションをフローに追加できます。一般的なアクションは「作成」、「取得」、および「更新/作成」ですが、特有のアクションを備えているアプリケーションもあります。例えば、Equals 3 Lucy アプリケーションには「Ask Lucy」というアクションがあり、Watson Personality Insights アプリケーションには「Analyze personality」というアクションがあります。アプリケーションでサポートされるアクションのリストを {{site.data.keyword.appconserviceshort}} で表示するには、「アプリケーション」ページの最上部にある検索フィールドにアクション・タイプを入力します。

![アプリケーションでサポートされる取得アクションを示すスクリーン・ショット](images/RetrieveApps2.jpg)

**作成 (Create)**

名前が示すように、作成アクションはアプリケーション内にオブジェクトまたはレコードを作成します。例えば、誰かがイベントに登録するか完了フォームを送信したら、その人のレコードを CRM アプリケーションまたはマーケティング・アプリケーション内に作成することが必要な場合があります。また、誰かがヘルプ・デスク・アプリケーションでチケットを開いたら、誰かがそれにすぐに対応できるようにするために、E メールやインスタント・メッセージを作成することが必要な場合があります。作成するオブジェクトが既に存在している可能性がある場合は、代わりに*更新または作成* アクションを使用できます。

アプリケーションによっては、オブジェクトを作成する場所をフローが認識できるように、フローに作成アクションを追加するときに何らかの補足情報を指定しなければならない場合もあります。例えば、Asana や Trello のようなプロジェクト管理アプリケーションを使用する場合は、タスクつまりカードを作成するときに、プロジェクト、つまりカードを追加するボードを指定することが必要になります。

**更新/作成 (Update or Create)**

更新/作成アクションは、ターゲット・アプリケーション内の既存レコードを変更しますが、まだ存在しない場合はレコードを作成します。これは upsert (更新/挿入、update or insert) アクションとも呼ばれます。

例えば、住所の変更を含む Wufoo フォームを誰かが送信したとします。CRM システムに既に連絡先があれば住所を更新する必要がありますが、連絡先がない場合は追加する必要があります。取得アクションと同様、アプリケーションのうちの 1 つにあるデータを更新するアクションを選択するときに、1 つ以上の条件を追加することで、必ず正しい情報を更新するようにすることができます。

基準と一致するレコードがターゲット・システムに複数存在する場合は、フローのエラーがダッシュボードに表示され、フローはレコードの更新も作成も行いません。例えば、名と姓が同じ連絡先が複数存在するかもしれません。このような場合は、E メール・アドレスなどの固有情報を使用して連絡先を突き合わせるようにすることができます。

更新/作成アクションに対する応答として出される可能性がある状況コードは、以下のとおりです。

-   200: レコードが更新されました
-   201: レコードが作成されました

これらの応答コードはその後フローで使用できます。レコードが更新されたか作成されたかによって異なるアクションを取る必要があるかもしれません。応答コードに基づいたアクションの定義の例については、チュートリアルの [Creating an event-driven flow that updates or creates a contact in Salesforce and updates Asana whenever you receive a form in Wufoo](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/creating-event-driven-flow-updates-creates-contact-salesforce-updates-asana-whenever-receive-form-wufoo/) を参照してください。

**取得 (Retrieve)**

取得アクションは、別のアプリケーションで使用できるようにアプリケーションから情報を取得します。

オブジェクトを取得するためにフローにアクションを追加するときに、必ず正しい項目を取得するように 1 つ以上の条件を定義できます。あるいは、特定のタイプの項目をすべて取得するだけなら、条件を削除します。取得する項目の数と、{{site.data.keyword.appconserviceshort}} がその数より多いまたは少ない項目を検出した場合の対応を定義することもできます。

取得された項目は次の 2 つの方法で扱えます。

-   取得アクションの後に「For each」ノードを追加することにより、取得された項目のそれぞれに対してアクションを実行できます。
-   取得アクションの後に別のアクションを追加することにより、取得された項目のリストを処理できます。これは、項目がいくつ返されても、単一のアクションです (例えば、取得された項目をすべてリストした E メールの作成など)。

取得アクションに対する応答として取得する状況コードに基づいて、どのようなアクションを取るかを決定することもできます。状況コードによって異なるアクションを実行するには、「If」ノードを使用します。取得アクションに対する応答として出される可能性がある状況コードは、以下のとおりです。

-   204: レコードが見つかりませんでした
-   200: アプリケーション内のすべてのレコードが条件に一致します
-   206: 指定された最大数のレコードが取得されましたが、アプリケーションにはさらにレコードが存在します

詳しくは、[Retrieving items from your applications](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/using-ibm-app-connect-retrieve-items-applications/) を参照してください。

## データ・マッピング
{: #transforms}

フローを作成し、アプリケーションを追加し、適切なアクションを選択したら、アプリケーション間で転送する情報を指定する必要があります。フロー・エディターでフローにアクションを追加すると、そのアプリケーションで使用できるフィールドのリストが表示されます。これらのフィールドに、ソース・アプリケーションからのデータ、またはフロー内の前のアクションからのデータを取り込めます。

いくつかのフィールドは必須であり、それらにはアスタリスクのマークが付けられます。例えば、Salesforce にリードを作成する場合は、姓を指定する必要があります。

![「Last name」フィールドが必須であることを示すスクリーン・ショット](images/LastName.jpg)

これらのフィールドのいずれかをクリックすると、**「参照の挿入 (Insert reference)」** ![「参照の挿入 (Insert reference)」アイコン](images/InsertRef.jpg) と**「関数の適用 (Apply a Function)」** ![「関数の適用 (Apply a Function)」アイコン](images/Functions.jpg) の 2 つのアイコンが表示されます。**「参照の挿入 (Insert reference)」**をクリックすると、フロー内のこれまでのアプリケーションから、そのフィールドに入れることができる使用可能データが表示されます。次の例は、Wufoo ソース・アプリケーションから、またはフロー内の前の Salesforce アクションからフィールドを選択できることを示しています。Salesforce の更新/作成アクションからの状況コードを使用することもできます。

![データ・マッピングに使用できる入力を示すスクリーン・ショット](images/Inputs.jpg)

次の例では、Wufoo で受け取られる新規完了フォームでフローがトリガーされます。そのフォームを送信した人の連絡先を Salesforce に作成する必要があります。そのため、Salesforce の「Create contact」アクションをフローに追加するときに、Wufoo フォームから連絡先の詳細をコピーします。この例では、Salesforce の連絡先の姓については Wufoo フォームの送信者の姓を選択しています。その色から、マップ・フィールドは Wufoo からのものであることがわかります。

![Wufoo の「Last name」フィールドが Salesforce の「Last name」フィールドにマップされたことを示すスクリーン・ショット](images/Mapping.jpg)

次の例では、フロー内の Salesforce の「Update or create contact」アクションの後に Slack の「Create message」アクションを追加しています。この Salesforce アクションに対してどのような応答コードを受け取ったかを示すメッセージを Slack に伝えたいだけです。

![応答コードをマップする Slack の「Create message」アクションのスクリーン・ショット](images/SlackSC.jpg)

Slack の「Create message」アクションの**「Text」**フィールドにはメッセージを入力し、Salesforce の「Update or create contact」アクションに対する状況コードにマップしていることがわかります。

以下は、異なる方法で応答コードをマップする別の例です。今度は、Salesforce の既存の連絡先が更新されたか新しい連絡先が作成されたかによって異なるアクションを実行する必要があるため、Salesforce の「Update or create contact」アクションの後に「If」ノードを追加しています。この場合、応答コード「200」は、連絡先が更新されたことを意味します。したがって、この「If」ノード分岐には、更新されたレコード固有のアクションが含まれます。

![If ノードで使用される応答コードを示すスクリーン・ショット](images/IfSC.jpg)

**「関数の適用 (Apply a function)」**アイコン ![「関数の適用 (Apply a function)」アイコン](Functions.jpg) をクリックすると、フローの中で渡すデータをカスタマイズするために使用できる変換関数のリストが表示されます。これらの関数には、特定のフィールドを大文字または小文字に変換するといった単純なものもあれば、データ内の特定のパターンを検出して置換するなど、やや複雑なものもあります。正規表現を記述するという強力なものもあります。必要な関数をリストから選択することも、ユーザー自身が入力することもできます。関数の構文は、照会と変換のための軽量言語である JSONata です。詳しくは、[http://jsonata.org](http://jsonata.org) を参照してください。


## BAR ファイルと統合サーバー
{: #barfiles}

BAR ファイルとは、IBM Integration Bus または App Connect Enterprise におけるデプロイ可能リソースを追加する圧縮ファイルのことです。Integration Bus または App Connect Enterprise で統合ソリューションを開発したら、メッセージ・フローとそれらのメッセージ・フローが使用するすべてのリソースを BAR ファイルにパッケージした後、その BAR ファイルを統合サーバーにデプロイします。そのサーバーの場所は、オンプレミスまたは {{site.data.keyword.appconserviceshort}} 内になります。Integration Bus または App Connect Enterprise ソリューションを App Connect で実行できます。IT インフラストラクチャーを確保して保守する必要はありません。BAR ファイルを App Connect にアップロードすると、その BAR ファイルの内容を実行するための統合サーバーが作成されます。クラウド・ベースのリソースとオンプレミス・リソースの間の基本認証とセキュア接続を構成できます ([Running your Integration Bus solutions in App Connect ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan) を参照)。  
