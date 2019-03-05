---

copyright:
  years: 2017
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

-   在 {{site.data.keyword.appconserviceshort}} 仪表板上查看正在运行的流的磁贴。如果有绿色勾号，说明流已成功运行；单击勾号可查看上次触发流的时间。

    ![显示流已成功运行的屏幕快照](/images/SuccessfulFlow.jpg)

    如果有红色惊叹号，说明发生了问题；单击惊叹号可了解发生了什么错误。
![显示流有问题的屏幕快照](/images/ErroredFlow.jpg)

-   查看 {{site.data.keyword.appconserviceshort}} 状态页面，以确定是否有任何当前已知的问题或是否计划了任何维护：[{{site.data.keyword.appconserviceshort}} 状态页面 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://developer.ibm.com/integration/docs/app-connect/app-connect-status/)
-   要查看流的日志信息，请单击 {{site.data.keyword.appconserviceshort}} 汉堡菜单中的**日志**。缺省情况下，Kibana 中会显示流的错误和参考消息；在 Kibana 中可以查看特定时间范围的数据，或使用过滤器来显示某些类型的信息。要查看流的调试信息，请在 {{site.data.keyword.appconserviceshort}} 仪表板上打开流磁贴上的菜单，并选择**启用调试日志记录**。然后，您需要重新启动流，才可启动调试日志记录。请注意，启用调试日志记录后，IBM 运营商可查看调试日志条目（可能包含有效内容数据）。要了解有关调试日志记录的更多信息，请参阅 [Debugging your message flows in {{site.data.keyword.appconserviceshort}}](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/debugging-message-flows-ibm-app-connect/)。要了解有关 Kibana 的更多信息，请参阅 [Kibana 文档 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://www.elastic.co/guide/en/kibana/4.0/discover.html)。
-   要查看集成服务器的日志信息，请打开集成服务器，然后单击**下载日志**或**查看日志**。要在 Kibana 中查看集成服务器的日志，必须将“日志记录”策略连接到该集成服务器（请参阅 [Viewing logs for your integration servers ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/viewing-logs-for-your-integration-servers-in-app-connect-enterprise-beta)）。
-   在 [Frequently asked questions about {{site.data.keyword.appconserviceshort}} ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://developer.ibm.com/integration/docs/app-connect/faq/) 中查找有关 {{site.data.keyword.appconserviceshort}} 的常见问题的答案。
-   按照 [Tutorials for {{site.data.keyword.appconserviceshort}} ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/) 中有关如何连接应用程序的逐步指示信息进行操作。
-   如果有关于使用 {{site.data.keyword.appconserviceshort}} 开发或部署应用程序的技术问题，请在 [Stack Overflow ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](http://stackoverflow.com/search?q=app-connect+ibm-bluemix) 上发帖提问，并使用“ibm-bluemix”和“app-connect”（含连字符）标记您的问题。
-   有关服务和入门指示信息的问题，请使用 [IBM developerWorks&reg; dW Answers ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://developer.ibm.com/answers/topics/app_connect/?smartspace=bluemix) 论坛。请包含“bluemix”和“app_connect”（含下划线）标记。

    有关使用 {{site.data.keyword.Bluemix}} 支持机制的更多信息，请参阅[获取帮助 ![外部链接图标](../../icons/launch-glyph.svg "外部链接图标")](https://console.ng.bluemix.net/docs/support/index.html#getting-help)。


