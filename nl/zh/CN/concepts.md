---

copyright:
  years: 2017
lastupdated: "2019-02-20"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip} 
{:download: .download}


# IBM App Connect 概念
{: #concepts}

{{site.data.keyword.appconservicefull}} 是一种业务友好型工具，可用于集成基于云的应用程序或内部部署应用程序，以自动执行繁琐、重复的任务。

下面，我们将说明 {{site.data.keyword.appconserviceshort}} 的功能和术语：

-   [流](#flows)
-   [应用程序](#apps)
-   [操作](#actions)
-   [数据映射](#transforms)
-   [BAR 文件和集成服务器](#barfiles)

## 流
{: #flows}

在 {{site.data.keyword.appconserviceshort}} 中可以创建两种类型的流：事件驱动的流和 API 流。

在事件驱动的流中，您可确定可能在第一个应用程序（源应用程序）中发生的事件，以及可在一个或多个目标应用程序中执行的操作。流用于将事件链接到操作，以便每当源应用程序中发生事件时，都会在目标应用程序中自动触发相应操作。每个成功完成的操作都会计入每月配额。创建流时，可添加应用程序，并选择操作。然后，映射要在应用程序之间传输的数据。

例如，您可能会创建一个流，以便每当有人通过 Eventbrite 注册为新的出席者时（事件），{{site.data.keyword.appconserviceshort}} 都会自动从 Salesforce 中检索该出席者的详细信息，并在 Asana 中创建新任务（操作）。

![一个多节点流，包含源应用程序和两个目标应用程序](images/multi_node_flow2.jpg)

有关更多信息，请参阅 [Creating an event-driven flow ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/creating-event-driven-flow/)。

API 流包含请求、一个或多个目标应用程序操作以及响应。请求使用您定义的模型来请求在应用程序中创建、替换或检索数据对象。提交请求时，每个目标应用程序都会执行其操作，然后流会返回响应，响应确认操作成功或返回请求的数据。

![用于在 Salesforce 中创建产品的 API 流](images/APIFlow2.jpg)

有关更多信息，请参阅 [Creating flows for an API ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/creating-flows-api/)。

除了向流添加应用程序外，还可以在**逻辑**选项卡中添加节点，以允许您配置数据处理方式。例如，使用 If 节点添加一些条件处理，即根据您收到的数据执行不同的操作（请参阅 [Adding conditional logic to a flow ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/adding-conditional-logic-flow/)）。如果要对“检索”操作返回的每条记录执行操作，请使用 For each 节点（请参阅 [Retrieving items from your applications ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/using-ibm-app-connect-retrieve-items-applications/)）。

如果您是 IBM Integration Bus 或 App Connect Enterprise 开发者，那么还可以通过在 Integration Toolkit 中开发消息流，并将其打包为 BAR 文件来创建复杂的集成解决方案。

流和集成服务器在 App Connect 仪表板上用磁贴表示。磁贴会显示有关流、API 或集成服务器的摘要信息，例如流是正在运行还是已停止，以及流是已成功运行还是生成了错误。可以单击勾号和惊叹号图标来查看流上次成功运行的时间，或查看引发的错误。单击三个点 ![3 个垂直点的图标，可打开菜单以启动、停止、编辑或删除流](images/Menu.jpg) 可打开菜单，通过该菜单，您可以启动、停止、编辑或删除资源。必须先停止流，然后才能对其进行编辑。

![显示仪表板中表示事件驱动的流、API 流和集成服务器的磁贴的屏幕快照](images/Dashboard.jpg)

## 应用程序
{: #apps}

创建事件驱动的流或 API 流时，_应用程序_是要连接的基于云的软件应用程序。您可以在**应用程序**页面上查看可以与 {{site.data.keyword.appconserviceshort}} 连接的应用程序的列表。单击应用程序可了解有关该应用程序的更多信息，查看支持的事件和操作，以及连接到您自己的帐户。在“应用程序”页面上，可以针对每个应用程序连接多个帐户，并可在帐户之间进行切换。连接到帐户后，还可以在此页面上更新或除去帐户。

![“应用程序”页面上其中一个应用程序的屏幕快照](images/Magento2.jpg)

您不必在“应用程序”页面上连接到应用程序；还可以在流编辑器中将应用程序添加到流时进行连接。许多应用程序只需要用户名和密码，但有些应用程序需要更多信息。您可以在 [How-to guides for apps ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://developer.ibm.com/integration/docs/app-connect/how-to-guides-for-apps/) 中了解如何查找这些信息。

如果要使用 {{site.data.keyword.appconservicefull}} 在云中运行 Integration Bus 或 App Connect Enterprise 解决方案，那么_应用程序_是保存消息流、库以及解决方案所需的其他资源的容器。 

## 操作
{: #actions}

您可以向流添加多种类型的操作。常见操作是“创建”、“检索”和“更新或创建”，但某些应用程序具有特定操作。例如，Equals 3 Lucy 应用程序有一个名为“Ask Lucy”的操作，Watson Personality Insights 应用程序有一个名为“Analyze personality”的操作。在 {{site.data.keyword.appconserviceshort}} 中，通过在“应用程序”页面顶部的搜索字段中输入操作类型，可以查看应用程序支持的操作的列表：

![显示应用程序支持的“检索”操作的屏幕快照](images/RetrieveApps2.jpg)

**创建**

顾名思义，“创建”操作用于在应用程序中创建对象或记录。例如，如果有人报名参加您的活动或提交了填写的表单，那么您可能需要在 CRM 或市场营销应用程序中为此人创建记录。或者，如果有人在您的帮助台应用程序中开具了凭单，那么您可能需要创建电子邮件或即时消息，以确保有人立即对此进行处理。如果要创建的对象有可能已存在，那么可以改为使用*更新或创建*操作。

对于某些应用程序，在向流添加“创建”操作时，可能必须提供一些额外信息，以便流了解创建对象的位置。例如，如果使用的是 Asana 或 Trello 等项目管理应用程序，那么在创建任务或卡时，需要指定要添加该任务或卡的项目或仪表板。

**更新或创建**

“更新或创建”操作用于更改目标应用程序中的现有记录（如果存在），但如果记录尚不存在，那么会创建记录。这也称为增删改（更新或插入）操作。

例如，假设某人提交了一份包含地址更改的 Wufoo 表单。如果该联系人已在 CRM 系统中，那么您需要更新其地址；但如果 CRM 系统中尚没有该联系人，那么需要添加此人。与“检索”操作类似，选择用于更新某个应用程序中数据的操作时，可以添加一个或多个条件以确保更新的是正确的信息。

如果目标系统中有多条记录符合条件，那么您会在仪表板上看到有关流的错误，并且流不会更新或创建任何记录。例如，您可能有多个具有相同名字和姓氏的联系人。为此，您可以尝试使用唯一数据（例如，联系人的电子邮件地址）来匹配联系人。

在“更新或创建”操作的响应中，可能会看到的状态码如下：

-   200: 记录已更新
-   201: 记录已创建

您可以在流中的后面部分使用这些响应代码。或许您希望根据记录是已更新还是已创建而执行不同的操作。有关基于响应代码来定义操作的示例，请参阅 [Updating or creating a contact in Salesforce and updating Asana when a Wufoo form is submitted](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/creating-event-driven-flow-updates-creates-contact-salesforce-updates-asana-whenever-receive-form-wufoo/) 教程。

**检索**

“检索”操作用于从应用程序中获取信息，以便您可以在其他应用程序中使用这些信息。

向流添加用于检索对象的操作时，可以定义一个或多个条件以确保检索的是正确的项。或者，如果您只想检索特定类型的所有项，那么可以删除条件。您还可以定义要检索的项数，以及 {{site.data.keyword.appconserviceshort}} 查找的数量多于或少于该数量时要执行的操作。

可以通过两种方式处理检索到的项：

-   可以在“检索”操作之后添加“For each”节点，以针对检索到的每项执行操作。
-   可以在“检索”操作之后添加另一个操作，以处理检索到的项的列表。这是单个操作，与返回的项数无关 - 例如，创建列出所有检索到的项的电子邮件。

您还可以根据在“检索”操作的响应中获得的状态码来决定要执行的操作。可以使用“If”节点针对不同的状态码执行不同的操作。在“检索”操作的响应中，可能会看到的状态码如下：

-   204: 找不到记录
-   200: 应用程序中的所有记录都符合条件
-   206: 检索到指定的最大记录数，但应用程序中存在更多匹配的记录

有关更多信息，请参阅 [Retrieving items from your applications](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/using-ibm-app-connect-retrieve-items-applications/)。

## 数据映射
{: #transforms}

已创建流，添加了应用程序并选择了相应的操作后，您需要指定要在应用程序之间传输的信息。在流编辑器中，向流添加操作时，您将看到该应用程序的可用字段列表，可以使用源应用程序中的数据或流中的先前操作来填充这些字段。

某些字段是必填的，会标有星号。例如，在 Salesforce 中创建潜在用户时，必须指定姓氏：

![显示“姓氏”字段是必填项的屏幕快照](images/LastName.jpg)

单击其中一个字段时，将显示若干图标：**插入参考** ![“插入参考”图标](images/InsertRef.jpg) 和**应用函数** ![“应用函数”图标](images/Functions.jpg)。如果单击**插入参考**，您将看到可以在流中先前应用程序的该字段中放入的可用数据。以下示例显示了可以从 Wufoo 源应用程序中选择字段，也可以从流中的先前 Salesforce 操作中选择字段。此外，还可以使用 Salesforce“更新或创建”操作中的状态码。

![显示用于数据映射的可用输入的屏幕快照](images/Inputs.jpg)

在以下示例中，在 Wufoo 中收到新填写的表单将触发流。我们需要在 Salesforce 中为提交表单的人员创建联系人。因此，将 Salesforce“创建联系人”操作添加到流时，可从 Wufoo 表单中复制联系人的详细信息。在此可以看到，对于 Salesforce 联系人的姓氏，选择了 Wufoo 表单提交者的姓氏。您可以看到映射的字段是来自 Wufoo，这可根据颜色得知：

![显示 Wufoo“姓氏”字段映射到 Salesforce“姓氏”字段的屏幕快照](images/Mapping.jpg)

在以下示例中，在流中的 Salesforce“更新或创建联系人”操作之后添加了 Slack“创建消息”操作。我们只想在 Slack 上发布一条消息，表明对于该 Salesforce 操作收到的响应代码：

![对应到某个响应代码的 Slack“创建消息”操作的屏幕快照](images/SlackSC.jpg)

您可以看到，在 Slack“创建消息”操作的**文本**字段中，我们已输入了一条消息，然后在 Salesforce“更新或创建联系人”操作的状态码中对其进行了映射。

下面是以不同方式映射响应代码的另一个示例。这次，是在 Salesforce“更新或创建联系人”操作之后添加了“If”节点，因为我们希望根据是更新了现有 Salesforce 联系人还是创建了新联系人来执行不同的操作。在本例中，响应代码“200”表示更新了联系人。因此，“If”节点的此分支将包含特定于已更新记录的操作。

![显示 If 节点中使用的响应代码的屏幕快照](images/IfSC.jpg)

**应用函数**图标 ![“应用函数”图标](Functions.jpg) 显示转换函数的列表，可以使用这些函数来定制通过流传递的数据。这些函数既可以像将特定字段转换为大写或小写一样简单，也可以稍微复杂一些，例如查找并替换数据中的特定模式。此外，这些函数也可以像构成正则表达式一样有强大的功能。您可以从列表中选择所需的函数，也可以自行输入函数。函数的语法是 JSONata，这是一种轻量级查询和转换语言。有关更多信息，请参阅 [http://jsonata.org](http://jsonata.org)。


## BAR 文件和集成服务器
{: #barfiles}

在 IBM Integration Bus 或 App Connect Enterprise 中，BAR 文件是可向其添加多个可部署资源的压缩文件。在 Integration Bus 或 App Connect Enterprise 中开发集成解决方案时，可将消息流以及这些消息流使用的所有资源打包为 BAR 文件，然后将 BAR 文件部署到集成服务器。该服务器可以为内部部署，也可以位于 {{site.data.keyword.appconserviceshort}} 中。您可以在 App Connect 中运行 Integration Bus 或 App Connect Enterprise 解决方案，而无需获取和维护 IT 基础架构。将 BAR 文件上传到 App Connect 时，会创建一个集成服务器来运行 BAR 文件的内容。您可以配置基于云的资源和内部部署资源之间的基本认证和安全连接（请参阅 [Running your Integration Bus solutions in App Connect ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan)）。  
