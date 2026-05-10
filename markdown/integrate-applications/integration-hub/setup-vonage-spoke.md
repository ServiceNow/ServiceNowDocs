---
title: Set up the Vonage spoke
description: Integrate your ServiceNow instance with the Vonage instance to enable communication between them. With this integration, your ServiceNow instance can automate actions on the Vonage instance, while the Vonage instance can send payloads to your ServiceNow instance.Generate essential credentials, such as API keys, secrets, and signature secrets, to set up your Vonage developer instance. Your ServiceNow instance uses these credentials in the connection record to connect to the Vonage developer instance.Configure a connection record that enables your ServiceNow instance to connect with the Vonage instance and automate various actions on the Vonage instance. For example, create a flow on Workflow Studio that gets your Vonage account balance.Configure a connection record that enables your ServiceNow instance to connect with the Vonage instance and automate various actions on the Vonage instance. For example, create a flow on Workflow Studio that gets your Vonage account balance.Set up webhooks for SMS to enable the Vonage API platform to send data to your ServiceNow instance. For instance, if a flow in your ServiceNow instance sends an API request for call details to the Vonage API but the request fails initially, the webhook ensures that the Vonage API sends the data later.Customise the webhook routing policy and subflow as per your requirement.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 6
breadcrumb: [Vonage Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Vonage spoke

Integrate your ServiceNow instance with the Vonage instance to enable communication between them. With this integration, your ServiceNow instance can automate actions on the Vonage instance, while the Vonage instance can send payloads to your ServiceNow instance.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Vonage spoke plugin on your ServiceNow instance.
-   Role required: admin.
-   Vonage developer instance account.

## Configure the Vonage developer instance

Generate essential credentials, such as API keys, secrets, and signature secrets, to set up your Vonage developer instance. Your ServiceNow instance uses these credentials in the connection record to connect to the Vonage developer instance.

### Before you begin

Role required: admin

Access to a Vonage developer account.

### Procedure

1.  Log in to [https://developer.vonage.com/en/home](https://developer.vonage.com/en/home).

2.  On the Vonage Developer Center page, select My dashboard.![My dashboard page.](../image/Vonage-spoke-my-dashboard-link.png)

3.  On the Vonage API Dashboard page, use the default API key and the API secret or create your custom API key and API secret.

    1.  To use the default API key and the API secret, copy the default API key and the API secret values.![Copy button for API key and API secret.](../image/Vonage-spoke-copy-API-key-secret.png)

    2.  To generate a custom API key and API secret, on the left panel, select API Settings.![API settings link.](../image/Vonage-spoke-api-settings-link.png)

    3.  Select **Request more API keys**.

    4.  Fill and submit the form.

    5.  Select **Create new secret**.

    6.  In the Add a new secret window, enter your custom secret.

    7.  Select **Save**.

4.  From the Signature secret field, copy the signature secret.


## Configure connection record for Vonage connection and credential alias

Configure a connection record that enables your ServiceNow instance to connect with the Vonage instance and automate various actions on the Vonage instance. For example, create a flow on Workflow Studio that gets your Vonage account balance.

### Before you begin

Role required: admin

**Note:** Ensure that you are in the **Vonage spoke** scope.

![](../image/vonage-spoke-scope.png)

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Select Connections.

3.  In the Search all connections field, enter `Vonage`.![Search all connections field.](../image/search-all-conections.png)

4.  On the Vonage card, select **View Details**.

5.  Select **Configure**.

6.  Fill the form.

    |Field|Description|
    |-----|-----------|
    |Connection Name|The default and read-only name of the connection record. To provide a custom name to the connection record, create a connection record by selecting **Add Connection**.|
    |Connection URL|The URL to connect to the Vonage API.|
    |Messages API Version|The version of APIs the connection record requests for using the SMS feature in the Vonage instance.|
    |Voice API Version|The version of APIs the connection record requests for using the Voice feature in the Vonage instance.|
    |Credential Name|Name of the credential record. The default name os Vonage credential which you can update.|
    |Application Name|Name of the account that you had entered in the Settings page of the Vonage developers account.![Account name field on Vonage instance.](../image/Vonage-spoke-conn-record-account-name.png)|
    |API Key|API key you had acquired in the Vonage developer instance.|
    |API Secret|API secret you had acquired in the Vonage developer instance.|
    |Signature Secret|Signature secret key you had acquired in the Vonage developer instance.|

7.  Select **Create Connection**.


## Configure connection record for Vonage Primary alias

Configure a connection record that enables your ServiceNow instance to connect with the Vonage instance and automate various actions on the Vonage instance. For example, create a flow on Workflow Studio that gets your Vonage account balance.

### Before you begin

Role required: admin

**Note:** Ensure that you are in the **Vonage spoke** scope.

![](../image/vonage-spoke-scope.png)

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Flow Designer**.

2.  Select Connections.

3.  In the Search all connections field, enter `Vonage`.![Search all connections field.](../image/search-all-conections.png)

4.  On the VonagePrimary card, select **View Details**.

5.  Select **Configure**.

6.  Fill the form.

    |Field|Description|
    |-----|-----------|
    |Connection Name|The default and read-only name of the connection record. To provide a custom name to the connection record, create a connection record by selecting **Add Connection**.|
    |Connection URL|The URL to connect to the Vonage API. Enter [https://rest.nexmo.com](https://rest.nexmo.com).|
    |API Key|API key you had acquired in the Vonage developer instance.|
    |API Secret|API secret you had acquired in the Vonage developer instance.|

7.  Select **Create Connection**.


## Create a webhook to receive data from Vonage

Set up webhooks for SMS to enable the Vonage API platform to send data to your ServiceNow instance. For instance, if a flow in your ServiceNow instance sends an API request for call details to the Vonage API but the request fails initially, the webhook ensures that the Vonage API sends the data later.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Vonage spoke** &gt; **Vonage webhook Registries**.

2.  Select **New**.

3.  On the form, fill in these fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name to uniquely identify the webhook record.|
    |Description|Description of the webhook record.|
    |Event Type|Type of event for which the webhook is set up. Select **SMS**.|
    |Secret Key|Secret key to authenticate the webhook requests. Enter your custom secret key.|

4.  Right-click the form header and select **Save**.

5.  Select **Callback URL**.

    The system displays the webhook callback URL.

6.  Copy and record the webhook callback URL.

7.  Log in to [https://developer.vonage.com/en/home](https://developer.vonage.com/en/home).

8.  On the left panel, under Build &amp; Manage, select Applications.![Applications link under Build & Manage.](../image/Vonage-spoke-dashboard-applications.png)

9.  On the Your applications page, select the menu icon \(![Menu icon.](../image/Vonage-spoke-three-dots.png)\) for your application.![My application.](../image/Vonage-spoke-my-applications.png)

10. Select **Edit**.

11. Under the Messages heading, enter the callback URL in the Inbound URL and the Status URL fields.![Messages settings.](../image/Vonage-spoke-messages.png)

12. On the left panel, select API Settings.

13. On the Settings page, under SMS Settings heading, make sure that you've selected **SMS API**.

14. Fill the values.

    |Field|Value|
    |-----|-----|
    |Delivery receipts \(DLR\) webhooks|Webhook callback URL|
    |Inbound SMS webhooks|Webhook callback URL|

15. Select **Save changes**.

    SMS settings for the application are saved.


## Customize webhooks and routing policies

Customise the webhook routing policy and subflow as per your requirement.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Flow Designer** &gt; **Designer**.

2.  Click **Subflows**.

3.  Create a copy of the required default subflow.

4.  Customize the subflow as per your requirement and publish it.

    See [Building subflows](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/subflows.md) for more information about creating and using subflows and [Vonage Spoke](../concept/vonage-spoke.md) for information about the fields that the default routing policy and subflows support.

5.  Navigate to **Vonage Spoke** &gt; **Vonage WebHook Routing Policy**.

6.  Click **New**.

7.  On the form, fill in the fields.

<table id="table_awj_xgv_z3b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Label

</td><td>

Unique label to identify the routing policy.

</td></tr><tr><td>

Default answer

</td><td>

Option to specify if this is the default answer. The default answer is applicable when the conditions are not met.1.  Click the lookup icon \(![Lookup icon](../image/lookup-icon.png)\).
2.  Select the required subflow from the Document list.

**Note:** Ensure that the **Table name** is `Flow [sys_hub_flow]`.

</td></tr><tr><td>

Condition

</td><td>

Conditions to be met when the required events occur in Vonage. The supported Vonage fields are:-   Keywords
-   Call Direction
-   Call Status
-   Event Type
-   From
-   SMS Status
-   SMS Text
-   To
-   WhatsApp Message Status
-   WhatsApp Text
-   Show Related Fields


</td></tr><tr><td>

Answer

</td><td>

Subflow that must be triggered when the specified conditions are met.

</td></tr></tbody>
</table>8.  Click **Submit**.

    **Note:** These routing policies are saved in the Decision tables. Users are cautioned against directly updating or modifying data in these tables.


