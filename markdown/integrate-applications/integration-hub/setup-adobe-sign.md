---
title: Synchronize Adobe Sign group with ServiceNow
description: Synchronize ServiceNow with the required group in Adobe Sign to access the group specific documents, and agreements from the Adobe Sign spoke.Create a custom OAuth application from your Adobe Sign account to enable OAuth 2.0 authentication with the Adobe Sign spoke.Configure the webhook in your Adobe Sign application to enable Adobe Sign to send data to ServiceNow when a participant signs an agreement or document.Add and configure a Adobe Sign spoke connection to authenticate ServiceNow requests.Allow Adobe Sign spoke to create group admin user role when an Adobe Sign group is synchronized with ServiceNow tables by configuring the application access of the required ServiceNow tables.Synchronize ServiceNow with the required group in Adobe Sign by creating a record in the AdobeSign Group Details \[sn\_adobesign\_spoke\_adobesign\_group\_details\] table.Synchronize ServiceNow with the required group in Adobe Sign to access the documents and agreements that are specific to the group, from the Adobe Sign spoke.
locale: en-US
release: xanadu
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Adobe Sign Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Creating integrations with applications]
---

# Synchronize Adobe Sign group with ServiceNow

Synchronize ServiceNow with the required group in Adobe Sign to access the group specific documents, and agreements from the Adobe Sign spoke.

## Before you begin

-   Request Integration Hub subscription
-   Activate the Adobe Sign spoke
-   Role required: admin

## About this task

These steps are performed to synchronize only one Adobe Sign group. To synchronize another Adobe Sign group, repeat this process.

## Create custom OAuth application in Adobe Sign account

Create a custom OAuth application from your Adobe Sign account to enable OAuth 2.0 authentication with the Adobe Sign spoke.

### Before you begin

-   Adobe Sign account
-   Role required: Adobe Sign admin credentials

### About this task

