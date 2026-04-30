---
title: Set up the Microsoft Azure Artifacts spoke
description: Integrate the ServiceNow instance and Microsoft Azure Artifacts using Basic Authentication to authenticate ServiceNow requests.Create and record the personal access tokens in your Microsoft Azure portal. The personal access tokens are required to authenticate ServiceNow requests.Add and configure a Microsoft Azure Artifacts connection to authenticate ServiceNow requests.
locale: en-US
release: yokohama
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Microsoft Azure Artifacts Spoke, Integration Hub available spokes, Building integrations in Integration Hub, Integration Hub, Data and Automation]
---

# Set up the Microsoft Azure Artifacts spoke

Integrate the ServiceNow instance and Microsoft Azure Artifacts using Basic Authentication to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Microsoft Azure Artifacts spoke.
-   Create a Personal Access Token in your Azure Devops account and record it for later use.
-   Role required: admin.

## Obtain the personal access token

Create and record the personal access tokens in your Microsoft Azure portal. The personal access tokens are required to authenticate ServiceNow requests.

### Before you begin

Role required: admin

### Procedure

1.  Log in to your Azure Artifacts portal as an admin.

2.  Navigate to **User Settings** &gt; **Personal access tokens**.

3.  Click **New Token**.

4.  On the form, fill the required fields.

5.  Click **Create**.

    The token is displayed.

6.  Copy and record the value of token for later use.


## Configure a connection for Microsoft Azure Artifacts spoke

Add and configure a Microsoft Azure Artifacts connection to authenticate ServiceNow requests.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Under **Connections**, toggle and enable the **Outbound** connections.

4.  Locate the alias for **sn\_ms\_artfcts\_spke** and click **View Details**.

    -   To configure the default connection and credential alias record that is shipped along with the Microsoft Azure Artifacts spoke, click **View Details**.
    -   To manage more than one Microsoft Azure Artifacts spoke connection records, you should create a new child alias record by clicking Add Connection. For more information about using multiple connections, see [Supporting multiple connections](../../integrationhub/concept/support-multiple-connections.md).
    If you are configuring the spoke for the first time, click **Configure**. Otherwise, click **Edit**.

5.  On the **Configure Connection** form, fill in the fields:

    |Field|Description|
    |-----|-----------|
    |Connection Name|Name to uniquely identify the connection record. For example, enter `Microsoft Azure Artifacts Connection`.|
    |Connection URL|URL of the Microsoft Azure Artifacts instance. For example, enter the URL in this format: `https://feeds.dev.azure.com/`|
    |Credential Name|Name to uniquely identify the credential record. For example, enter `Microsoft Azure Artifacts Credential`.|
    |User Name|User name to log in to your Azure Artifacts instance.|
    |Password|Personal access token to authenticate Azure Artifacts.|

6.  Click **Configure Connection**.

    The connection for the Microsoft Azure Artifacts spoke is created.

7.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

8.  Open the `Microsoft Azure Artifacts` Connection and Credential type.

9.  From the `Connections` tab, open the Credential record which is created from the connection template.

10. Click the lock icon beside the **Credential alias** field.

11. Search for `sn_ms_artfcts_spke.Microsoft_Azure_Project` and select it from the list.

12. Save the record.


### Result

The Microsoft Azure Artifacts spoke connection is configured and ready to be used.

