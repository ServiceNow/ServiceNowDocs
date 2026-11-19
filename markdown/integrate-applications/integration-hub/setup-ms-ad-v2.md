---
title: Set up the Microsoft Active Directory v2 spoke
description: Integrate the ServiceNow instance and the Microsoft Active Directory v2 spoke by using the Windows credentials to authenticate ServiceNow requests.Configure a connection record to connect to the Microsoft Active Directory v2 spoke host and enable the Microsoft Active Directory v2 spoke connections and credentials alias to authorize actions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/integration-hub/setup-ms-ad-v2.html
release: brazil
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Microsoft Active Directory v2 Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Microsoft Active Directory v2 spoke

Integrate the ServiceNow instance and the Microsoft Active Directory v2 spoke by using the Windows credentials to authenticate ServiceNow requests.

\[Omitted video\] Description: Demonstrates setting up the Microsoft Active Directory v2 spoke.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Microsoft Active Directory v2 spoke.
-   Role required: admin

## Configure a connection for the Microsoft Active Directory v2 spoke

Configure a connection record to connect to the Microsoft Active Directory v2 spoke host and enable the Microsoft Active Directory v2 spoke connections and credentials alias to authorize actions.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Under **Connections**, toggle and enable the **Outbound** connections.

4.  Locate the **AD\_v2** connection alias and click **View Details**.

    -   To configure the default connection and credential alias record that is shipped along with the Microsoft Active Directory v2 spoke, click **View Details**.

        \[Omitted image "click-add-connection-ad-v2.png"\] Alt text: Configure connection and credentials for Microsoft Active Directory v2.

    -   To manage more than one Microsoft Active Directory v2 spoke connection records, you should create a new child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/integration-hub/support-multiple-connections.md).
    If you are configuring the spoke for the first time, click **Configure**. Otherwise, click **Edit**

    \[Omitted image "configure-def-alias-adv2.png"\] Alt text: Configure the default alias.

5.  Enter the following details in the form.

    |Field|Description|
    |-----|-----------|
    |Connection Information|
    |Connection Name|Name to uniquely identify the record.|
    |Host|Fully qualified domain name or IP address of the domain controller where the Microsoft Active Directory is installed. For example, `<host>.<domain>.com`.|
    |Credential Information|
    |User Name|User name for outbound authentication in `domain\username` format.|
    |Password|Password for the account.|

    \[Omitted image "create-connection-form.png"\] Alt text: Configure connection form.

6.  Click **Save**.


### Result

The spoke connection is configured and ready to be used.

### What to do next

To use the spoke actions, your instance must have a MID Server set up and configured to use PowerShell. For more information about running actions on the MID Server, see [Integration steps](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/integration-hub/integration-steps.md). For more information about the MID Server, see [MID Server](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/servicenow-platform/mid-server-landing.md).

To set up the MID Server for this spoke, see [Set up MID Server for a spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/integration-hub/config-adv-mid-settings-for-oauth-on-mid.md).

**Note:** You must install the MID Server and Microsoft Active Directory on different servers.