Complete these steps from your Adobe Sign account. See the [Adobe Sign development](https://www.adobe.io/apis/documentcloud/sign/docs.html) documentation for instructions on creating and configuring custom applications.

### Procedure

1.  From your Adobe Sign account, create an application.

2.  Copy and record the Application ID and Application Secret for later use.

    These details are required to register the application as a third-party OAuth provider on your ServiceNow instance.


### Result

The custom OAuth application from your Adobe Sign account is created and can be integrated with the ServiceNow instance.

## Configure the webhook

Configure the webhook in your Adobe Sign application to enable Adobe Sign to send data to ServiceNow when a participant signs an agreement or document.

### Before you begin

Role required: admin

### About this task

If the scope of the Adobe Sign application is Account, use the same webhook for all the groups defined within the account scope. If the scope of the Adobe Sign application is Group, you must configure for each group.

### Procedure

1.  From your Adobe Sign account, create a webhook with these configurations.

    1.  Enter the target URL in **URL** in this format: `https://<instance-name>.service-now.com/api/sn_adobesign_spoke/adobesign_webhook`.

    2.  Enter `Agreement all events` and `Mega Sign all events` in **Events**.

    3.  Select all the required agreement events in **Notification Parameters**.

        See the [Adobe Sign development](https://www.adobe.io/apis/documentcloud/sign/docs.html) documentation for more information about creating webhooks in your Adobe Sign account.

2.  In your ServiceNow instance, add the client details.

    1.  Navigate to **Adobe Sign Spoke** &gt; **Client Details**.

    2.  Open the record, **Adobe Sign Client ID**.

    3.  On the form, fill these values.

        |Field|Description|
        |-----|-----------|
        |Authentication Key|Key to authenticate. Enter `UB7E5BXCXY`.|
        |Client ID|Application ID created during the Adobe Sign account configuration.|

    4.  Click **Update**.


### Result

Webhook is created in your Adobe Sign account and signing events in Adobe Sign are updated in the tables of the Adobe Sign spoke.

## Configure a connection for the Adobe Sign spoke

Add and configure a Adobe Sign spoke connection to authenticate ServiceNow requests.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Under **Connections**, toggle and enable the **Outbound** connections.

4.  Locate the alias for **AdobeSign\_HR\_Group** and click **View Details**.

    -   To configure the default connection and credential alias record that is shipped along with the Adobe Sign spoke, click **View Details**.

        ![Connection for Adobe Sign spoke](../image/adobe-sign-connection.png)

    -   To manage more than one Adobe Sign spoke connection records, you should create a new child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](../../integrationhub/concept/support-multiple-connections.md).
    If you are configuring the spoke for the first time, click **Configure**. Otherwise, click **Edit**.

    ![First-time connection configuration.](../image/adobe-sign-connection-configure.png)

5.  On the **Configure Connection** form, fill in the fields:

    |Field|Description|
    |-----|-----------|
    |Connection Information|
    |Name|Name to uniquely identify the connection record. This is auto-populated.|
    |Connection URL|URL to connection to the Adobe Sign account in this format: `https://api.<region>.echosign.com`.|
    |Credential Information|
    |Auth URL|OAuth authorization code endpoint. For example, `https://secure.<region>.echosign.com/public/oauth/v2`.|
    |Token URL|OAuth server token endpoint. For example, `https://secure.<region>.echosign.com/oauth/v2/token`.|
    |Refresh Token URL|URL to refresh a token. For example, `https://secure.<region>.echosign.com/oauth/v2/refresh`.|
    |OAuth Client ID|Application ID created during the Adobe Sign account configuration.|
    |OAuth Client Secret|Application Secret created during the Adobe Sign account configuration.|
    |OAuth Redirect URL|OAuth callback endpoint in this format: `https://<ServiceNow-instance-name>.service-now.com/oauth_redirect.do`|

    ![Configure a connection for the Adobe Sign spoke.](../image/adobe-sign-connection-template.png)

6.  Click **Configure and Get OAuth Token**.

    The spoke connection is configured.


## Configure Application Access to ServiceNow tables

Allow Adobe Sign spoke to create group admin user role when an Adobe Sign group is synchronized with ServiceNow tables by configuring the application access of the required ServiceNow tables.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Tables**.

2.  For each of the following tables, ensure that the **Can read**,**Can create**, and **Can update** options are selected in the Application Access related list.

    |Label|Name|
    |-----|----|
    |Role|sys\_user\_role|
    |Access Control|sys\_security\_acl|
    |Access Roles|sys\_security\_acl\_role|
    |Application Menu|sys\_app\_application|
    |Module|sys\_app\_module|

3.  Click **Update**.


### Result

Application access of the required ServiceNow tables is configured.

## Create Adobe Sign group in ServiceNow

Synchronize ServiceNow with the required group in Adobe Sign by creating a record in the AdobeSign Group Details \[sn\_adobesign\_spoke\_adobesign\_group\_details\] table.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Adobe Sign Spoke** &gt; **Groups**.

2.  Click **New**.

3.  On the form, fill in the fields.

    | | |
    |---|---|
    |Group Name|Name to uniquely identify the Adobe Sign group. For example, `Legal`.|
    |Group ID|Unique ID associated with the record.|
    |Connection Alias|Connection alias created to synchronize the Adobe Sign group with ServiceNow.|


### Result

The required Adobe Sign group is created in ServiceNow and can be managed from the Adobe Sign spoke.

User role specific to the group is created in ServiceNow, when the group is created in the ServiceNow instance. For example, a HR group user role, sn\_adobesign\_spoke.HR, is created when the HR group is created in ServiceNow. ServiceNow admin can assign these group user roles to users and control access to the group-specific information such as:

-   Documents and agreements
-   Connection and credential aliases
-   Credential records
-   Application registries
-   Data in tables of the Adobe Sign spoke

Only ServiceNow admin has access to information about all Adobe Sign groups that are synchronised with the ServiceNow instance.

## Synchronize documents in Adobe Sign group with ServiceNow

Synchronize ServiceNow with the required group in Adobe Sign to access the documents and agreements that are specific to the group, from the Adobe Sign spoke.

### Before you begin

Role required: admin

### About this task

Ensure that the groups are setup and configured with their respective connection and credential aliases before synchronizing the group documents.

### Procedure

1.  Navigate to **All** &gt; **Adobe Sign Spoke** &gt; **Documents**.

    The AdobeSign Documents \[sn\_adobesign\_spoke\_adobe\_sign\_documents\] table opens.

2.  Click the Get Documents related list.

    **Note:**

    -   If you have logged in as an admin, you can synchronize the documents of all Adobe Sign groups.
    -   If you have logged in as a group admin, you can synchronize only those documents that are specific to your Adobe Sign groups.

### Result

Details of all documents specific to the required Adobe Sign groups are synchronized with ServiceNow.

