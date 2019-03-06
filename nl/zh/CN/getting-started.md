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


# IBM App Connect 入门
{: #gettingStarted}

{{site.data.keyword.appconservicefull}} 可帮助您连接应用程序：从简单的触发/操作交互到复杂的集成。您可以使用 {{site.data.keyword.appconserviceshort}} 来创建事件驱动的流或 API 流；或者可以上传并运行在 IBM Integration Bus 中创建的集成解决方案，而无需获取和维护 IT 基础架构。您可以在 {{site.data.keyword.appconserviceshort}} 仪表板上的一个位置中查看和管理所有集成 - 集成服务器、事件驱动的流和 API 流。 

创建 {{site.data.keyword.appconserviceshort}} 服务实例后，可以在 {{site.data.keyword.Bluemix}}“仪表板”中访问 {{site.data.keyword.appconserviceshort}}。

以下步骤提供了足够的信息，供您开始使用 App Connect。有关更详细的指示信息、特定应用程序的操作指南、教程和视频，请参阅 [IBM App Connect ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://developer.ibm.com/integration/docs/app-connect/) 上的完整文档集。

## 创建事件驱动的流

顾名思义，事件驱动的流由源应用程序中的事件（用于触发流）以及目标应用程序中的一个或多个操作组成。因此，源应用程序中发生事件时，会在目标应用程序中触发操作。要创建事件驱动的流以用于连接基于云的应用程序，请完成以下步骤。
1.  在 {{site.data.keyword.appconserviceshort}} 仪表板上，单击**新建** > **事件驱动的流**。
    {{site.data.keyword.appconserviceshort}} 会在您执行操作时自动保存更改。如果您在任何阶段离开流，流会保存为草稿流，您可以在其他时间完成此流。
1.  输入流的名称。
1.  通过展开应用程序并选择事件来选择用于启动流的触发器事件。
1.  如果尚未连接到应用程序，请单击**连接到_应用程序_**，然后输入应用程序的登录详细信息。
    您可能必须为某些应用程序提供其他连接详细信息；如果需要有关查找特定应用程序的凭证的帮助，请参阅 [How-to guides for apps ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://developer.ibm.com/integration/docs/app-connect/how-to-guides-for-apps/)。
1.  通过展开应用程序并选择操作，选择要在第二个应用程序中触发的操作。
    如果需要，请单击**连接到应用程序**，然后输入目标应用程序的登录详细信息。
1. 输入要在应用程序之间传输的数据。
    可以通过单击字段，然后单击“映射”图标 ![“映射”图标](/images/MappingIcon.jpg) 来手动添加源字段名称。您还可以输入文本，或使用转换函数来定制源值。有关更多信息，请参阅[如何使用转换 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://developer.ibm.com/integration/docs/app-connect/faq/#faq_transforms)。
1. 可选：可以通过执行以下操作来优化流的工作方式：
    * 通过单击流中的加号图标 ![“添加应用程序”图标](/images/AddApp.jpg)，添加更多目标应用程序和操作。
    * 向流添加“检索”操作，以检索符合特定条件的项，检索指定数量的记录，定义错误处理或定义如何处理检索到的项（请参阅 [Using App Connect to retrieve items from your applications ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/using-ibm-app-connect-retrieve-items-applications/)）。
    * 添加一些条件逻辑，以根据从流中的应用程序中收到的数据来执行不同的操作（请参阅 [Adding conditional logic to a flow ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/adding-conditional-logic-flow/)）。

1. 配置流后，打开标题栏上的“选项”菜单，然后单击**启动流**。

如果返回到 {{site.data.keyword.appconserviceshort}} 仪表板，即可以看到该流在运行。在第一个应用程序中发生事件时，{{site.data.keyword.appconserviceshort}} 会在第二个应用程序中自动触发操作。可以在 {{site.data.keyword.appconserviceshort}} 仪表板上查看流的状态。要查看流的日志，请打开汉堡菜单 ![“汉堡菜单”图标](/images/HamburgerMenuSm.jpg)，展开**管理**，然后单击**日志**。

有关创建事件驱动的流的更详细信息（包括一些示例），请参阅 [Creating an event-driven flow ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/creating-event-driven-flow/)。

## 创建 API 流

如果您希望开发者能够创建应用程序来利用基于云的应用程序中的数据，那么可以提供 API。要创建 API 流，请完成以下步骤。
1. 在 {{site.data.keyword.appconserviceshort}} 仪表板上，单击**新建** > **API 流**。
1. 输入 API 的名称。
1. 为模型输入可反映 API 将使用的对象类型的名称，然后单击**创建模型**。
1. 添加属性以用于定义 API 将使用的对象的结构。
    例如，如果 API 将创建或检索客户，那么可添加名为 Customer_ID、First_Name、Last_Name 和 Email_Address 的属性。可以输入属性的名称，也可以单击**从应用程序中选择属性**，以从连接到的一个或多个应用程序中选择属性。
1. 单击**操作**以定义 API 将与对象交互的方式，并添加所需的操作。 
1. 对于每个操作，单击**实现流**以创建定义每个操作如何工作的流。 
1. 向流添加一个或多个目标应用程序（位于请求和响应之间）。
    如果希望流针对不同条件执行不同操作，那么还可以添加一些条件逻辑（请参阅 [Adding conditional logic to a flow ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/adding-conditional-logic-flow/)）。
1. 单击流中的**响应**，以定义在执行操作后将返回的响应。映射目标应用程序中的可用字段。 
1. 单击**完成**以返回到模型。
1. 定义了所有模型和操作后，从菜单中选择**启动 API** 以启动 API。 

您已创建了 API 流。在 {{site.data.keyword.appconserviceshort}} 仪表板上，API 流用 API 图标标识。您可以像操作其他任何流一样，启动和停止这些流。您可以在 API 运行期间将其打开，但必须将其停止后，才能对其进行编辑。

有关如何创建 API 流的更详细信息（包括示例），请参阅 [Creating flows for an API  ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/creating-flows-api/)。

要了解如何测试 API，请参阅 [Exposing an App Connect flow through API Connect ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://developer.ibm.com/integration/blog/2017/08/29/exposing-app-connect-flow-api-connect/)。


## 运行 IBM Integration Bus 集成解决方案 (Enterprise beta)

如果要将在 IBM Integration Bus 或 App Connect Enterprise 中开发的集成解决方案部署到云，而无需获取或维护 IT 基础架构，您可以导入包含构成集成解决方案的所有工件的 BAR 文件，然后在 App Connect 中的集成服务器中运行该文件的内容。要将 BAR 文件上传到 App Connect，您必须在内部部署安装 IBM Integration Bus V10.0.0.4 或更高版本，或者安装 App Connect Enterprise。

要在 App Connect 中运行 Integration Bus 或 App Connect Enterprise 解决方案，请完成以下步骤。
1. 在 {{site.data.keyword.appconserviceshort}} 仪表板上，单击**新建** > **导入 BAR 文件**。
1. 选择要导入的 BAR 文件，根据需要编辑名称，然后单击**导入**。
    如果看到认证错误，请检查 BAR 文件是否有效（请参阅 [What makes a BAR file valid in App Connect? ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/what-makes-a-bar-file-valid-for-app-connect-app-connect-enterprise-beta)）。
    这将创建集成服务器，并会向仪表板添加磁贴以表示该集成服务器。集成服务器准备好进行配置并启动时，状态将从“正在准备”更改为“已停止”。 
1. 单击磁贴以打开集成服务器。
1. 配置集成服务器：
    * 添加或编辑集成解决方案的描述。
    * 配置 HTTPS 基本认证（请参阅 [Configuring HTTPS basic authentication ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/configuring-https-basic-authentication-app-connect-enterprise-beta)）。
    * 连接策略，以便可以连接到内部部署系统（请参阅 [Configuring secure connectivity between integration servers on App Connect and on-premises systems ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/configuring-secure-connectivity-between-integration-servers-on-app-connect-and-on-premises-systems-app-connect-enterprise-beta)）。
1. 可选：要在内部部署环境和 App Connect 之间拆分消息流处理，请通过打开汉堡菜单 ![“汉堡菜单”图标](/images/HamburgerMenuSm.jpg)，展开**管理**，然后选择**可调用的流**来配置可调用的流（请参阅 [Sharing message flow processing between App Connect and Integration Bus ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/sharing-message-flow-processing-between-app-connect-and-integration-bus-app-connect-enterprise-beta)）。
1. 完成配置后，返回到 App Connect 仪表板，通过打开相应磁贴菜单并单击**启动**以启动集成服务器。

集成服务器在运行时，可以通过打开该集成服务器，并单击**下载日志**或**查看日志**来查看和下载日志。要查看日志，必须将“日志记录”策略连接到集成服务器（请参阅 [Viewing logs for your integration servers ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/viewing-logs-for-your-integration-servers-in-app-connect-enterprise-beta)）。

有关更详细信息，请参阅 [Running your Integration Bus solutions in App Connect ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan)。
