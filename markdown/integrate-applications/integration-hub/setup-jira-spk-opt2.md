---
title: Set up the Jira spoke for Jira Cloud
description: Integrate your ServiceNow instance with the Jira Cloud instance to authenticate the requests from ServiceNow.Integrate the ServiceNow instance with your Jira account using OAuth to authenticate ServiceNow requests.Obtain the value of Cloud ID of the cloud instance. This value is required during the configuration of the connection record in your ServiceNow instance.Add and configure a Jira connection to authenticate ServiceNow requests in Jira spoke.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/integration-hub/setup-jira-spk-opt2.html
release: brazil
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-09-02"
reading_time_minutes: 2
breadcrumb: [Jira Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Jira spoke for Jira Cloud

Integrate your ServiceNow instance with the Jira Cloud instance to authenticate the requests from ServiceNow.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Jira spoke.
-   Role required: admin.

## About this task

**Important:**

Starting with the Australia release, instructions for generating and using API tokens have been removed from our documentation to align with Atlassian's Acceptable Use Policy. See the Atlassian blog, [Building Secure and Scalable Integrations: Our Guidance for Third-Party Apps](https://www.atlassian.com/blog/developer/building-secure-and-scalable-integrations-our-guidance-for-third-party-apps) for more information.

## Option 1: Using OAuth authentication \(Authorization Code grant type\)

Integrate the ServiceNow instance with your Jira account using OAuth to authenticate ServiceNow requests.

### Before you begin

Role required: admin.

### Obtain the value of Cloud ID

Obtain the value of Cloud ID of the cloud instance. This value is required during the configuration of the connection record in your ServiceNow instance.

#### Before you begin

Role required: admin

#### Procedure

1.  Log in to [Atlassian Administration](https://admin.atlassian.com/) as an admin.

2.  Click **Select** against the required organization.

3.  From the **Jira Software** product, click **Manage product access**.

    A new window is opened and the URL is in this format: `https://admin.atlassian.com/s/<Cloud-ID>/apps`.

4.  Copy the value of the Cloud ID for later use.


### Configure a connection for Jira spoke

Add and configure a Jira connection to authenticate ServiceNow requests in Jira spoke.

#### Before you begin

Role required: admin

#### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Under **Connections**, the **Outbound** connections are displayed by default.

4.  Locate the **Jira** connection alias and click **View Details**.

    -   To configure the default connection and credential alias record that is shipped along with the Jira spoke, click **View Details**.
    -   To manage more than one Jira spoke connection records, you should create a new child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/integrate-applications/integration-hub/support-multiple-connections.md).
    If you are configuring the spoke for the first time, click **Configure**. Otherwise, click **Edit**.

5.  On the **Connection** form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Connection Name|Name to uniquely identify the connection. For example, `Jira Spoke OAuth basic conn`.|
    |Connection URL|URL of your Jira instance in this format: `https://api.atlassian.com/ex/jira/{cloud-id}/`. Replace `{cloud-id}` with value of the Cloud ID you had obtained previously.|
    |Scopes|By default, these scopes are provided `read:jira-work, read:jira-user, write:jira-work, manage:jira-project, manage:jira-configuration, manage:jira-webhook, manage:jira-data-provider, delete:sprint:jira-software, read:sprint:jira-software, write:sprint:jira-software, read:board-scope:jira-software, read:project:jira, read:jql:jira, read:issue-details:jira, read:me, read:account, offline_access`. You can modify the scopes as per your requirement.|

    \[Omitted image "jira-new-conf-temp.jpg"\] Alt text:

6.  Click **Save and Get OAuth Token**.


