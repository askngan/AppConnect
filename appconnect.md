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


# IBM App Connect concepts
{: #concepts}

{{site.data.keyword.appconservicefull}} is a business-friendly tool that you can use to integrate your cloud-based or on-premises applications to automate tedious and repetitive tasks.

{{site.data.keyword.appconserviceshort}} connects your applications in minutes - automating updates, notifications, and events, and keeping your data in sync between multiple applications. You can use it to connect applications in the cloud or local (on-premises) applications.  

You can run two types of resource in {{site.data.keyword.appconserviceshort}} to connect your apps, depending on your business needs: integration servers and flows.  To run your IBM Integration Bus or App Connect Enterprise solutions, you upload an integration solution in a BAR file, then run it in an integration server in {{site.data.keyword.appconserviceshort}}.  You create flows in {{site.data.keyword.appconserviceshort}} to connect your applications so that something that happens in one application makes something else happen in another application.  You can create event-driven flows and flows for APIs.

You can use the {{site.data.keyword.appconserviceshort}} dashboard to monitor your flows and integration servers to see how much work they're doing for you. Start and stop them, and change them when you need to.

Here we explain the features and terminology of {{site.data.keyword.appconserviceshort}} in more detail:

-   [Flows](#flows)
-   [Applications](#apps)
-   [Actions](#actions)
-   [Data mapping](#transforms)
-   [BAR files and integration servers](#barfiles)

## Flows
{: #flows}

You can create two types of flow in {{site.data.keyword.appconserviceshort}}: an event-driven flow and a flow for an API.

In an event-driven flow, you identify an event that can occur in your first application (the source application), and actions that can be performed in one or more target applications. The flow links the event to the actions so that, whenever the event occurs in the source application, the action is automatically triggered in the target applications. Each successfully completed action counts towards your monthly quota. When you create a flow, you add your applications, and choose actions. Then, you map the data that you want to transfer between your applications.

For example, you might create a flow so that whenever someone registers as a new attendee with Eventbrite (the event), {{site.data.keyword.appconserviceshort}} automatically retrieves details of the attendee from Salesforce and creates a new task in Asana (the actions).

![A multi-node flow, with the source application and two target applications](images/multi_node_flow2.jpg)

For more information, see [Creating an event-driven flow ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/creating-event-driven-flow/).

A flow for an API contains a request, one or more target application actions, and a response. The request uses a model that you define to request the creation, replacement, or retrieval of data objects in your applications. When the request is submitted, each target application performs its action.  The flow then returns a response that either confirms that the actions were successful, or returns the data that was requested.

![A flow for an API that creates a product in Salesforce](images/APIFlow2.jpg)

For more information, see [Creating flows for an API ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/creating-flows-api/).

As well as adding applications to your flows, you can also add nodes from the **Logic** tab to configure how you process data. For example, use the If node to add some conditional processing - performing different actions according to the data that you receive (see [Adding conditional logic to a flow ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/adding-conditional-logic-flow/)). And use the For each node when you want to perform an action for each record that's returned by a retrieve action (see [Retrieving items from your applications ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/using-ibm-app-connect-retrieve-items-applications/)).

If you're an IBM Integration Bus or App Connect Enterprise developer, you can also create complex integration solutions by developing message flows in the Integration Toolkit and packaging them into BAR files.

Your flows and integration servers are represented by tiles on the App Connect dashboard. The tiles show summary information about the flow, API, or integration server, such as whether a flow is running or stopped, and if it's run successfully, or produced an error. You can click the tick and exclamation point icons to see when the flow last ran successfully, or what errors were raised. Click the three dots ![Icon of three vertical dots opens a menu to start, stop, edit, or delete the flow](images/Menu.jpg) to open a menu to start, stop, edit, or delete your resources. Flows have to be stopped before you can edit them.

![Screen capture showing tiles from the dashboard for event-driven flows, flows for APIs, and integration servers](images/Dashboard.jpg)

## Applications
{: #apps}

When you create event-driven flows or flows for APIs, _applications_ are the cloud-based software applications that you're connecting.  You can see a list of the applications that you can connect with {{site.data.keyword.appconserviceshort}} on the **Applications** page. Click an application to find out more about it, to see what events and actions are supported, and to connect to your own account. You can connect multiple accounts to each application and switch between them on the Applications page. After you connect to your account, you can also update or remove your account on this page.

![Screen capture of one of the applications on the Applications page](images/Magento2.jpg)

You don't have to connect to your applications on the Applications page; you can also connect in the flow editor as you add the applications to your flow. Many applications require just a user name and password, but some need more information. You can find out how to find this information in the [How-to guides for apps ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/integration/docs/app-connect/how-to-guides-for-apps/).

If you're using {{site.data.keyword.appconservicefull}} to run Integration Bus or App Connect Enterprise solutions in the cloud, an _application_ is the container that holds your message flows, libraries, and other resources that are required by your solution. 

## Actions
{: #actions}

You can add several types of action to your flows. Common actions are create, retrieve, and update or create, but some applications have specific actions. For example, the Watson Personality Insights application has an action that's called "Analyze personality". You can see a list of actions that are supported for applications in {{site.data.keyword.appconserviceshort}} by typing the action type in the search field on the Applications page:

![Screen capture showing supported retrieve actions for applications](images/RetrieveApps2.jpg)

**Create**

As the name suggests, the create action creates an object or record in an application. For example, if someone signs up to your event or submits a completed form, you might want to create a record for that person in your CRM or marketing application. Or if someone opens a ticket in your help desk application, you might want to create an email or instant message to ensure that someone deals with it straight away. If there’s a possibility that the object that you want to create might already exist, you can use an *update or create* action instead.

For some applications, you might have to provide some extra information when you add a create action to a flow so that your flow knows where to create the object. For example, if you're using a project management application like Asana or Trello, when you create a task or a card, you need to specify the project or the board where you want to add it.

**Update or create**

The update or create action changes an existing record in your target application if it exists, but creates the record if it doesn’t exist. It’s also known as an upsert (update or insert) action.

For example, say that someone submits a Wufoo form with a change of address. If the contact is already in your CRM system, you want to update their address; but if they’re not, you want to add them. Like the retrieve action, when you choose an action to update data in one of your applications, you can add one or more conditions to ensure that you’re updating the right information.

If there’s more than one record in your target system that matches your criteria, you see an error for the flow on the dashboard, and the flow won’t update or create any records. For example, maybe you have more than one contact with the same first and last names. So you could try to match a contact by using unique data, such as their email address.

The status codes that you’re likely to see in response to an update or create action are:

-   200: A record was updated
-   201: A record was created

You can use these response codes later in your flow. Maybe you want to take different actions depending on whether a record was updated or created. For an example of defining actions based on response codes, see the tutorial [Creating an event-driven flow that updates or creates a contact in Salesforce and updates Asana whenever you receive a form in Wufoo ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/creating-event-driven-flow-updates-creates-contact-salesforce-updates-asana-whenever-receive-form-wufoo/).

**Retrieve**

The retrieve action gets information from an application so that you can use it in another application.

When you add an action to your flow to retrieve objects, you can define one or more conditions to make sure that you’re retrieving the right items. Or, if you want to retrieve all items of a particular type, you can delete the condition. You can also define how many items you want to retrieve, and what happens if {{site.data.keyword.appconserviceshort}} finds more than or less than that number.

You can handle your retrieved items in two ways:

-   You can add a "For each" node after the retrieve action to perform an action for each of the items that were retrieved.
-   You can add another action after the retrieve action to process the list of retrieved items. This action is a single action, no matter how many items are returned – such as creating an email that lists all the retrieved items.

You can also decide what action to take based on the status code that you get in response to the retrieve action. You could use an “If” node to perform different actions for different status codes. The status codes that you’re likely to see in response to a retrieve action are:

-   204: No records were found
-   200: All records in the application match the condition
-   206: The specified maximum number of records were retrieved, but more matching records exist in the application

For more information, see [Retrieving items from your applications ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/using-ibm-app-connect-retrieve-items-applications/).

## Data mapping
{: #transforms}

When you've created a flow, added your applications, and selected appropriate actions, you need to specify what information you want to transfer between your applications. You can see in the flow editor that when you add an action to your flow, you see a list of available fields for that application.  You can populate these fields with data from your source application, or previous actions in the flow.

Some fields are mandatory, and they're marked with an asterisk. For example, when you're creating a lead in Salesforce, you must specify a last name:

![Screen capture showing that the Last name field is mandatory](images/LastName.jpg)

When you click in one of these fields, you see a couple of icons: **Insert reference**![Insert reference icon](images/InsertRef.jpg) and **Apply a Function**![Apply a function icon](images/Functions.jpg). If you click **Insert reference**, you can see the available data that you can put in that field from preceding applications in the flow. The following example shows that we can choose fields from the Wufoo source application, or from a previous Salesforce action in the flow. We can also use the status code from the Salesforce update or create action.

![Screen capture showing available inputs for a data mapping](images/Inputs.jpg)

In the following example, our flow is triggered by a new completed form being received in Wufoo. We want to create a contact in Salesforce for the person who's submitted the form. So when we add our Salesforce "Create contact" action to the flow, we copy the details for our contact from the Wufoo form. Here we can see that for the last name of the Salesforce contact, we've selected the last name of the Wufoo form submitter. You can see that the mapped field is from Wufoo because of the color:

![Screen capture showing that the Wufoo Last name field is mapped to the Salesforce Last name field](images/Mapping.jpg)

In the following example, we've added a Slack "Create message" action to the flow after a Salesforce "Update or create contact" action. We simply want to put a message on Slack to say what response code was received for the Salesforce action:

![Screen capture of a Slack Create message action that maps a response code](images/SlackSC.jpg)

You can see that in the **Text** field for the Slack "Create message" action, we've typed a message, then mapped in the status code for the Salesforce "Update or create contact" action.

Here's another example of mapping response codes in a different way. This time, we've added an "If" node after a Salesforce "Update or create contact" action because we want to perform different actions that depend on whether an existing Salesforce contact was updated, or a new contact was created. In this case, a response code of "200" means that the contact was updated. So this branch of the "If" node contains an action that's specific to an updated record.

![Screen capture showing response codes being used in an If node](images/IfSC.jpg)

The **Apply a function** icon ![Apply a function icon](Functions.jpg) shows you a list of transformation functions that you can use to customize the data that you're passing through your flow. These functions can be as simple as converting a particular field to upper or lower case, or slightly more complex, such as finding and replacing specific patterns in the data. They can also be as powerful as forming regular expressions. You can either select the function that you want from the list, or you can type it in yourself. The syntax of the functions is JSONata, a lightweight query and transformation language. For more information, see [http://jsonata.org ![External link icon](../../icons/launch-glyph.svg "External link icon")](http://jsonata.org).


## BAR files and integration servers
{: #barfiles}

A BAR file is a compressed file to which you add deployable resources in IBM Integration Bus or App Connect Enterprise.  When you develop an integration solution in Integration Bus or App Connect Enterprise, you package your message flows and all the resources that those message flows use in a BAR file.  You then deploy the BAR file to an integration server.  That server can be on premises or in {{site.data.keyword.appconserviceshort}}.  You can run your Integration Bus or App Connect Enterprise solutions in App Connect, without the need to acquire and maintain an IT infrastructure.  When you upload a BAR file to App Connect, an integration server is created to run the contents of the BAR file.  You can configure basic authentication and secure connectivity between your cloud-based and on-premises resources (see [Running your Integration Bus solutions in App Connect ![External link icon](../../icons/launch-glyph.svg "External link icon")](https://developer.ibm.com/integration/docs/app-connect/tutorials-for-ibm-app-connect/running-your-ibm-integration-bus-solutions-in-ibm-app-connect-enterprise-beta-plan)).  

