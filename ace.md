---

copyright:
  years: 2017, 2020
lastupdated: "2020-09-18"

content-type: tutorial
services:
account-plan: paid
completion-time: 30m

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip}
{:download: .download}
{:step: data-tutorial-type='step'}


# Running an ACE or IIB integration solution
{: #tutorial-ace}
{: toc-content-type="tutorial"}
{: toc-services=""}
{: toc-completion-time="30m"}

You can deploy integration solutions that are developed in App Connect Enterprise (ACE) or IBM Integration Bus (IIB) to the cloud, without the need to acquire and maintain an IT infrastructure. Import a BAR file that contains all the artifacts that make up your integration solution, then run the contents in an integration server in App Connect. (To create a BAR file, you must have App Connect Enterprise, or Integration Bus v10.0.0.4 or later, installed on premises.)
{: shortdesc}

To run your App Connect Enterprise or Integration Bus solutions in App Connect, complete the following steps.

## Before you begin
{: #ace-prereqs}

Create an instance of the {{site.data.keyword.appconserviceshort}} service using the Enterprise plan.

## Import a BAR file
{: #import-bar-file}
{: step}

1. On the {{site.data.keyword.appconserviceshort}} dashboard, click **New** > **Import a BAR file**.
1. Select the BAR file that you want to import, then click **Import**.
    If you see an authentication error, check that your BAR file is valid (see [What makes a BAR file valid in App Connect? ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://www.ibm.com/support/knowledgecenter/en/SSTTDS_11.0.0/com.ibm.ace.cloud.doc/developing-integration-for-app-connect-on-cloud.html#validbarforaceoc)).
    An integration server is created, and a tile is added to the dashboard to represent it. The status changes from "Preparing" to "Stopped" when the integration server is ready to be configured and started.
1. Click the tile to open the integration server.

## Configure an integration server
{: #integration-server}
{: step}

Configure the integration server:
- Add or edit a description for your integration solution.
- Configure HTTPS basic authentication (see [Configuring HTTPS basic authentication ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://www.ibm.com/support/knowledgecenter/en/SSTTDS_11.0.0/com.ibm.ace.cloud.doc/configuring-https-basic-auth.html)).
- Attach a policy so that you can connect to on-premises systems (see [Configuring integration servers by using policies ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://www.ibm.com/support/knowledgecenter/en/SSTTDS_11.0.0/com.ibm.ace.cloud.doc/aceoc-policies.html)).

## Configure a callable flow
{: #callable-flow}
{: step}

Optional: To split message flow processing between your on-premises environment and App Connect, configure callable flows by clicking the **Callable flows** icon ![Callable flows icon](/images/CallFlowIcon.jpg) (see [Sharing flow processing between App Connect on IBM Cloud and App Connect Enterprise or Integration Bus ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://www.ibm.com/support/knowledgecenter/en/SSTTDS_11.0.0/com.ibm.ace.cloud.doc/sharing-processing-cloud-and-on-premises.html)).

## Start the integration server
{: #start-integration-server}
{: step}

When the configuration is complete, return to the App Connect dashboard and start the integration server by opening the tile menu and clicking **Start**.

When your integration server is running, you can view and download logs by opening the integration server and clicking **View logs**. To view the logs, you have to attach a Logging policy to your integration server (see [Viewing logs for your integration servers ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://www.ibm.com/support/knowledgecenter/en/SSTTDS_11.0.0/com.ibm.ace.cloud.doc/viewing-logs-for-integration-servers.html).)

## Next steps
{: #ace-next-steps}

- For more information, see [Running enterprise integration solutions in App Connect ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://www.ibm.com/support/knowledgecenter/en/SSTTDS_11.0.0/com.ibm.ace.cloud.doc/deploying-testing-enterprise-integration-solution-app-connect-ibm-cloud.html).
