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


# 入門指導教學
{: #getting-started}

{{site.data.keyword.appconservicefull}} 可協助您連接應用程式：從簡單觸發動作互動到複雜整合。您可以使用 {{site.data.keyword.appconserviceshort}} 來建立事件驅動流程或 API 的流程。或者，您可以上傳及執行在 IBM Integration Bus 中所建立的整合解決方案，而不需要獲得及維護 IT 基礎架構。您可以在 {{site.data.keyword.appconserviceshort}} 儀表板的一個位置查看及管理所有整合（整合伺服器、事件驅動流程及流程的 API）。 

在您建立 {{site.data.keyword.appconserviceshort}} 服務實例之後，可以從 {{site.data.keyword.Bluemix}} 儀表板存取 {{site.data.keyword.appconserviceshort}}。

下列步驟提供足夠的資訊，以供您開始使用 App Connect。如需詳細指示、特定應用程式的作法手冊、指導教學及視訊，請參閱 [IBM App Connect ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://developer.ibm.com/integration/docs/app-connect/) 上的完整文件集。

## 建立事件驅動流程

顧名思義，事件驅動流程包含來源應用程式中可觸發流程的事件，以及目標應用程式中的一個以上動作。因此，在來源應用程式中發生某件事時，會在目標應用程式中觸發動作。若要建立可連接您雲端型應用程式的事件驅動流程，請完成下列步驟。
1.  在 {{site.data.keyword.appconserviceshort}} 儀表板上，按一下**新建** > **事件驅動流程**。
    {{site.data.keyword.appconserviceshort}} 會自動即時儲存您的變更。如果您在任何階段離開流程，則會將流程儲存為草稿流程，您可以在其他時間完成。
1.  輸入流程的名稱。
1.  展開應用程式並選取事件，以選取觸發事件來啟動流程。
1.  如果您尚未連接至應用程式，請按一下**連接至_應用程式_**，並輸入應用程式的登入詳細資料。
    您可能需要提供部分應用程式的額外連線詳細資料；如果您需要協助尋找特定應用程式的認證，請參閱 [How-to guides for apps ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://developer.ibm.com/integration/docs/app-connect/how-to-guides-for-apps/)。
1.  展開應用程式並選取動作，以選取要在第二個應用程式中觸發的動作。
    必要的話，請按一下**連接至應用程式**，並輸入目標應用程式的登入詳細資料。
1. 輸入您要在應用程式之間傳送的資料。
    您可以按一下欄位並按一下對映圖示 ![對映圖示](/images/MappingIcon.jpg)，以手動新增來源欄位名稱。您也可以鍵入文字，或使用轉換函數來自訂來源值。如需相關資訊，請參閱 [How to use transformations ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://developer.ibm.com/integration/docs/app-connect/faq/#faq_transforms)。
1. 選用項目：您可以執行下列事項來修正流程運作方式：
    * 按一下流程中的加號圖示 ![新增應用程式圖示](/images/AddApp.jpg)，以新增更多目標應用程式及動作。
    * 將擷取動作新增至流程，以擷取符合特定準則的項目或擷取指定數目的記錄。您也可以新增用來定義錯誤處理，或定義如何處理已擷取項目的擷取動作（請參閱 [Using App Connect to retrieve items from your applications ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/using-ibm-app-connect-retrieve-items-applications/)）。
    * 新增部分條件式邏輯，以根據從流程中應用程式接收到的資料來執行不同動作（請參閱 [Adding conditional logic to a flow ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/adding-conditional-logic-flow/)）。

1. 已配置流程時，請開啟標頭列上的選項功能表，然後按一下**啟動流程**。

如果您回到 {{site.data.keyword.appconserviceshort}} 儀表板，則可以看到流程正在執行中。在第一個應用程式中發生事件時，第二個應用程式中的 {{site.data.keyword.appconserviceshort}} 會自動觸發動作。您可以在 {{site.data.keyword.appconserviceshort}} 儀表板上檢視流程的狀態。若要檢視流程的日誌，請開啟漢堡功能表 ![漢堡功能表圖示](/images/HamburgerMenuSm.jpg)，並展開**管理**，然後按一下**日誌**。

如需相關資訊，請參閱[建立事件驅動流程 ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/creating-event-driven-flow/)。

## 建立 API 的流程

如果您希望開發人員建立的應用程式，能夠使用雲端型應用程式中的資料，則可以提供 API。若要建立 API 的流程，請完成下列步驟。
1. 在 {{site.data.keyword.appconserviceshort}} 儀表板上，按一下**新建** > **API 的流程**。
1. 輸入 API 的名稱。
1. 輸入反映 API 使用之物件類型的模型名稱，然後按一下**建立模型**。
1. 新增定義 API 使用之物件結構所需的內容。
    例如，如果 API 會建立或擷取客戶，則您可能會新增稱為 Customer_ID、First_Name、Last_Name 及 Email_Address 的內容。您可以鍵入內容的名稱，或按一下**從應用程式選取內容**以從您已連接的一個以上應用程式中選擇內容。
1. 按一下**作業**，以定義 API 如何與物件互動，然後新增您需要的作業。 
1. 對於每個作業，按一下**實作流程**，以建立定義每個作業運作方式的流程。 
1. 在要求與回應之間，將一個以上的目標應用程式新增至流程。
    如果您要流程針對不同的條件執行不同的事物，則也可以新增某個條件式邏輯（請參閱 [Adding conditional logic to a flow ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/adding-conditional-logic-flow/)）。
1. 按一下流程中的**回應**，以定義在完成作業時所傳回的回應。從目標應用程式中對映可用的欄位。 
1. 按一下**完成**，以回到您的模型。
1. 定義所有模型和作業後，請從功能表中選取**啟動 API** 來啟動 API。 

您的 API 流程已備妥。在 {{site.data.keyword.appconserviceshort}} 儀表板上，API 的流程是透過 API 圖示所識別。您可以使用與任何其他流程相同的方式來啟動及停止它們。您可以開啟正在執行的 API，但必須先停止它，才能進行編輯。

如需相關資訊，請參閱 [Creating flows for an API ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/creating-flows-api/)。

若要瞭解如何測試 API，請參閱 [Exposing an App Connect flow through API Connect ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://developer.ibm.com/integration/blog/2017/08/29/exposing-app-connect-flow-api-connect/)。


## 執行 IBM Integration Bus 整合解決方案

您可以將在 IBM Integration Bus 或 App Connect Enterprise 中開發的整合解決方案部署至雲端，而不需要獲得及維護 IT 基礎架構。匯入包含構成整合解決方案之所有構件的 BAR 檔案，然後在 App Connect 中執行整合伺服器的內容。若要將 BAR 檔案上傳至 App Connect，您必須具有 IBM Integration Bus 10.0.0.4 版或更新版本，或已在內部部署安裝的 App Connect Enterprise。

若要在 App Connect 中執行 Integration Bus 或 App Connect Enterprise 解決方案，請完成下列步驟。
1. 在 {{site.data.keyword.appconserviceshort}} 儀表板上，按一下**新建** > **匯入 BAR 檔案**。
1. 選取您要匯入的 BAR 檔案，並視需要編輯名稱，然後按一下**匯入**。
    如果您看到鑑別錯誤，則請檢查 BAR 檔案是否有效（請參閱 [What makes a BAR file valid in App Connect? ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/what-makes-a-bar-file-valid-for-app-connect-app-connect-enterprise-beta)）。已建立整合伺服器，並在儀表板中新增磚來代表它。準備好要配置及啟動整合伺服器時，狀態會從「準備中」變更為「已停止」。 
1. 按一下磚以開啟整合伺服器。
1. 配置整合伺服器：
    * 新增或編輯整合解決方案的說明。
    * 配置 HTTPS 基本鑑別（請參閱 [Configuring HTTPS basic authentication ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/configuring-https-basic-authentication-app-connect-enterprise-beta)）。
    * 附加原則，以連接至內部部署系統（請參閱 [Configuring secure connectivity between integration servers on App Connect and on-premises systems ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/configuring-secure-connectivity-between-integration-servers-on-app-connect-and-on-premises-systems-app-connect-enterprise-beta)）。
1. 選用項目：若要在內部部署環境與 App Connect 之間分割訊息流程處理，請配置可呼叫的流程。開啟漢堡功能表 ![「漢堡功能表」圖示](/images/HamburgerMenuSm.jpg)、展開**訊息**，然後選取**可呼叫流程**（請參閱 [Sharing message flow processing between App Connect and Integration Bus ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/sharing-message-flow-processing-between-app-connect-and-integration-bus-app-connect-enterprise-beta)）。
1. 配置完成後，請回到 App Connect 儀表板，並啟動整合伺服器，方法是開啟磚功能表，然後按一下**啟動**。

當您的整合伺服器正在執行時，可以開啟整合伺服器，並按一下**下載日誌**或**檢視日誌**，來檢視及下載日誌。若要檢視日誌，您必須將「記載」原則附加至整合伺服器（請參閱 [Viewing logs for your integration servers ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/viewing-logs-for-your-integration-servers-in-app-connect-enterprise-beta)）。

如需相關資訊，請參閱 [Running your Integration Bus solutions in App Connect ![外部鏈結圖示](../../icons/launch-glyph.svg "外部鏈結圖示")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan)。
