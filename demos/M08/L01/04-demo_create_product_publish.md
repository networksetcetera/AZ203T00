# Demo: Create and publish a product

In this demo you'll learn how to perform the following actions:

* Create and publish a product

>✔️ **Note:** This demo relies on the successful completion of the  *Create an APIM instance by using Azure CLI* and *Import an API by using the Azure Portal* demos.

## Prerequisites

This demo is performed in the Azure Portal.

### Login to the Azure Portal

1.  Login to the portal: [https://portal.azure.com](https://portal.azure.com) 


## Go to your API Management instance

1. In the Azure portal, search for and select **API Management services**.

    ![Image showing searching for, and selecting, API Management services](../../linked_image_files/view-apim1.png)

2. On the **API Management** screen, select the API Management instance you created in the *Create an APIM instance by using Azure CLI* demo.


## Create and publish a product

1.  Click on **Products** in the menu on the left to display the **Products** page.

2.  Click **+ Add**. When you add a product, you need to supply the following information:

    <table>
    <thead>
    <tr>
    <th>Setting</th>
    <th>Value</th>
    <th>Description</th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><p>Display name</p></td>
    <td><p><em>AZ204 API Demo</em></p></td>
    <td><p>The name as you want it to be shown in the <strong>Developer portal</strong>.</p></td>
    </tr>
    <tr>
    <td><p>Id</p></td>
    <td><p><em>az204-api-demo</em></p></td>
    <td><p>This is auto-populated when you tab out of the <strong>Display name</strong> field.</p></td>
    </tr>
    <tr>
    <td><p>Description</p></td>
    <td><p><em>AZ204 Class Demo</em></p></td>
    <td><p>The <strong>Description</strong> field allows you to provide detailed information about the product such as its purpose, the APIs it provides access to, and other useful information.</p></td>
    </tr>
    <tr>
    <td><p>State</p></td>
    <td><p>Select <strong>Published</strong></p></td>
    <td><p>Before the APIs in a product can be called, the product must be published. By default new products are unpublished, and are visible only to the  <strong>Administrators</strong> group.</p></td>
    </tr>
    <tr>
    <td><p>Requires subscription</p></td>
    <td><p>Leave unchecked</p></td>
    <td><p>Check <strong>Require subscription</strong> if a user is required to subscribe to use the product.</p></td>
    </tr>
    <tr>
    <td><p>Requires approval</p></td>
    <td><p>Leave unchecked</p></td>
    <td><p>Check <strong>Require approval</strong> if you want an administrator to review and accept or reject subscription attempts to this product. If the box is unchecked, subscription attempts are auto-approved.</p></td>
    </tr>
    <tr>
    <td><p>Subscription count limit</p></td>
    <td><p>Leave blank</p></td>
    <td><p>To limit the count of multiple simultaneous subscriptions, enter the subscription limit.</p></td>
    </tr>
    <tr>
    <td><p>Legal terms</p></td>
    <td><p>Leave blank</p></td>
    <td><p>You can include the terms of use for the product which subscribers must accept in order to use the product.</p></td>
    </tr>
    <tr>
    <td><p>APIs</p></td>
    <td><p>Select <strong>Select API</strong> and add the <em>Demo Conference API</em></p></td>
    <td><p>Products are associations of one or more APIs. You can include a number of APIs and offer them to developers through the developer portal.</p></td>
    </tr>
    </tbody>
    </table>

    <!--
    Setting | Value | Description
    - | - | -
    Display name | *AZ204 API Demo* | The name as you want it to be shown in the **Developer portal**.
    Id | *az204-api-demo* | This is auto-populated when you tab out of the **Display name** field.
    Description | *AZ204 Class Demo* | The **Description** field allows you to provide detailed information about the product such as its purpose, the APIs it provides access to, and other useful information.
    State | Select **Published** | Before the APIs in a product can be called, the product must be published. By default new products are unpublished, and are visible only to the  **Administrators** group.
    Requires subscription | Leave unchecked | Check **Require subscription** if a user is required to subscribe to use the product.
    Requires approval | Leave unchecked | Check **Require approval** if you want an administrator to review and accept or reject subscription attempts to this product. If the box is unchecked, subscription attempts are auto-approved.
    Subscription count limit | Leave blank | To limit the count of multiple simultaneous subscriptions, enter the subscription limit.
    Legal terms | Leave blank | You can include the terms of use for the product which subscribers must accept in order to use the product.
    APIs | Select **Select API** and add the *Demo Conference API* | Products are associations of one or more APIs. You can include a number of APIs and offer them to developers through the developer portal.
    -->

3.  Select **Create** to create the new product.

>✔️ **Note:** The developer portal will not be available since the APIM instance was created using the Consumption plan. 

