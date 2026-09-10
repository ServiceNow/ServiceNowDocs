---
title: Set up the Confluence Cloud spoke
description: Integrate the ServiceNow instance and Confluence Cloud by creating a custom OAuth 2.0 application in Confluence Cloud to authenticate ServiceNow requests.Obtain the value of Cloud ID of the cloud instance. This value is required during the configuration of the connection record in your ServiceNow instance.Add and configure a Confluence Cloud connection to authenticate ServiceNow requests in Confluence Cloud spoke.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/integration-hub/setup-confluence-cloud.html
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Confluence Cloud Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Confluence Cloud spoke

Integrate the ServiceNow instance and Confluence Cloud by creating a custom OAuth 2.0 application in Confluence Cloud to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Confluence Cloud spoke.
-   Atlassian role required: site admin
-   Role required: admin.

## Obtain the value of Cloud ID

Obtain the value of Cloud ID of the cloud instance. This value is required during the configuration of the connection record in your ServiceNow instance.

### Before you begin

Role required: admin

### Procedure

1.  Log in to [Atlassian Administration](https://admin.atlassian.com/) as an admin.

2.  Click **Select** against the required organization.

3.  From the **Jira Software** product, click **Manage product access**.

    A new window is opened and the URL is in this format: `https://admin.atlassian.com/s/<Cloud-ID>/apps`.

4.  Copy the value of the Cloud ID for later use.


## Configure a connection for the Confluence spoke

Add and configure a Confluence Cloud connection to authenticate ServiceNow requests in Confluence Cloud spoke.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Under **Connections**, the **Outbound** connections are displayed by default.

4.  Locate the **Confluence Cloud** connection alias and click **View Details**.

    -   To configure the default connection and credential alias record that is shipped along with the Confluence Cloud spoke, click **View Details**.
    -   To manage more than one Confluence Cloud spoke connection records, you should create a new child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/support-multiple-connections.md).
    If you are configuring the spoke for the first time, click **Configure**. Otherwise, click **Edit**.

5.  On the **Connection** form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Connection Name|Name to uniquely identify the connection. For example, `Confluence Cloud Spoke Connection`.|
    |Connection URL|URL of the Atlassian API endpoint: `https://api.atlassian.com/ex/jira/{cloud-id}/`. Replace `{cloud-id}` with value of the Cloud ID you had obtained previously.|
    |Scopes|By default, these scopes are provided: `ace:confluence, read:page:confluence, search:confluence, read:confluence-groups, write:confluence-groups, read:confluence-user, read:me, read:account, offline_access`. You can modify the scopes as per your requirement.|

    \[Omitted image "confluence-cloud-spoke-conn-config.png"\] Alt text: Create a connection for Confluence Cloud spoke using connection template

6.  Click **Save and Get OAuth Token**.


