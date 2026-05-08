---
title: Connecting Agile Development 2.0 and Azure DevOps
description: Establish a connection between Agile Development 2.0 and Azure DevOps using a connection alias and an Azure DevOps instance.Create a Basic Auth credential and an HTTP\(s\) connection which will together be used as a connection alias to establish a connection with Azure DevOps.Create an Azure DevOps instance record using the connection alias that you created. This instance is used to establish an integration between Agile Development 2.0 and Azure DevOps.Connect Azure DevOps with Agile Development 2.0 to enable the integration.
locale: en-US
release: australia
product: Microsoft Azure DevOps Integrations Comm
classification: microsoft-azure-devops-integrations-comm
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Setting up the integration between Microsoft Azure DevOps and Agile Development 2.0, Microsoft Azure DevOps Integration for Agile Development, Strategic Portfolio Management]
---

# Connecting Agile Development 2.0 and Azure DevOps

Establish a connection between Agile Development 2.0 and Azure DevOps using a connection alias and an Azure DevOps instance.

**Parent Topic:**[Setting up the integration between Microsoft Azure DevOps and Agile Development 2.0](../concept/setting-up-agile-azure-integration.md)

## Create an Azure DevOps connection alias

Create a Basic Auth credential and an HTTP\(s\) connection which will together be used as a connection alias to establish a connection with Azure DevOps.

### Before you begin

Roles required:

-   admin to create a connection and credential alias
-   sn\_ado\_int.admin or sn\_ado\_int.user to create basic authorization credentials and HTTP\(s\) connection

### Procedure

1.  Create a Connection &amp; Credential alias

    -   A connection alias \(sn\_ado\_int.Azure\_DevOps\) is available by default.
    -   You must create a connection alias for every Azure DevOps organization that you use.
2.  Use OAuth 2.0 or Basic Auth to create credentials.

    -   OAuth 2.0: See Set up the Microsoft Azure DevOps Boards spoke using OAuth.

        **Important:** Make sure to specify a username in the OAuth 2.0 Credentials \[oauth\_2\_0\_credentials\] table for the Credential Alias record. This username must correspond to the service account used to interact with Azure DevOps.

    -   Basic Authentication: See Basic authentication credentials.

        **Note:** When creating Basic Auth credentials, use the details of your personal access token in Azure DevOps.

        -   Set the **Password** field of the basic authentication credential as the personal access token in Azure DevOps.
        -   Set the **User Name** field of the basic authentication credential as the username used to create the personal access token in Azure DevOps.

            If your login is in the format of **domainname\\username**, use only the **username**.

3.  Create Create an HTTP\(s\) connection.


### What to do next

[Create an Azure DevOps instance](connect-sn-agile-with-azure.md#)

.

## Create an Azure DevOps instance

Create an Azure DevOps instance record using the connection alias that you created. This instance is used to establish an integration between Agile Development 2.0 and Azure DevOps.

### Before you begin

Role required: sn\_ado\_int.admin or sn\_ado\_int.user

### Procedure

1.  Navigate to **All** &gt; **Agile Azure DevOps Integration** &gt; **Azure DevOps Instances**.

2.  Click **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the Azure DevOps instance. Enter a name of your choice.|
    |Connection Alias|Azure DevOps connection alias that you already created. Use the lookup \(![Lookup icon](../../project-workspace/image/lookup_icon.png)\) option to select your connection alias.|
    |Version|Azure DevOps version. Use the lookup \(![Lookup icon](../../project-workspace/image/lookup_icon.png)\) option to select your Azure DevOps version.|

4.  Click **Submit**.


### What to do next

[Connect to Azure DevOps](connect-sn-agile-with-azure.md#)

.

## Connect to Azure DevOps

Connect Azure DevOps with Agile Development 2.0 to enable the integration.

### Before you begin

Role required: sn\_ado\_int.user

### Procedure

1.  Navigate to **All** &gt; **Agile Azure DevOps Integration** &gt; **Azure DevOps Instances**.

2.  Open your Azure DevOps instance record.

3.  Click **Connect**.


### Result

If the **State** field on the Azure DevOps Instance record shows:

-   **Connected**, the connection is successful.
-   **Not connected**, the connection could not be established. You can view the reason for the failure in the error message.

### What to do next

[Discover and import Azure DevOps projects](../task/discover-import-azure-projects.md)

.

