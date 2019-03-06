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


# IBM App Connect 疑難排解
{: #troubleshooting}

若要疑難排解 {{site.data.keyword.appconservicefull}} 流程及整合伺服器的問題，您可以在 Kibana 中檢視日誌。如果您在使用 {{site.data.keyword.appconserviceshort}} 時有問題或疑問，請搜尋資訊或透過討論區提問來取得協助。使用討論區提問時，請標記您的問題，以便 {{site.data.keyword.Bluemix}} 及 {{site.data.keyword.appconserviceshort}} 開發團隊能看到它。

-   在 {{site.data.keyword.appconserviceshort}} 儀表板上，查看執行中流程的磚。如果有綠色記號，表示已順利執行流程；按一下記號，以查看上次何時觸發流程。

    ![擷取畫面，顯示已順利執行流程](/images/SuccessfulFlow.jpg)

    如果有紅色驚嘆號，表示發生問題：按一下驚嘆號，以瞭解哪裏發生錯誤。![擷取畫面，顯示流程發生問題](/images/ErroredFlow.jpg)

-   檢查 {{site.data.keyword.appconserviceshort}} 狀態頁面，以查看是否有任何現行已知問題或規劃任何維護：[{{site.data.keyword.appconserviceshort}} 狀態頁面 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://developer.ibm.com/integration/docs/app-connect/app-connect-status/)
-   若要檢視流程的日誌資訊，請按一下 {{site.data.keyword.appconserviceshort}} 漢堡功能表中的**日誌**。依預設，會在 Kibana 中顯示流程的錯誤及參考訊息，而您可以在其中檢視特定時間範圍的資料，或使用過濾器來顯示特定類型的資訊。若要檢視流程的除錯資訊，請在 {{site.data.keyword.appconserviceshort}} 儀表板的流程磚上開啟功能表，然後選取**啟用除錯記載**。您接著需要重新啟動流程，才會啟動除錯記載。請注意，當您啟用除錯記載時，IBM 操作員可以看到除錯日誌項目（可能包括有效負載資料）。若要進一步瞭解除錯記載，請參閱 [Debugging your message flows in {{site.data.keyword.appconserviceshort}}](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/debugging-message-flows-ibm-app-connect/)。若要進一步瞭解 Kibana，請參閱 [Kibana 文件 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://www.elastic.co/guide/en/kibana/4.0/discover.html)。
-   若要檢視整合伺服器的日誌資訊，請開啟整合伺服器，然後按一下**下載日誌**或**檢視日誌**。若要在 Kibana 中檢視整合伺服器的日誌，您必須將「記載」原則附加至該整合伺服器（請參閱 [Viewing logs for your integration servers ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/viewing-logs-for-your-integration-servers-in-app-connect-enterprise-beta)）。
-   在 [Frequently asked questions about {{site.data.keyword.appconserviceshort}} ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://developer.ibm.com/integration/docs/app-connect/faq/) 中，尋找 {{site.data.keyword.appconserviceshort}} 常見問題的答案。
-   在 [Tutorials for {{site.data.keyword.appconserviceshort}} ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/) 中，遵循如何連接應用程式的逐步指示。
-   如果您有使用 {{site.data.keyword.appconserviceshort}} 開發或部署應用程式的相關技術問題，請將問題張貼在 [Stack Overflow ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](http://stackoverflow.com/search?q=app-connect+ibm-bluemix)，並使用 "ibm-bluemix" 和 "app-connect"（含連字號）來標記問題。
-   若為服務及開始使用指示的相關問題，請使用 [IBM developerWorks&reg; dW Answers ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://developer.ibm.com/answers/topics/app_connect/?smartspace=bluemix) 討論區。請包含標籤 "bluemix" 及 "app_connect"（含底線）。

    如需使用 {{site.data.keyword.Bluemix}} 支援機制的相關資訊，請參閱[取得協助 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://console.ng.bluemix.net/docs/support/index.html#getting-help)。


