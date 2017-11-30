---

copyright:
  years: 2017
lastupdated: "2017-09-08"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip} 
{:download: .download}


# Troubleshooting IBM App Connect
{: #troubleshooting}

To troubleshoot problems with {{site.data.keyword.appconservicefull}} flows and integration servers, you can view logs in Kibana. If you have questions or problems when you're using {{site.data.keyword.appconserviceshort}}, get help by searching for information or by asking questions through a forum. When you use the forums to ask a question, tag your question so that it is seen by the {{site.data.keyword.Bluemix}} and {{site.data.keyword.appconserviceshort}} development teams.

-   Look at the tile for a running flow on the {{site.data.keyword.appconserviceshort}} dashboard. If there’s a green tick, the flow has run successfully; click the tick to see when the flow was last triggered.

    ![Screenshot showing that a flow has run successfully](/images/SuccessfulFlow.jpg)

    If there’s a red exclamation point, there’s a problem; click the exclamation point to find out what’s gone wrong. ![Screenshot showing that a flow has a problem](/images/ErroredFlow.jpg)

-   Check the {{site.data.keyword.appconserviceshort}} status page to see if there are any current known issues or any maintenance is planned: [{{site.data.keyword.appconserviceshort}} status page ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/integration/docs/app-connect/app-connect-status/)
-   To view log information for your flows, click **Logs** in the {{site.data.keyword.appconserviceshort}} hamburger menu. Information about your flows is shown in Kibana, where you can view data for a specific time range, or use filters to show certain types of information. To learn more about Kibana, see [Kibana documentation ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://www.elastic.co/guide/en/kibana/4.0/discover.html).
-   To view log information for your integration servers (if you have the {{site.data.keyword.appconservicefull}} Enterprise plan), open an integration server and click **Download logs** or **View logs**.  To view logs for an integration server in Kibana, you have to attach a Logging policy to that integration server (see [Viewing logs for your integration servers ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/viewing-logs-for-your-integration-servers-in-app-connect-enterprise-beta)).
-   Find answers to common questions about {{site.data.keyword.appconserviceshort}} in [Frequently asked questions about {{site.data.keyword.appconserviceshort}} ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/integration/docs/app-connect/faq/).
-   Follow step-by-step instructions about how to connect your applications in [Tutorials for {{site.data.keyword.appconserviceshort}} ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/).
-   If you have technical questions about developing or deploying an application with {{site.data.keyword.appconserviceshort}}, post your question on [Stack Overflow ![External link icon](../../icons/launch-glyph.svg "External link icon")](http://stackoverflow.com/search?q=app-connect+ibm-bluemix) and tag your question with "ibm-bluemix" and "app-connect" (with a hyphen).
-   For questions about the service and getting started instructions, use the [IBM developerWorks&reg; dW Answers ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/answers/topics/app_connect/?smartspace=bluemix) forum. Include the tags "bluemix" and "app_connect" (with an underscore).

    For more information about using {{site.data.keyword.Bluemix}} support mechanisms, see [Getting help ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://console.ng.bluemix.net/docs/support/index.html#getting-help).


