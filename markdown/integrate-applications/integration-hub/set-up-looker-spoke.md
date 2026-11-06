---
title: Setting up the Looker spoke
description: Integrate the ServiceNow instance and Looker by using Looker credentials to authenticate ServiceNow requests.Configure API key settings to manage and retrieve Looker API keys.Configure a connection to your Looker account. The Looker spoke connection and credential aliases use these connections to perform actions in Looker.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/integrate-applications/integration-hub/set-up-looker-spoke.html
release: australia
product: Integration Hub
classification: integration-hub
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Looker Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Setting up the Looker spoke

Integrate the ServiceNow instance and Looker by using Looker credentials to authenticate ServiceNow requests.

## Configure Looker API key settings

Configure API key settings to manage and retrieve Looker API keys.

### Before you begin

-   Request an Integration Hub subscription.
-   Activate the Looker spoke.
-   Role required: Looker admin.

### Procedure

1.  Navigate to your Looker \(https://&lt;instancename&gt;.looker.com/\) instance.

2.  Select the gear icon to open Admin settings.

3.  Select **Users** &gt; **Open the admin user account**.

4.  Select **Edit API3 Keys** under the Profile tab.

5.  Select **New API3 Key**.

6.  Copy the Client ID and Client secret for later use.


## Configure a connection for the Looker spoke

Configure a connection to your Looker account. The Looker spoke connection and credential aliases use these connections to perform actions in Looker.

### Before you begin

Role required: admin.

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Under **Connections**, toggle and enable the **Outbound** connections.

4.  Locate the alias for **Looker** and click **View Details**.

    -   To configure the default connection and credential alias record that is shipped along with the Looker spoke, click **View Details**.

        \[Omitted image "looker-connection.png"\] Alt text: Connection for the Looker spoke with View Details highlighted.

    -   To manage more than one Looker spoke connection records, you should create a new child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/integrate-applications/integration-hub/support-multiple-connections.md).
    If you are configuring the spoke for the first time, click **Configure**. Otherwise, click **Edit**.

    \[Omitted image "looker-connection-conf.png"\] Alt text: Initial connection configuration with Configure highlighted.

5.  On the form, fill in these fields:

    |Field|Value required|
    |-----|--------------|
    |Connection Information|
    |Connection Name|Name to identify the Looker connection record.|
    |Connection URL|URL of your Looker instance in this format: `https://<instance_name>.looker.com`. Replace `<instance_name>` with the name of your Looker instance.|
    |Credential Information|
    |OAuth Client ID|Client ID of your Looker API key.|
    |OAuth Client Secret|Client secret of your Looker API key.|
    |OAuth Redirect URL|Redirect URL of your ServiceNow instance in this format: `https://<instance-name>.service-now.com/oauth_redirect.do`.|

    \[Omitted image "looker-conf-temp.png"\] Alt text: Configure a connection for the Looker spoke.

6.  Click **Save and Get OAuth Token**.


### Result

The Looker spoke connection is configured and ready to be used.

