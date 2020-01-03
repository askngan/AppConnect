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


# Troubleshooting IBM App Connect
{: #troubleshooting}

To troubleshoot problems with {{site.data.keyword.appconservicefull}} flows and integration servers, you can view the information in the logs. If you have questions or problems when you're using {{site.data.keyword.appconserviceshort}}, get help by searching for information or by asking questions through a forum. When you use the forums to ask a question, tag your question so that it is seen by the {{site.data.keyword.Bluemix}} and {{site.data.keyword.appconserviceshort}} development teams.

-   Look at the tile for a running flow on the {{site.data.keyword.appconserviceshort}} dashboard. If there’s a green tick, the flow is running successfully; click the tick to see when the flow was last triggered.

    ![Screen capture that shows that a flow is running successfully](/images/SuccessfulFlow.jpg)

    If there’s a red exclamation point, there’s a problem; click the exclamation point to find out what the problem is. ![Screen capture that shows that a flow has a problem](/images/ErroredFlow.jpg)

-   Check the {{site.data.keyword.appconserviceshort}} status page to see whether any issues are reported or maintenance is planned: [{{site.data.keyword.appconserviceshort}} status page ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/integration/docs/app-connect/app-connect-status/)
-   To view log information for your flows, click **Manage > Logs** in the {{site.data.keyword.appconserviceshort}} menu. You can view data for a specific time range, or use filters to show certain types of information. To view debugging information for your flows, open the menu on a flow tile on the {{site.data.keyword.appconserviceshort}} dashboard, then select **Enable debug logging**.  You then need to restart your flow for debug logging to start.  When you enable debug logging, debug log entries, potentially including payload data, are visible to IBM operators. To learn more about debug logging, see [Debugging your message flows in {{site.data.keyword.appconserviceshort}} ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/debugging-message-flows-ibm-app-connect/).  
-   To view log information for your integration servers, open an integration server and click **View logs**.  
-   To monitor and manage {{site.data.keyword.appconserviceshort}} logs in IBM Log Analysis with LogDNA, provision an instance of the IBM Log Analysis with LogDNA service under the same account and region as your {{site.data.keyword.appconserviceshort}} instance. Then configure IBM Log Analysis with LogDNA to receive platform services logs. You can then use IBM Log Analysis with LogDNA to view messages from your {{site.data.keyword.appconserviceshort}} flows and App Connect Enterprise integration servers that are running in the {{site.data.keyword.appconserviceshort}} instance. To learn more, see [Monitoring and managing {{site.data.keyword.appconserviceshort}} logs in IBM Log Analysis with LogDNA ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/integration/docs/app-connect/troubleshooting/monitoring-and-managing-app-connect-logs-in-logdna/).
-   Find answers to common questions about {{site.data.keyword.appconserviceshort}} in [Frequently asked questions about {{site.data.keyword.appconserviceshort}} ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/integration/docs/app-connect/faq/).
-   Follow step-by-step instructions about how to connect your applications in [Tutorials for {{site.data.keyword.appconserviceshort}} ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/).
-   For questions about the service and getting started instructions, use the [IBM dW Answers ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/answers/topics/app_connect) forum. Include the tags "ibm_cloud" and "app_connect" (with an underscore).

    For more information about using {{site.data.keyword.Bluemix}} support mechanisms, see [Support ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://cloud.ibm.com/unifiedsupport/supportcenter).

## Reporting a problem to the IBM App Connect team
{: #reporting}

If you followed the troubleshooting advice and you're still experiencing a problem, you can get help from the   {{site.data.keyword.appconserviceshort}} team.  From the {{site.data.keyword.appconserviceshort}} menu, click **Contact us**, then **Get support**.  Sign in with your IBM ID, click **Create a case**, and provide as much of the following information as you can. (You can also click **Support** in the {{site.data.keyword.Bluemix}} console.) 

* The {{site.data.keyword.Bluemix}} region where your instance of {{site.data.keyword.appconserviceshort}} is provisioned. (For example, Dallas or London.)
* The Instance ID of the {{site.data.keyword.appconserviceshort}} service that you're using. (You can find this ID by looking at the account information under the {{site.data.keyword.appconserviceshort}} Instance Identifier.)
* The problem that you're experiencing. (For example, whether the problem is with a specific application or function.)
* The batch ID if the problem is related to batch processing. (If errors occur in a batch process, and you defined an ID for each record in the batch, your defined ID is in the "batch-record-id_str" column of the log. For more information, see [How to use batch processing in {{site.data.keyword.appconserviceshort}} ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/integration/docs/app-connect/toolbox-utilities/how-to-use-batch-processing-in-ibm-app-connect/).)
* The date and time (including time zone) when the problem first occurred, and the length of time that the flow was running before the problem occurred.
* Whether the problem is still occurring, and if you can replicate it.
* If applicable, the browser type and version that you're using. ({{site.data.keyword.appconserviceshort}} supports the latest browser versions only.)
* Any log entries that describe the problem.
* The impact that the problem is having on your business.
