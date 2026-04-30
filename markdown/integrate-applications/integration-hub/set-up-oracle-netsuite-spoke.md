---
title: Set up Oracle NetSuite Spoke
description: Set up your ServiceNow instance and Oracle NetSuite application so that they are integrated.Configure an OAuth 2.0 profile on Oracle NetSuite that enables integration between it and the ServiceNow instance through the OAuth 2.0 framework.Upload and commit the Update Set to your ServiceNow instance to deploy a script include called OAuthCustomOracleNetsuitGlobal to the ServiceNow instance.Configure a connection record between your ServiceNow instance and Oracle NetSuite. The record centrally stores credentials, OAuth tokens, client ID, and client secret, and is a reusable connection across flows.Generate an authentication token that enables the Oracle NetSuite requests to your ServiceNow instance to get authenticated. The requests contain events occurring in the Oracle NetSuite real-time. For example, Oracle NetSuite sends a notification when a customer record is created.Deploy a SuiteScript that enables the Oracle NetSuite to send real-time event details to the scripted API in your ServiceNow instance using the webhook.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-18"
reading_time_minutes: 6
breadcrumb: [Oracle NetSuite Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Set up Oracle NetSuite Spoke

Set up your ServiceNow instance and Oracle NetSuite application so that they are integrated.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate Oracle NetSuite Spoke.
-   Role required: admin

## Configure OAuth 2.0 in Oracle NetSuite ​

Configure an OAuth 2.0 profile on Oracle NetSuite that enables integration between it and the ServiceNow instance through the OAuth 2.0 framework.

### Before you begin

Role required: admin

### Procedure

1.  Log in to Oracle NetSuite.

2.  Navigate to **Setup** &gt; **Integration** &gt; **Manage Integrations**.

3.  Select **New**.

4.  Fill the form.

    |Field|Description|
    |-----|-----------|
    |Name|Option to enter a unique name for the OAuth integration profile.|
    |Description|Option to enter a description of the OAuth integration profile.|
    |Authorization Code Grant|Option to indicate the flow that the ServiceNow instance will use to access Oracle NetSuite.|
    |Redirect URI|Option to enter the redirect URI of ServiceNow instance in the format: `https://<instancename>.service-now.com/oauth_rediect.do`.|
    |REST Web Services|Option to indicate the scope.|

5.  Select **Save**.

    The client ID and client secret are generated.

6.  Copy and store the client ID and client secret at a secure place.

    You will need the client ID and client secret when you configure the connection and credential alias on your ServiceNow instance.


## Upload Update Set

Upload and commit the Update Set to your ServiceNow instance to deploy a script include called OAuthCustomOracleNetsuitGlobal to the ServiceNow instance.

### Before you begin

Role required: admin

### About this task

The OAuthCustomOracleNetsuitGlobal script in the Update Set contains methods for Oracle OAuth connections, designed specifically for Oracle NetSuite integration. You can upload and commit the Update Set across ServiceNow instances and enable them to handle Oracle NetSuite integration.

### Procedure

1.  From the [Oracle NetSuite spoke](https://store.servicenow.com/sn_appstore_store.do#!/store/application/5b03388aeb1d62108cc7f41fbad0cdf9/1.0.1) page on [ServiceNow Store](https://store.servicenow.com/store), download the `OAuthCustomOracleNetsuitGlobal` Update Set from to your local disk.

2.  Navigate to **System Update Sets** &gt; **Retrieved Update Sets**.

3.  Under Related Links, select Import Update Set from XML.

4.  Select **Choose File** and then navigate to the location of the `OAuthCustomOracleNetsuitGlobal` Update Set.

5.  Select **Upload**.

6.  Select **Commit Update Set**.

    The OAuthCustomOracleNetsuitGlobal script is deployed into the ServiceNow instance.


## Configure a connection record for Oracle NetSuite

Configure a connection record between your ServiceNow instance and Oracle NetSuite. The record centrally stores credentials, OAuth tokens, client ID, and client secret, and is a reusable connection across flows.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Close the notification, if it appears.

    ![New version available notification.](../image/oracle-netsuite-spk-cls-note.png)

3.  Select **Integrations**.

4.  Select the **Connections** tab.

5.  In the Search all connections field, enter `Oracle NetSuite`.

    If the **Outbound** tab is selected by default, you can do this step. If it isn’t selected, confirm that you have selected it.

6.  On the Oracle NetSuite card, select **View Details**.

    ![Oracle NetSuite View Details button.](../image/oracle-netsuite-view-details.png)

7.  Select **Configure**.

    ![Configure button.](../image/oracle-netsuite-spk-configure-button.png)

8.  Fill the form.

    |Field|Description|
    |-----|-----------|
    |Connection Name|Option to provide a unique name to the connection record.|
    |Connection URL|Option to provide the base API URL of the third-party application your ServiceNow instance connects to.|
    |OAuth Entity Name|Option to provide the name of the OAuth Entity Configuration record in ServiceNow.|
    |OAuth Client ID|Option to provide the OAuth client ID that you had generated earlier.|
    |OAuth Client Secret|Option to provide the OAuth client secret that you had generated earlier.|
    |OAuth API Script|Option to provide an optional Script Include in ServiceNow that can customize the OAuth flow. You must select `OAuthCustomOracleNetsuitGlobal` script that you had downloaded.|
    |OAuth Redirect URL|Option to enter the redirect URI of ServiceNow instance in the format: `https://<instancename>.service-now.com/oauth_rediect.do`.|
    |OAuth Authorization URL|Option to provide the URL of Oracle NetSuite’s authorization server.|
    |OAuth Token URL|Option to provide the endpoint that issues access tokens after authorization.|

9.  Select **Configure and Get OAuth Token**.

    The OAuth Access token is generated for the Oracle NetSuite spoke.

    **Note:** You must log in to Oracle NetSuite before the OAuth access token is granted.

    ![Oracle NetSuite OAuth configuration done.](../image/oracle-netsuite-spk-oauth-token-avl.png)


## Generate webhook authentication token

Generate an authentication token that enables the Oracle NetSuite requests to your ServiceNow instance to get authenticated. The requests contain events occurring in the Oracle NetSuite real-time. For example, Oracle NetSuite sends a notification when a customer record is created.

### Before you begin

Role required: admin

### About this task

**Important:** Skip this procedure if you don’t need to initiate an inbound call from Oracle NetSuite to ServiceNow.

Oracle NetSuite Webhook, a preconfigured sample scripted REST API, is available on your ServiceNow instance. It listens to events occurring on the Oracle NetSuite real-time, and logs the status of the events as success or failure in your ServiceNow instance. To enable the authentication of the events that Oracle NetSuite sends to the scripted REST API, you must generate an authentication token in the Oracle NetSuite webhook registry. The token is included in the webhook that Oracle NetSuite sends.

To access the webhook, navigate to **All**&gt;**System Web Services****&gt; Scripted Web Services****&gt; Scripted REST APIs**, in the Name field, enter `Oracle NetSuite Webhook`, and press **Enter**.

### Procedure

1.  Navigate to **All** &gt; **Oracle Netsuite Spoke** &gt; **Webhook Registry**.

2.  Select **New**.

3.  Fill the form.

    |Field|Description|
    |-----|-----------|
    |Oracle Netsuite Account Number|Option to enter the account number that the Oracle NetSuite provides.|
    |Object Name|Option to provide the type of the object in Oracle NetSuite that it includes in the webhook. For example, customer.|
    |Authentication Token|Option to generate the authentication token that Oracle NetSuite uses to have its requests authenticated on your ServiceNow instance. The token is generated after you select **Generate Authentication Token**.|
    |Description|Option to enter a description of the webhook.|

4.  Select **Generate Authentication Token**.

    The authentication token is generated.

    ![Authentication token generated.](../image/oracle-netsuite-spk-auth-token-generated.png)

5.  Copy and store the authentication token at a secure place.

6.  Select **Update**.

    The webhook is recorded in the webhook registry.

    ![Webhook registered in the webhook registry.](../image/oracle-netsuite-spk-webhook-regd.png)


## Deploy SuiteScript in Oracle NetSuite

Deploy a SuiteScript that enables the Oracle NetSuite to send real-time event details to the scripted API in your ServiceNow instance using the webhook.

### Before you begin

Role required: admin

### About this task

**Important:** Skip this procedure if you don’t need to initiate an inbound call from Oracle NetSuite to ServiceNow.

ServiceNow provides a preconfigured sample SuiteScript that you can update and enable the Oracle NetSuite to send real-time events to the scripted API in your ServiceNow instance. You update the SuiteScript by providing the authentication token you had generated, ServiceNow Webhook URL, object, and the Oracle NetSuite account number at appropriate places in the NetSuite script. After configuring the sample NetSuite script, you must deploy it on the Oracle NetSuite application so it can send events to the scripted API in your ServiceNow instance.

### Procedure

1.  From the [Oracle NetSuite spoke](https://store.servicenow.com/sn_appstore_store.do#!/store/application/5b03388aeb1d62108cc7f41fbad0cdf9/1.0.1) page on [ServiceNow Store](https://store.servicenow.com/store), download the `servicenow_webhook_call.js` file to your local disk.

2.  Log in to Oracle NetSuite.

3.  Navigate to **Customization** &gt; **Scripting** &gt; **Scripts** &gt; **New**.

4.  Select **New Script**.

    ![New Script button.](../image/oracle-netsuite-spk-deploy-netsuit1.png)

5.  Move the pointer over the **Script File** field, and click on the plus \(“+”\) icon

    ![Script File field.](../image/oracle-netsuite-spk-deploy-script2.png)

6.  Fill the form.

<table id="table_y4k_gz5_1gc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Attach From

</td><td>

Option to indicate the location from which you will attach the SuiteScript.

</td></tr><tr><td>

File Name

</td><td>

Option to provide the name of the SuiteScript file.**Important:** You must provide the extension \(.js\) of the SuiteScript file with its name.

</td></tr><tr><td>

Folder

</td><td>

Option to provide the name of the folder that contains the SuiteScript file.

</td></tr><tr><td>

Select File

</td><td>

Option to select the SuiteScript file.

</td></tr></tbody>
</table>    ![Enter file details.](../image/oracle-netsuite-spk-upload-script3.png)

7.  Select **Save**.

8.  Select **Create Script Record**.

    ![Create Script Record button.](../image/oracle-netsuite-spk-deploy-script4.png)

9.  In the Name field, enter a unique name.

    For example, `servicenow_webhook_call_customer`.

10. Provide an ID format with underscores.

    For example, `_servicenow_webhook_call_cus`

11. Select **Save**.

    ![Create script records.](../image/oracle-netsuite-spk-deploy-script5.png)

    The script record screen appears.

12. Select **Deploy Script**.

    ![Deploy Script button.](../image/oracle-netsuite-spk-deploy-script6.png)

13. In the Script Deployment page, enter the name of the object in the Applies to field.

    Example of an object: Customer.

14. Enter the ID that you have already created earlier in the procedure.

15. Enter information in the other fields, as required.

16. Select **Save**.

    The NetSuite script is deployed.


