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


# 对 IBM App Connect 进行故障诊断
{: #troubleshooting}

要对使用 {{site.data.keyword.appconservicefull}} 流和集成服务器时遇到的问题进行故障诊断，您可以在 Kibana 中查看日志。如果在使用 {{site.data.keyword.appconserviceshort}} 时遇到任何问题或有任何疑问，请通过搜索信息或通过论坛提问来获取帮助。在使用论坛提问时，请标记您的问题，以便 {{site.data.keyword.Bluemix}} 和 {{site.data.keyword.appconserviceshort}} 开发团队能看到您的问题。

-   在 {{site.data.keyword.appconserviceshort}} 仪表板上查看正在运行的流的磁贴。如果有绿色勾号，说明流正在成功运行；单击勾号可查看上次触发流的时间。

    ![显示流正在成功运行的截屏](/images/SuccessfulFlow.jpg)

    如果有红色惊叹号，说明发生了问题；单击惊叹号可了解发生了什么问题。
![显示流有问题的截屏](/images/ErroredFlow.jpg)

-   查看 {{site.data.keyword.appconserviceshort}} 状态页面，以确定是否报告了任何问题或是否计划了维护：[{{site.data.keyword.appconserviceshort}} 状态页面 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://developer.ibm.com/integration/docs/app-connect/app-connect-status/)
-   要查看流的日志信息，请单击 {{site.data.keyword.appconserviceshort}} 菜单中的**日志**。缺省情况下，Kibana 中会显示流的错误和参考消息；在 Kibana 中可以查看特定时间范围的数据，或使用过滤器来显示某些类型的信息。要查看流的调试信息，请在 {{site.data.keyword.appconserviceshort}} 仪表板上打开流磁贴上的菜单，并选择**启用调试日志记录**。然后，您需要重新启动流，才可启动调试日志记录。启用调试日志记录后，IBM 运营商可查看调试日志条目（可能包含有效内容数据）。要了解有关调试日志记录的更多信息，请参阅 [Debugging your message flows in {{site.data.keyword.appconserviceshort}} ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/debugging-message-flows-ibm-app-connect/)。要了解有关 Kibana 的更多信息，请参阅 [Kibana 文档 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://www.elastic.co/guide/en/kibana/4.0/discover.html)。
-   要查看集成服务器的日志信息，请打开集成服务器，然后单击**下载日志**或**查看日志**。要在 Kibana 中查看集成服务器的日志，必须将“日志记录”策略连接到该集成服务器（请参阅 [Viewing logs for your integration servers ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/viewing-logs-for-your-integration-servers-in-app-connect-enterprise-beta)）。
-   在 [Frequently asked questions about {{site.data.keyword.appconserviceshort}} ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://developer.ibm.com/integration/docs/app-connect/faq/) 中查找有关 {{site.data.keyword.appconserviceshort}} 的常见问题的答案。
-   按照 [Tutorials for {{site.data.keyword.appconserviceshort}} ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/) 中有关如何连接应用程序的逐步指示信息进行操作。
-   有关服务和入门指示信息的问题，请使用 [IBM dW Answers ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://developer.ibm.com/answers/topics/app_connect) 论坛。请包含“ibm_cloud”和“app_connect”（含下划线）标记。

    有关使用 {{site.data.keyword.Bluemix}} 支持机制的更多信息，请参阅[支持 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://cloud.ibm.com/unifiedsupport/supportcenter)。

## 向 IBM App Connect 团队报告问题
{: #reporting}

如果您遵循了故障诊断建议，但仍然遇到问题，那么可以从 {{site.data.keyword.appconserviceshort}} 团队那里获得帮助。在 {{site.data.keyword.appconserviceshort}} 菜单中，单击**联系我们**，然后单击**获取支持**。使用您的 IBM 标识登录，单击**创建案例**，并尽可能多地提供以下信息。（您还可以单击 {{site.data.keyword.Bluemix}} 控制台中的**支持**。） 

* 在其中供应 {{site.data.keyword.appconserviceshort}} 实例的 {{site.data.keyword.Bluemix}} 区域。（例如，达拉斯或伦敦。）
* 使用的 {{site.data.keyword.appconserviceshort}} 服务的实例标识。（您可以通过查看 {{site.data.keyword.appconserviceshort}}“实例标识”下的帐户信息来找到此标识。）
* 遇到的问题。（例如，问题是否与特定应用程序或函数相关。）
* 批次标识（如果问题与批处理相关）。（如果批处理过程中发生错误，并且已为批处理过程中的每个记录定义了标识，那么可以在 Kibana 日志的“batch-record-id_str”列中找到定义的标识；请参阅 [How to use batch processing in {{site.data.keyword.appconserviceshort}} ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://developer.ibm.com/integration/docs/app-connect/toolbox-utilities/how-to-use-batch-processing-in-ibm-app-connect/)。）
* 问题首次发生时的日期和时间（包括时区），以及流在问题发生之前运行的时间长度。
* 问题是否仍然发生，以及是否可以重现。
* 使用的浏览器类型和版本（如果适用）。（我们仅支持最新的浏览器版本。）
* 描述问题的任何日志条目。
* 问题对您的业务产生的影响。
