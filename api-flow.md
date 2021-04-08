---

copyright:
  years: 2017, 2020, 2021
lastupdated: "2021-04-08"

subcollection: AppConnect

content-type: tutorial
account-plan: lite
completion-time: 10m

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


# Creating a flow for an API
{: #tutorial-api-flow}
{: toc-content-type="tutorial"}
{: toc-completion-time="10m"}

If you want a developer to be able to create an application that uses the data in your cloud-based applications, you can provide an API. To create flows for an API, complete the following steps.
{: shortdesc}

## Create a flow for an API
{: #create-flow-api}
{: step}

1. On the {{site.data.keyword.appconnect_notm}} dashboard, click **New** > **Flows for an API**.
1. Enter a name for your API.

## Create a model
{: #create-model}
{: step}

1. Enter a name for your model that reflects the type of object that your API works with, then click **Create model**.
1. Add the properties that are required to define the structure of your object that your API works with.
    For example, if your API creates or retrieves a customer, you might add properties that are called Customer_ID, First_Name, Last_Name, and Email_Address. You can either type in the name of a property, or click **Select properties from applications** to choose properties from one or more of the applications that you’re connected to.
1. Click **Operations** to define how the API interacts with the object, and add the operations that you need.

## Implement a flow
{: #implement-flow}
{: step}

1. For each operation, click **Implement flow** to create a flow that defines how each operation works.
1. Add one or more target applications to the flow, between the request and response.
    If you want your flow to do different things for different conditions, you can also add some conditional logic (see [Adding conditional logic to a flow ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://www.ibm.com/docs/en/app-connect/cloud?topic=utilities-if-conditional)).
1. Click the **Response** in the flow to define the response that is returned when the operation is completed. Map the available fields from your target application.
1. Click **Done** to return to your model.

## Start your API
{: #start-api}
{: step}

When all your models and operations are defined, start the API by selecting **Start API** from the menu.

The flows for your API are ready. On the {{site.data.keyword.appconnect_notm}} dashboard, flows for APIs are identified by the API icon. You can start and stop them in the same way as any other flow. You can open an API while it’s running, but you have to stop it before you can edit it.

## Next steps
{: #api-next-steps}

- To follow a tutorial about creating a flow for an API, see [Creating flows for an API  ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://www.ibm.com/docs/en/app-connect/cloud?topic=connect-introduction-creating-flows-api-part-1).
- To find out how to test your API, see [Testing an API flow ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://www.ibm.com/docs/en/app-connect/cloud?topic=flows-testing-running-flow#testapi).
