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


# Troubleshooting IBM App Connect
{: #troubleshooting}

To troubleshoot problems with {{site.data.keyword.appconservicefull}} flows and integration servers, you can view logs in Kibana. If you have questions or problems when you're using {{site.data.keyword.appconserviceshort}}, get help by searching for information or by asking questions through a forum. When you use the forums to ask a question, tag your question so that it is seen by the {{site.data.keyword.Bluemix}} and {{site.data.keyword.appconserviceshort}} development teams.

-   Look at the tile for a running flow on the {{site.data.keyword.appconserviceshort}} dashboard. If there’s a green tick, the flow is running successfully; click the tick to see when the flow was last triggered.

    ![Screen capture showing that a flow is running successfully](/images/SuccessfulFlow.jpg)

    If there’s a red exclamation point, there’s a problem; click the exclamation point to find out what the problem is. ![Screen capture showing that a flow has a problem](/images/ErroredFlow.jpg)

-   Check the {{site.data.keyword.appconserviceshort}} status page to see whether any issues are reported or maintenance is planned: [{{site.data.keyword.appconserviceshort}} status page ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/integration/docs/app-connect/app-connect-status/)
-   To view log information for your flows, click **Logs** in the {{site.data.keyword.appconserviceshort}} hamburger menu. Error and information messages for your flows are shown by default in Kibana, where you can view data for a specific time range, or use filters to show certain types of information. To view debugging information for your flows, open the menu on a flow tile on the {{site.data.keyword.appconserviceshort}} dashboard, then select **Enable debug logging**.  You then need to restart your flow for debug logging to start.  When you enable debug logging, debug log entries, potentially including payload data, are visible to IBM operators. To learn more about debug logging, see [Debugging your message flows in {{site.data.keyword.appconserviceshort}} ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/debugging-message-flows-ibm-app-connect/).  To learn more about Kibana, see [Kibana documentation ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://www.elastic.co/guide/en/kibana/4.0/discover.html).
-   To view log information for your integration servers, open an integration server and click **Download logs** or **View logs**.  To view logs for an integration server in Kibana, you have to attach a Logging policy to that integration server (see [Viewing logs for your integration servers ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan/viewing-logs-for-your-integration-servers-in-app-connect-enterprise-beta)).
-   Find answers to common questions about {{site.data.keyword.appconserviceshort}} in [Frequently asked questions about {{site.data.keyword.appconserviceshort}} ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/integration/docs/app-connect/faq/).
-   Follow step-by-step instructions about how to connect your applications in [Tutorials for {{site.data.keyword.appconserviceshort}} ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/).
-   If you have technical questions about developing or deploying an application with {{site.data.keyword.appconserviceshort}}, post your question on [Stack Overflow ![External link icon](../../icons/launch-glyph.svg "External link icon")](http://stackoverflow.com/search?q=app-connect+ibm-bluemix) and tag your question with "ibm-bluemix" and "app-connect" (with a hyphen).
-   For questions about the service and getting started instructions, use the [IBM dW Answers ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/answers/topics/app_connect/?smartspace=bluemix) forum. Include the tags "bluemix" and "app_connect" (with an underscore).

    For more information about using {{site.data.keyword.Bluemix}} support mechanisms, see [Getting help ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://console.ng.bluemix.net/docs/support/index.html#getting-help).


