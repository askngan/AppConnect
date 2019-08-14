---

copyright:
  years: 2017, 2019
lastupdated: "2019-08-14"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip} 
{:download: .download}


# IBM App Connect のトラブルシューティング
{: #troubleshooting}

{{site.data.keyword.appconservicefull}} のフローと統合サーバーに関する問題をトラブルシューティングするために、Kibana でログを表示することができます。 {{site.data.keyword.appconserviceshort}} の使用中に疑問または問題が生じた場合は、情報を検索するか、またはフォーラムで質問して支援を受けてください。 フォーラムを使用して質問するときは、{{site.data.keyword.Bluemix}} と {{site.data.keyword.appconserviceshort}} の開発チームの目に留まるように、質問にタグを付けてください。

-   {{site.data.keyword.appconserviceshort}} ダッシュボード上の実行中のフローのタイルを確認します。 緑のチェック・マークが付いている場合、フローは正常に実行されています。フローが最後にトリガーされたときを確認するには、そのチェック・マークをクリックします。

    ![フローが正常に実行されていることを示す画面キャプチャー](/images/SuccessfulFlow.jpg)

    赤の感嘆符が付いている場合、何か問題があります。何が問題かを確認するには、その感嘆符をクリックします。![フローに問題があることを示す画面キャプチャー](/images/ErroredFlow.jpg)

-   何か問題が報告されているか、または保守が計画されているかどうかを調べるには、次の {{site.data.keyword.appconserviceshort}} の状況ページを確認します。[{{site.data.keyword.appconserviceshort}} の状況ページ ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://developer.ibm.com/integration/docs/app-connect/app-connect-status/)
-   フローのログ情報を表示するには、{{site.data.keyword.appconserviceshort}} のメニューにある**「ログ」**をクリックします。フローのエラー・メッセージと情報メッセージは、デフォルトでは Kibana に表示され、そこで特定の時刻範囲のデータを表示でき、またフィルターを使用して特定のタイプの情報を表示することもできます。 フローのデバッグ情報を表示するには、{{site.data.keyword.appconserviceshort}} ダッシュボードでフローのタイルのメニューを開いて、**「デバッグ・ロギングの有効化 (Enable debug logging)」**を選択します。  次に、デバッグ・ロギングを開始するために、フローを再始動する必要があります。デバッグ・ロギングを有効にした場合、デバッグ・ログ・エントリー (ペイロード・データが含まれる可能性がある) が IBM のオペレーターに表示されます。デバッグ・ロギングについて詳しくは、[Debugging your message flows in {{site.data.keyword.appconserviceshort}} ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/debugging-message-flows-ibm-app-connect/) を参照してください。  Kibana について詳しくは、[Kibana の資料 ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://www.elastic.co/guide/en/kibana/4.0/discover.html) を参照してください。
-   統合サーバーのログ情報を表示するには、統合サーバーを開いて**「ログのダウンロード (Download logs)」**または**「ログの表示 (View logs)」**をクリックします。  Kibana で統合サーバーのログを表示するには、その統合サーバーにロギング・ポリシーを付加する必要があります ([Viewing logs for your integration servers ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/viewing-logs-for-your-integration-servers-in-app-connect-enterprise-beta) を参照)。
-   {{site.data.keyword.appconserviceshort}} に関するよくある質問の回答は、[Frequently asked questions about {{site.data.keyword.appconserviceshort}}
![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://developer.ibm.com/integration/docs/app-connect/faq/) で検索してください。
-   [Tutorials for {{site.data.keyword.appconserviceshort}} ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/) にあるアプリケーションの接続方法に関するステップバイステップの説明に従ってください。
-   サービスや使用開始の手順についての質問には、[IBM dW Answers ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://developer.ibm.com/answers/topics/app_connect) フォーラムを使用してください。 「ibm_cloud」と「app_connect」(下線付き) のタグを含めます。

    {{site.data.keyword.Bluemix}} サポート・メカニズムの使用について詳しくは、[Support![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://cloud.ibm.com/unifiedsupport/supportcenter) を参照してください。

## IBM App Connect チームに問題を報告する
{: #reporting}

トラブルシューティングに関するアドバイスに従っても依然として問題が解決しない場合は、{{site.data.keyword.appconserviceshort}} チームに援助してもらうことができます。{{site.data.keyword.appconserviceshort}} メニューで、**「詳しくはお問い合わせください」**をクリックしてから、**「サポートの利用」**をクリックします。ご使用の IBMid でサインインし、**「Case の作成 (Create a case)」**をクリックし、以下の情報をできるだけ多く提供してください。(また、{{site.data.keyword.Bluemix}} コンソールの**「サポート」**をクリックすることもできます。) 

* {{site.data.keyword.appconserviceshort}} のインスタンスがプロビジョンされている {{site.data.keyword.Bluemix}} 地域。(例えば、ダラスまたはロンドン。)
* 使用している {{site.data.keyword.appconserviceshort}} サービスのインスタンス ID。(この ID は、{{site.data.keyword.appconserviceshort}} インスタンス ID のアカウント情報を見ると分かります。)
* 発生している問題。(例えば、問題は特定のアプリケーションまたは機能に特有かどうか。)
* 問題がバッチ処理に関連している場合は、バッチ ID。(エラーがバッチ処理で発生していて、バッチ処理の各レコードの ID を既に定義している場合、定義した ID は Kibana ログの "batch-record-id_str" 列にあります。[How to use batch processing in {{site.data.keyword.appconserviceshort}} ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://developer.ibm.com/integration/docs/app-connect/toolbox-utilities/how-to-use-batch-processing-in-ibm-app-connect/)を参照してください。)
* 問題が最初に発生した日時 (タイム・ゾーンを含む)、および問題発生前にフローが実行されていた時間の長さ。
* 問題が依然として発生しているか、および再現できるかどうか。
* 該当する場合、使用しているブラウザーのタイプとバージョン。(最新バージョンのブラウザーだけをサポートしています。)
* 問題を説明するすべてのログ・エントリー。
* 問題がビジネスに与えているインパクト。
