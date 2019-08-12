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

-   在 {{site.data.keyword.appconserviceshort}} 儀表板上，查看執行中流程的磚。如果有綠色記號，表示流程順利執行；請按一下記號，以查看上次觸發流程的時間。

    ![顯示流程順利執行的擷取畫面](/images/SuccessfulFlow.jpg)

    如果有紅色驚嘆號，表示發生問題；請按一下驚嘆號，以找出問題所在。![顯示流程發生問題的擷取畫面](/images/ErroredFlow.jpg)

-   檢查 {{site.data.keyword.appconserviceshort}} 狀態頁面，以查看是否報告任何問題或規劃任何維護：[{{site.data.keyword.appconserviceshort}} 狀態頁面 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://developer.ibm.com/integration/docs/app-connect/app-connect-status/)
-   若要檢視流程的日誌資訊，請按一下 {{site.data.keyword.appconserviceshort}} 功能表中的**日誌**。依預設，會在 Kibana 中顯示流程的錯誤及參考訊息，而您可以在其中檢視特定時間範圍的資料，或使用過濾器來顯示特定類型的資訊。若要檢視流程的除錯資訊，請在 {{site.data.keyword.appconserviceshort}} 儀表板的流程磚上開啟功能表，然後選取**啟用除錯記載**。您接著需要重新啟動流程，才會啟動除錯記載。當您啟用除錯記載時，IBM 操作員可以看到除錯日誌項目（可能包括有效負載資料）。若要進一步瞭解除錯記載，請參閱 [Debugging your message flows in {{site.data.keyword.appconserviceshort}} ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/debugging-message-flows-ibm-app-connect/)。若要進一步瞭解 Kibana，請參閱 [Kibana 文件 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://www.elastic.co/guide/en/kibana/4.0/discover.html)。
-   若要檢視整合伺服器的日誌資訊，請開啟整合伺服器，然後按一下**下載日誌**或**檢視日誌**。若要在 Kibana 中檢視整合伺服器的日誌，您必須將「記載」原則附加至該整合伺服器（請參閱 [Viewing logs for your integration servers ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/viewing-logs-for-your-integration-servers-in-app-connect-enterprise-beta)）。
-   在 [Frequently asked questions about {{site.data.keyword.appconserviceshort}} ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://developer.ibm.com/integration/docs/app-connect/faq/) 中，尋找 {{site.data.keyword.appconserviceshort}} 常見問題的答案。
-   在 [Tutorials for {{site.data.keyword.appconserviceshort}} ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/) 中，遵循如何連接應用程式的逐步指示。
-   若為服務及開始使用指示的相關問題，請使用 [IBM dW Answers ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://developer.ibm.com/answers/topics/app_connect) 討論區。請包含標籤 "ibm_cloud" 和 "app_connect"（含底線）。

    如需使用 {{site.data.keyword.Bluemix}} 支援機制的相關資訊，請參閱 [Support ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://cloud.ibm.com/unifiedsupport/supportcenter)。

## 向 IBM App Connect 團隊報告問題
{: #reporting}

如果您遵循疑難排解建議但仍然遭遇問題，可以從 {{site.data.keyword.appconserviceshort}} 團隊取得協助。從 {{site.data.keyword.appconserviceshort}} 功能表中，依序按一下**與我們聯絡**和**取得支援**。使用您的 IBM ID 登入、按一下**建立案例**，並且盡可能提供下列資訊。（您也可以按一下 {{site.data.keyword.Bluemix}}  主控台中的**支援**。） 

* 您已在其中佈建 {{site.data.keyword.appconserviceshort}} 實例的 {{site.data.keyword.Bluemix}} 地區。（例如，達拉斯或倫敦。）
* 您所使用之 {{site.data.keyword.appconserviceshort}} 服務的實例 ID。（您可以藉由查看「{{site.data.keyword.appconserviceshort}} 實例 ID」下的帳戶資訊來尋找此 ID。）
* 您遭遇的問題。（例如，問題是否與特定應用程式或功能有關。）
* 批次 ID，如果問題與批次處理相關。（如果批次處理程序發生錯誤，並且您已在批次處理程序中為每筆記錄定義了 ID，則可以在 Kibana 日誌的 "batch-record-id_str" 直欄中找到已定義的 ID；請參閱 [How to use batch processing in {{site.data.keyword.appconserviceshort}} ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://developer.ibm.com/integration/docs/app-connect/toolbox-utilities/how-to-use-batch-processing-in-ibm-app-connect/)。）
* 問題第一次發生的日期和時間（包括時區），以及問題發生前流程執行的時間長度。
* 問題是否仍然存在，以及您是否可以抄寫。
* 適用的話，您所使用的瀏覽器類型和版本。（我們僅支援最新的瀏覽器版本。）
* 所有用來說明問題的日誌項目。
* 問題對您的業務產生的影響。
