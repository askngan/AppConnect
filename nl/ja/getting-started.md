---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-06"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip} 
{:download: .download}


# IBM App Connect の概要
{: #gettingStarted}

{{site.data.keyword.appconservicefull}} は、単純なトリガー・アクション対話から複雑な統合に至るまで、アプリケーションを接続するのに役立ちます。{{site.data.keyword.appconserviceshort}} を使用して、イベント・ドリブン・フローや API 用のフローを作成できます。あるいは、IBM Integration Bus で作成した統合ソリューションを、IT インフラストラクチャーを獲得したり保守したりせずにアップロードして実行することもできます。{{site.data.keyword.appconserviceshort}} ダッシュボード上の 1 つの場所で、統合サーバー、イベント・ドリブン・フロー、API 用のフローといったすべての統合を参照したり管理したりできます。 

{{site.data.keyword.appconserviceshort}} サービスのインスタンスを作成し終えると、{{site.data.keyword.Bluemix}} ダッシュボードから {{site.data.keyword.appconserviceshort}} にアクセスできます。

以下の手順には、App Connect を開始するのに十分な情報が提供されています。詳細な指示、特定のアプリケーションに関する How-to ガイド、チュートリアル、ビデオについては、[IBM App Connect ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://developer.ibm.com/integration/docs/app-connect/) の資料一式を参照してください。

## イベント・ドリブン・フローの作成

名前が示すように、イベント・ドリブン・フローはソース・アプリケーション内の 1 つのイベント (フローをトリガーする) とターゲット・アプリケーション内の 1 つ以上のアクションから成ります。したがって、ソース・アプリケーション内でイベントが発生すると、ターゲット・アプリケーション内でアクションがトリガーされます。クラウド・ベースのアプリケーションを接続するイベント・ドリブン・フローを作成するには、以下の手順を実行します。
1.  {{site.data.keyword.appconserviceshort}} ダッシュボードで、**「新規 (New)」** > **「イベント・ドリブン・フロー (Event-driven flow)」**をクリックします。
    進んでいく過程で、{{site.data.keyword.appconserviceshort}} は変更内容を自動的に保存します。途中の段階でフローから離れると、そのフローはドラフト・フローとして保存されるので、別の機会に完了できます。
1.  フローの名前を入力します。
1.  アプリケーションを展開してイベントを選択し、フローを開始するトリガー・イベントを選択します。
1.  まだアプリケーションに接続していない場合は、**「アプリケーションに接続 (Connect to _application_)」**をクリックし、アプリケーションに対するログインの詳細情報を入力します。
    一部のアプリケーションでは、追加の接続の詳細情報を入力する必要が生じる場合があります。特定のアプリケーションのための資格情報を見つけるのに支援が必要な場合は、[How-to guides for apps ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://developer.ibm.com/integration/docs/app-connect/how-to-guides-for-apps/) を参照してください。
1.  アプリケーションを展開してアクションを選択し、2 つ目のアプリケーション内でトリガーされるアクションを選択します。
    必要に応じて、**「アプリケーションに接続 (Connect to application)」**をクリックし、ターゲット・アプリケーションに対するログインの詳細情報を入力します。
1. アプリケーション間で転送しようとしているデータを入力します。
    フィールドをクリックしてからマッピング・アイコン ![マッピング・アイコン](/images/MappingIcon.jpg) をクリックし、手動でソース・フィールド名を追加できます。テキストで入力するか、変換関数を使用してソース値をカスタマイズすることもできます。詳しくは、[How to use transformations ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://developer.ibm.com/integration/docs/app-connect/faq/#faq_transforms) を参照してください。
1. オプション: 以下のようにして、フローの働きを詳細化できます。
    * フロー内のプラス・アイコン ![アプリケーション追加アイコン](/images/AddApp.jpg) をクリックして、ターゲット・アプリケーションやアクションをさらに追加します。
    * 取得アクションをフローに追加して、特定の基準に一致する項目を取得するか、指定された数のレコードを取得するか、エラー処理を定義するか、または取得された項目を処理する方法を定義します ([Using App Connect to retrieve items from your applications ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/using-ibm-app-connect-retrieve-items-applications/) を参照)。
    * フロー内のアプリケーションから受け取るデータに応じて異なるアクションを実行するには、条件ロジックを追加します ([Adding conditional logic to a flow ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/adding-conditional-logic-flow/)を参照)。

1. フローを構成し終えたら、ヘッダー・バー上のオプション・メニューを開き、**「フローの開始 (Start flow)」**をクリックします。

{{site.data.keyword.appconserviceshort}} ダッシュボードに戻ると、フローが実行中であることが示されます。1 つ目のアプリケーション内でイベントが発生すると、2 つ目のアプリケーション内で {{site.data.keyword.appconserviceshort}} によりアクションが自動的にトリガーされます。{{site.data.keyword.appconserviceshort}} ダッシュボード上で、フローの状況を確認できます。フローに関するログを表示するには、ハンバーガー・メニュー ![ハンバーガー・メニュー・アイコン](/images/HamburgerMenuSm.jpg) を開き、**「管理」**を展開してから、**「ログ」**をクリックします。

イベント・ドリブン・フローの作成やその例について詳しくは、[Creating an event-driven flow ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/creating-event-driven-flow/) を参照してください。

## API 用のフローの作成

クラウド・ベースのアプリケーション内のデータを利用するアプリケーションを開発者が作成できるようにする場合は、API を提供できます。API 用のフローを作成するには、以下の手順を実行します。
1. {{site.data.keyword.appconserviceshort}} ダッシュボードで、**「新規 (New)」** > **「API 用のフロー (Flows for an API)」**をクリックします。
1. API の名前を入力します。
1. API で処理するオブジェクトのタイプを反映したモデルの名前を入力してから、**「モデルの作成 (Create model)」**をクリックします。
1. API で処理するオブジェクトの構造の定義に必要なプロパティーを追加します。
    例えば、API で顧客を作成するか取得する場合は、Customer_ID、First_Name、Last_Name、Email_Address と呼ばれるプロパティーを追加することができます。プロパティーの名前を入力するか、または**「アプリケーションからプロパティーを選択 (Select properties from applications)」**をクリックし、接続しようとしている 1 つ以上のアプリケーションからプロパティーを選択します。
1. **「操作」**をクリックして、API とオブジェクトの間で対話する方法を定義し、必要な操作を追加します。 
1. 操作ごとに、**「フローの実装 (Implement flow)」**をクリックして、各操作の働きを定義するフローを作成します。 
1. フロー内の要求と応答の間に 1 つ以上のターゲット・アプリケーションを追加します。
    条件によって異なるアクションをフローに実行させようとしている場合は、条件ロジックを追加することもできます ([Adding conditional logic to a flow ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/adding-conditional-logic-flow/)を参照)。
1. フロー内で**「応答」**をクリックして、操作の実行の終了時に戻される応答を定義します。ターゲット・アプリケーションから使用可能なフィールドをマップします。 
1. **「完了」**をクリックして、モデルに戻ります。
1. すべてのモデルと操作を定義し終えたら、メニューから**「API の開始 (Start API)」**を選択して、API を開始します。 

API 用のフローを作成し終えました。{{site.data.keyword.appconserviceshort}} ダッシュボード上で、API 用のフローは API アイコンで識別されます。このフローは、その他のフローと同じ方法で開始したり停止したりできます。API を実行中に開くことはできますが、編集する場合はその前に停止する必要があります。

API 用のフローの作成方法やその例について詳しくは、[Creating flows for an API ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/creating-flows-api/) を参照してください。

API をテストする方法については、[Exposing an App Connect flow through API Connect ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://developer.ibm.com/integration/blog/2017/08/29/exposing-app-connect-flow-api-connect/) を参照してください。


## IBM Integration Bus 統合ソリューションの実行 (エンタープライズ・ベータ版)

IT インフラストラクチャーを獲得したり保守したりせずに、IBM Integration Bus または App Connect Enterprise 内で開発済みの統合ソリューションをクラウドにデプロイしようとしている場合は、統合ソリューションを構成するすべての成果物が含まれる BAR ファイルをインポートしてから、そのコンテンツを App Connect 内の統合サーバー内で実行できます。BAR ファイルを App Connect にアップロードするには、IBM Integration Bus バージョン 10.0.0.4 以降か App Connect Enterprise がオンプレミスでインストール済みでなければなりません。

App Connect 内で Integration Bus または App Connect Enterprise ソリューションを実行するには、以下の手順を実行します。
1. {{site.data.keyword.appconserviceshort}} ダッシュボードで、**「新規 (New)」** > **「BAR ファイルのインポート (Import a BAR file)」**をクリックします。
1. インポートしようとしている BAR ファイルを選択し、必要に応じて名前を編集してから、**「インポート」**をクリックします。
    認証エラーが発生した場合は、BAR ファイルが有効か確認してください ([What makes a BAR file valid in App Connect? ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/what-makes-a-bar-file-valid-for-app-connect-app-connect-enterprise-beta) を参照)。
    統合サーバーが作成され、統合サーバーを表すタイルがダッシュボードに追加されます。統合サーバーの構成と開始の準備ができると、状況が「準備中 (Preparing)」から「停止」に変わります。 
1. タイルをクリックすると、統合サーバーが開きます。
1. 以下のように、統合サーバーを構成します。
    * 統合ソリューションの説明を追加するか編集します。
    * HTTPS 基本認証を構成します ([Configuring HTTPS basic authentication ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/configuring-https-basic-authentication-app-connect-enterprise-beta) を参照)。
    * オンプレミス・システムに接続できるように、ポリシーを付加します ([Configuring secure connectivity between integration servers on App Connect and on-premises systems ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/configuring-secure-connectivity-between-integration-servers-on-app-connect-and-on-premises-systems-app-connect-enterprise-beta) を参照)。
1. オプション: オンプレミス環境と App Connect の間でメッセージ・フロー処理を分割するには、ハンバーガー・メニュー ![ハンバーガー・メニュー・アイコン](/images/HamburgerMenuSm.jpg) を開き、**「管理」**を展開し、**「呼び出し可能フロー (Callable flows)」**を選択して、呼び出し可能フローを構成します ([Sharing message flow processing between App Connect and Integration Bus ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/sharing-message-flow-processing-between-app-connect-and-integration-bus-app-connect-enterprise-beta) を参照)。
1. 構成が完了したら、App Connect ダッシュボードに戻り、タイル・メニューを開き**「開始」**をクリックして統合サーバーを開始します。

統合サーバーの稼働中には、統合サーバーを開いて**「ログのダウンロード (Download logs)」**または**「ログの表示 (View logs)」**をクリックすると、ログを表示したりダウンロードしたりできます。ログを表示するには、ロギング・ポリシーを統合サーバーに付加する必要があります ([Viewing logs for your integration servers ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/viewing-logs-for-your-integration-servers-in-app-connect-enterprise-beta) を参照)。

詳しくは、[Running your Integration Bus solutions in App Connect ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan) を参照してください。
