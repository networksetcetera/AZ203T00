# Demo: Create a Logic App by using the Azure Portal

In this demo you'll learn how to perform the following actions:

* Create a Logic App workflow with:
    * A trigger that monitors an RSS feed
    * An action that sends an email when the feed updates


## Prerequisites

This demo is performed in the Azure Portal.

* To get a free account visit: [https://azure.microsoft.com/free/](https://azure.microsoft.com/free/)

* An email account from an email provider that's supported by Logic Apps, such as Office 365 Outlook, Outlook.com, or Gmail. For other providers, [review the connectors list here](https://docs.microsoft.com/connectors/). This quickstart uses an Office 365 Outlook account. If you use a different email account, the general steps stay the same, but your UI might slightly differ.


### Login to Azure

1. Login to the Azure portal [https://portal.azure.com](https://portal.azure.com).

## Create a Logic App

1.  From the Azure home page, in the search box, find and select **Logic Apps**.

2.  On the **Logic Apps** page, select **Add**.

3.  On the **Logic App** pane, provide details about your logic app as shown below. After you're done, select **Create**. Replace <*Azure-subscription-name*> and <*Azure-region*> with values to fit your needs.

    Property | Value 
    - | - 
    **Name** | *az204-logicapp-demo*
    **Subscription**   | <*Azure-subscription-name*>   
    **Resource group** | *az204-logicapp-demo-rg*
    **Location**       | <*Azure-region*>                                    
    **Log Analytics**  | **Off** 

    ✔️ **Note:** Deployment can take a few minutes to complete.

## Add the RSS trigger

1. When deployment is complete navigate to your newly created Logic App.

2. In the **Templates** section select **Blank Logic App.**

3.  In the **Logic App Designer**, under the search box, select **All**.

4.  In the search box, enter `rss` to find the RSS connector. From the triggers list, select the **When a feed item is published** trigger.

5. Provide the information below for your trigger:

    <table>
    <thead>
    <tr>
    <th>Property</th>
    <th>Value</th>
    <th>Description</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><p><strong>The RSS feed URL</strong></p></td>
    <td><p><code>http://feeds.reuters.com/reuters/topNews</code></p></td>
    <td><p>The link for the RSS feed that you want to monitor</p></td>
    </tr>
    <tr>
    <td><p><strong>Interval</strong></p></td>
    <td><p><em>1</em></p></td>
    <td><p>The number of intervals to wait between checks</p></td>
    </tr>
    <tr>
    <td><p><strong>Frequency</strong></p></td>
    <td><p><em>Minute</em></p></td>
    <td><p>The unit of time for each interval between checks</p></td>
    </tr>
    </tbody>
    </table>

    <!--
    Property | Value | Description 
    - | - | -
    **The RSS feed URL** | `http://feeds.reuters.com/reuters/topNews` | The link for the RSS feed that you want to monitor
    **Interval**  | *1* | The number of intervals to wait between checks
    **Frequency** | *Minute* | The unit of time for each interval between checks
    -->
    
    Together, the interval and frequency define the schedule for your logic app's trigger. This logic app checks the feed every minute.

6.  To collapse the trigger details for now, click inside the trigger's title bar.

    ![Image showing the triggers title bar](../../linked_image_files/collapse-trigger-shape.png)

2.  Save your logic app. On the designer toolbar, select **Save**.

Your logic app is now live but doesn't do anything other than check the RSS feed. Next we'll add an action that responds when the trigger fires.

## Add the send email action

1.  Under the **When a feed item is published** trigger, select **New step**.

 
2.  Under **Choose an action** and the search box, select **All**.

3.  In the Search connectors and actions field, type **Outlook**.

    >✔️ **Note:** If you do not have an Outlook.com email account and prefer not to create one, you can change the connectors search filter to send an email and select another email provider such as Gmail and Office 365 Outlook.

4. Select **Send an email**.

5.  If your selected email connector prompts you to authenticate your identity, complete that step now to create a connection between your logic app and your email service.


6.  In the **Send an email** action enter the information in the table below:

    Field | Value
    - | -
    **To** | For testing purposes, you can use your email address.
    **Subject** | *Logic App Demo Update*
    **Body** | Select **Feed published on** from  the **Add dynamic content** list.

7.  Save your logic app.

## Run your logic app

The logic app will automatically run on the specified schedule. If you want to run it manually,  select **Run** in the Designer toolbar.

>✔️ **Note:** It may take a while for the RSS feed to update. Monitor the email inbox for the notification of a new item.
