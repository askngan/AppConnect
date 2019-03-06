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


# IBM App Connect のトラブルシューティング
{: #troubleshooting}

{{site.data.keyword.appconservicefull}} のフローと統合サーバーに関する問題をトラブルシューティングするために、Kibana でログを表示することができます。{{site.data.keyword.appconserviceshort}} の使用中に疑問または問題が生じた場合は、情報を検索するか、またはフォーラムで質問して支援を受けてください。フォーラムを使用して質問するときは、{{site.data.keyword.Bluemix}} と {{site.data.keyword.appconserviceshort}} の開発チームの目に留まるように、質問にタグを付けてください。

-   {{site.data.keyword.appconserviceshort}} ダッシュボード上の実行中のフローのタイルを確認します。緑のチェック・マークが付いている場合、フローは正常に実行済みです。フローが最後にトリガーされたときを確認するには、そのチェック・マークをクリックします。

    ![フローが正常に実行済みであることを示しているスクリーン・ショット](/images/SuccessfulFlow.jpg)

    赤の感嘆符が付いている場合、なにか問題があります。何が失敗したかを確認するには、その感嘆符をクリックします。![フローに問題があることを示しているスクリーン・ショット](/images/ErroredFlow.jpg)

-   現在既知の問題があるかどうか、または保守が計画されているかどうかを調べるには、次の {{site.data.keyword.appconserviceshort}} の状況ページを確認します。[{{site.data.keyword.appconserviceshort}} の状況ページ ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://developer.ibm.com/integration/docs/app-connect/app-connect-status/)
-   フローのログ情報を表示するには、{{site.data.keyword.appconserviceshort}} のハンバーガー・メニューにある**「ログ」**をクリックします。フローのエラー・メッセージと情報メッセージは、デフォルトでは Kibana に表示され、そこで特定の時刻範囲のデータを表示でき、またフィルターを使用して特定のタイプの情報を表示することもできます。フローのデバッグ情報を表示するには、{{site.data.keyword.appconserviceshort}} ダッシュボードでフローのタイルのメニューを開いて、**「デバッグ・ロギングの有効化 (Enable debug logging)」**を選択します。次に、デバッグ・ロギングを開始するために、フローを再始動する必要があります。デバッグ・ロギングを有効にした場合、デバッグ・ログ・エントリー (ペイロード・データが含まれる可能性がある) が IBM のオペレーターに表示されることに注意してください。デバッグ・ロギングについて詳しくは、[Debugging your message flows in {{site.data.keyword.appconserviceshort}}](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/debugging-message-flows-ibm-app-connect/) を参照してください。Kibana について詳しくは、[Kibana の資料 ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://www.elastic.co/guide/en/kibana/4.0/discover.html) を参照してください。
-   統合サーバーのログ情報を表示するには、統合サーバーを開いて**「ログのダウンロード (Download logs)」**または**「ログの表示 (View logs)」**をクリックします。Kibana で統合サーバーのログを表示するには、その統合サーバーにロギング・ポリシーを付加する必要があります ([Viewing logs for your integration servers ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/viewing-logs-for-your-integration-servers-in-app-connect-enterprise-beta) を参照)。
-   {{site.data.keyword.appconserviceshort}} に関するよくある質問の回答は、[Frequently asked questions about {{site.data.keyword.appconserviceshort}}
![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://developer.ibm.com/integration/docs/app-connect/faq/) で検索してください。
-   [Tutorials for {{site.data.keyword.appconserviceshort}} ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/) にあるアプリケーションの接続方法に関するステップバイステップの説明に従ってください。
-   {{site.data.keyword.appconserviceshort}} を使用したアプリケーションの開発やデプロイについて技術的な質問がある場合は、質問を [Stack Overflow ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](http://stackoverflow.com/search?q=app-connect+ibm-bluemix) に投稿し、その質問に「ibm-bluemix」と「app-connect」(ハイフン付き) のタグを付けます。
-   サービスや使用開始の手順についての質問には、[IBM developerWorks&reg; dW Answers ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://developer.ibm.com/answers/topics/app_connect/?smartspace=bluemix) フォーラムを使用してください。「bluemix」と「app_connect」(下線付き) のタグを含めます。

    {{site.data.keyword.Bluemix}} サポート・メカニズムの使用について詳しくは、[Getting help ![外部リンク・アイコン](../../icons/launch-glyph.svg "外部リンク・アイコン")](https://console.ng.bluemix.net/docs/support/index.html#getting-help) を参照してください。


