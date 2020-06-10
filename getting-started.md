---

copyright:
  years: 2017, 2019
lastupdated: "2019-11-22"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip} 
{:download: .download}


# Getting started tutorial
{: #getting-started}

{{site.data.keyword.appconservicefull}} helps you to connect your applications: from simple trigger-action interactions to complex integrations.  You can use {{site.data.keyword.appconserviceshort}} to create event-driven flows or flows for APIs.  Or you can upload and run the integration solutions that you create in IBM App Connect Enterprise or IBM Integration Bus, without the need to acquire and maintain an IT infrastructure.  You can see and administer all your integrations - integration servers, event-driven flows, and flows for APIs - in one place on the {{site.data.keyword.appconserviceshort}} dashboard. 

After you create an instance of the {{site.data.keyword.appconserviceshort}} service, you can access {{site.data.keyword.appconserviceshort}} from the {{site.data.keyword.Bluemix}} dashboard.

The following steps provide enough information for you to get started with App Connect.  For more detailed instructions, how-to guides for specific applications, tutorials, and videos, see the full set of documentation at [IBM App Connect ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/integration/docs/app-connect/).

## Creating an event-driven flow

As the name suggests, an event-driven flow consists of an event in a source application, which triggers the flow, and one or more actions in target applications. So when something happens in the source application, an action is triggered in your target applications.  To create an event-driven flow that connects your cloud-based applications, complete the following steps.
1.  On the {{site.data.keyword.appconserviceshort}} dashboard, click **New** > **Event-driven flow**.
    {{site.data.keyword.appconserviceshort}} saves your changes automatically as you go. If you navigate away from the flow at any stage, the flow is saved as a draft flow that you can complete at another time.
1.  Enter a name for your flow.
1.  Select the trigger event to start your flow by expanding an application and selecting an event.
1.  If you're not already connected to your application, click **Connect** and enter your login details for the application.
    You might have to provide extra connection details for some applications; if you need help with finding credentials for a particular application, see the [How-to guides for apps ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/integration/docs/app-connect/how-to-guides-for-apps/).
1.  Select the action to be triggered in your second application by clicking the plus icon in the flow ![Add an application icon](/images/AddApp.jpg), expanding an application, and selecting an action.
    If necessary, click **Connect** and enter your login details for the target application.
1. Enter the data that you want to transfer between your applications.
    You can add source field names manually by clicking in a field then clicking the mapping icon ![Mapping icon](/images/MappingIcon.jpg). You can also type in text, or use a transformation function to customize the source value. For more information, see [Applying JSONata functions to transform your data ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/integration/docs/app-connect/creating-managing-event-driven-flows/completing-fields-action/applying-jsonata-functions/).
1. Optional: You can refine how your flow works by doing the following things:
    * Add more target applications and actions by clicking the plus icon in the flow ![Add an application icon](/images/AddApp.jpg).
    * Add retrieval actions to your flow to retrieve items that match certain criteria or retrieve a specified number of records.  You can also add retrieval actions that define error handling or define how you handle the items that are retrieved (see [Using App Connect to retrieve items from your applications ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/using-ibm-app-connect-retrieve-items-applications/)).
    * Add some conditional logic to perform different actions that depend on the data that is received from applications in your flow (see [Adding conditional logic to a flow ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/integration/docs/app-connect/toolbox-utilities/adding-conditional-logic-flow/)).

1. When your flow is configured, open the options menu on the header bar and click **Start flow**.

If you return to the {{site.data.keyword.appconserviceshort}} dashboard, you can see that your flow is running.  When an event happens in the first application, an action is triggered automatically by {{site.data.keyword.appconserviceshort}} in your second application. You can view the status of your flows on the {{site.data.keyword.appconserviceshort}} dashboard.  To view logs for your flows, click the **Logs** icon ![Logs icon](/images/LogsIcon.jpg).

For more information, see [Creating an event-driven flow ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/creating-event-driven-flow/).

To follow a tutorial for a typical event-driven flow, see [Creating a ServiceNow incident and sending an email when a Wufoo form is submitted ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/creating-event-driven-flow-creates-servicenow-incident-someone-submits-wufoo-form/).

## Creating a flow for an API

If you want a developer to be able to create an application that uses the data in your cloud-based applications, you can provide an API. To create flows for an API, complete the following steps.
1. On the {{site.data.keyword.appconserviceshort}} dashboard, click **New** > **Flows for an API**.
1. Enter a name for your API.
1. Enter a name for your model that reflects the type of object that your API works with, then click **Create model**.
1. Add the properties that are required to define the structure of your object that your API works with.
    For example, if your API creates or retrieves a customer, you might add properties that are called Customer_ID, First_Name, Last_Name, and Email_Address. You can either type in the name of a property, or click **Select properties from applications** to choose properties from one or more of the applications that you’re connected to.
1. Click **Operations** to define how the API interacts with the object, and add the operations that you need. 
1. For each operation, click **Implement flow** to create a flow that defines how each operation works. 
1. Add one or more target applications to the flow, between the request and response. 
    If you want your flow to do different things for different conditions, you can also add some conditional logic (see [Adding conditional logic to a flow ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/integration/docs/app-connect/toolbox-utilities/adding-conditional-logic-flow/)).
1. Click the **Response** in the flow to define the response that is returned when the operation is completed. Map the available fields from your target application. 
1. Click **Done** to return to your model.
1. When all your models and operations are defined, start the API by selecting **Start API** from the menu. 

The flows for your API are ready. On the {{site.data.keyword.appconserviceshort}} dashboard, flows for APIs are identified by the API icon. You can start and stop them in the same way as any other flow. You can open an API while it’s running, but you have to stop it before you can edit it.

For more information, see [Creating flows for an API  ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/creating-flows-api/).

To find out how to test your API, see [Exposing an App Connect flow through API Connect ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/integration/blog/2017/08/29/exposing-app-connect-flow-api-connect/).


## Running an IBM App Connect Enterprise or IBM Integration Bus integration solution

You can deploy integration solutions that are developed in App Connect Enterprise or Integration Bus to the cloud, without the need to acquire and maintain an IT infrastructure. Import a BAR file that contains all the artifacts that make up your integration solution, then run the contents in an integration server in App Connect. (To create a BAR file, you must have App Connect Enterprise, or Integration Bus v10.0.0.4 or later, installed on premises.)

To run your App Connect Enterprise or Integration Bus solutions in App Connect, complete the following steps.
1. On the {{site.data.keyword.appconserviceshort}} dashboard, click **New** > **Import a BAR file**.
1. Select the BAR file that you want to import, then click **Import**. 
    If you see an authentication error, check that your BAR file is valid (see [What makes a BAR file valid in App Connect? ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/integration/docs/app-connect/creating-managing-enterprise-integrations/running-on-ibm-cloud/what-makes-a-bar-file-valid-for-app-connect-app-connect-enterprise-beta/)).
    An integration server is created, and a tile is added to the dashboard to represent it. The status changes from "Preparing" to "Stopped" when the integration server is ready to be configured and started. 
1. Click the tile to open the integration server.
1. Configure the integration server:
    * Add or edit a description for your integration solution.
    * Configure HTTPS basic authentication (see [Configuring HTTPS basic authentication ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/integration/docs/app-connect/creating-managing-enterprise-integrations/running-on-ibm-cloud/configuring-https-basic-authentication-app-connect-enterprise-beta/)).
    * Attach a policy so that you can connect to on-premises systems (see [Configuring secure connectivity between integration servers on App Connect and on-premises systems ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/integration/docs/app-connect/creating-managing-enterprise-integrations/running-on-ibm-cloud/configuring-secure-connectivity-cloud-and-on-premises/)).
1. Optional: To split message flow processing between your on-premises environment and App Connect, configure callable flows by clicking the **Callable flows** icon ![Callable flows icon](/images/CallFlowIcon.jpg) (see [Sharing message flow processing between App Connect on IBM Cloud and App Connect Enterprise or Integration Bus ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/integration/docs/app-connect/creating-managing-enterprise-integrations/running-on-ibm-cloud/sharing-message-flow-processing-cloud-and-on-premises/)).
1. When configuration is complete, return to the App Connect dashboard and start the integration server by opening the tile menu and clicking **Start**.

When your integration server is running, you can view and download logs by opening the integration server and clicking **View logs**. To view the logs, you have to attach a Logging policy to your integration server (see [Viewing logs for your integration servers ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/integration/docs/app-connect/creating-managing-enterprise-integrations/running-on-ibm-cloud/viewing-logs-for-your-integration-servers-in-app-connect-enterprise-beta/).)

For more information, see [Running enterprise integration solutions in App Connect ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/integration/docs/app-connect/creating-managing-enterprise-integrations/running-on-ibm-cloud/).
