---

copyright:
  years: 2017, 2021
lastupdated: "2021-04-01"

subcollection: AppConnect

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

To troubleshoot problems with {{site.data.keyword.appconservicefull}} flows and integration servers, you can view the information in the logs. If you have questions or problems when you're using {{site.data.keyword.appconnect_notm}}, get help by searching for information or by asking questions through a forum. When you use the forums to ask a question, tag your question so that it is seen by the {{site.data.keyword.Bluemix}} and {{site.data.keyword.appconnect_notm}} development teams.

-   Look at the tile for a running flow on the {{site.data.keyword.appconnect_notm}} dashboard. If there’s a green tick, the flow is running successfully; click the tick to see when the flow was last triggered.

    ![Screen capture that shows that a flow is running successfully](/images/SuccessfulFlow.jpg)

    If there’s a red exclamation point, there’s a problem; click the exclamation point to find out what the problem is. ![Screen capture that shows that a flow has a problem](/images/ErroredFlow.jpg)

-   Check the {{site.data.keyword.appconnect_notm}} status page to see whether any issues are reported or maintenance is planned: [{{site.data.keyword.appconnect_notm}} status page ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://cloud.ibm.com/status?component=appconnect&selected=status)
-   To view log information for your flows, click the **Logs** icon ![Logs icon](/images/LogsIcon.jpg). You can view data for a specific time range, or use filters to show certain types of information. To view debugging information for your flows, open the menu on a flow tile on the {{site.data.keyword.appconnect_notm}} dashboard, then select **Enable debug logging**.  You then need to restart your flow for debug logging to start.  When you enable debug logging, debug log entries, potentially including payload data, are visible to IBM operators. To learn more about debug logging, see [Viewing {{site.data.keyword.appconnect_notm}} logs in the log viewer ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://www.ibm.com/support/knowledgecenter/en/SS6KM6/com.ibm.appconnect.doc/troubleshooting/viewing-app-connect-logs-in-the-log-viewer.html).  
-   To view log information for your integration servers, open an integration server and click **View logs**.  
-   To monitor and manage {{site.data.keyword.appconnect_notm}} logs in IBM Log Analysis, provision an instance of the IBM Log Analysis service under the same account and region as your {{site.data.keyword.appconnect_notm}} instance. Then configure IBM Log Analysis to receive platform services logs. You can then use IBM Log Analysis to view messages from your {{site.data.keyword.appconnect_notm}} flows and App Connect Enterprise integration servers that are running in the {{site.data.keyword.appconnect_notm}} instance. To learn more, see [Monitoring and managing {{site.data.keyword.appconnect_notm}} logs in IBM Log Analysis ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://www.ibm.com/support/knowledgecenter/en/SS6KM6/com.ibm.appconnect.doc/troubleshooting/monitoring-and-managing-app-connect-logs-in-logdna.html).
-   Find answers to common questions about {{site.data.keyword.appconnect_notm}} in [Frequently asked questions about {{site.data.keyword.appconnect_notm}} ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://www.ibm.com/support/knowledgecenter/en/SS6KM6/com.ibm.appconnect.cloud.doc/faq.html).
-   Follow step-by-step instructions about how to connect your applications in [Tutorials for {{site.data.keyword.appconnect_notm}} ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://www.ibm.com/support/knowledgecenter/en/SS6KM6/com.ibm.appconnect.dev.doc/tutorials/index.html).
-   For questions about the service and getting started instructions, use the [{{site.data.keyword.appconnect_notm}} Discussion forum ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://community.ibm.com/community/user/imwuc/communities/community-home/digestviewer?communitykey=77544459-9fda-40da-ae0b-fc8c76f0ce18&tab=digestviewer). Include the tags "ibm_cloud" and "app_connect" (with an underscore).

    For more information about using {{site.data.keyword.Bluemix}} support mechanisms, see [Support ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://cloud.ibm.com/unifiedsupport/supportcenter).

## Reporting a problem to the IBM App Connect team
{: #reporting}

If you followed the troubleshooting advice and you're still experiencing a problem, you can get help from the   {{site.data.keyword.appconnect_notm}} team.  From the {{site.data.keyword.appconnect_notm}} menu, click **Contact**, then **Get support**.  Sign in with your IBM ID, click **Create a case**, and click the **App Connect** tile.  Then provide as much of the following information as you can. (You can also click **Support** in the {{site.data.keyword.Bluemix}} console.)

* The {{site.data.keyword.Bluemix}} region where your instance of {{site.data.keyword.appconnect_notm}} is provisioned. (For example, Dallas or London.)
* The Instance ID of the {{site.data.keyword.appconnect_notm}} service that you're using. (You can find this ID by looking at the account information under the {{site.data.keyword.appconnect_notm}} Instance Identifier.)
* The URL that you use to access your {{site.data.keyword.appconnect_notm}} instance.
* The problem that you're experiencing. (For example, whether the problem is with a specific application or function.)
* The batch ID if the problem is related to batch processing. (If errors occur in a batch process, and you defined an ID for each record in the batch, your defined ID is in the "batch-record-id_str" column of the log. For more information, see [How to use batch processing in {{site.data.keyword.appconnect_notm}} ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://www.ibm.com/support/knowledgecenter/en/SS6KM6/com.ibm.appconnect.dev.doc/toolbox/batch-processing.html).)
* The date and time (including time zone) when the problem first occurred, and the length of time that the flow was running before the problem occurred.
* Whether the problem is still occurring, and if you can replicate it.
* If applicable, the browser type and version that you're using. ({{site.data.keyword.appconnect_notm}} supports the latest browser versions only.)
* Any log entries that describe the problem.
* The impact that the problem is having on your business.

If you have an {{site.data.keyword.Bluemix}} Lite account, you can open support cases related to account and access issues or billing and usage issues. Your options are "access other self-service opportunities by using the {{site.data.keyword.Bluemix}} Assistant, docs, and community forums" as outlined on [Basic, Advanced, and Premium Support plans ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://cloud.ibm.com/docs/get-support?topic=get-support-support-plans)
