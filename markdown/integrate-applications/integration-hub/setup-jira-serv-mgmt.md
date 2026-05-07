---
title: Set up the Jira Service Management spoke
description: Integrate the ServiceNow instance and Jira Service Management by using OAuth 2.0 to authenticate ServiceNow requests.Obtain the value of Cloud ID of the Jira Cloud instance. This value is required during the configuration of the connection record in your ServiceNow instance.Add and configure a Jira Service Management connection to authenticate ServiceNow requests in a Jira Service Management spoke.
locale: en-US
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Jira Service Management Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Jira Service Management spoke

Integrate the ServiceNow instance and Jira Service Management by using OAuth 2.0 to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Jira Service Management spoke.
-   Role required: admin.

## About this task

**Important:**

Starting with the Australia release, instructions for generating and using API tokens have been removed from our documentation to align with Atlassian's Acceptable Use Policy. See the Atlassian blog, [Building Secure and Scalable Integrations: Our Guidance for Third-Party Apps](https://www.atlassian.com/blog/developer/building-secure-and-scalable-integrations-our-guidance-for-third-party-apps) for more information.

## Obtain the value of Cloud ID

Obtain the value of Cloud ID of the Jira Cloud instance. This value is required during the configuration of the connection record in your ServiceNow instance.

### Before you begin

Role required: admin

### Procedure

1.  Log in to [Atlassian Administration](https://admin.atlassian.com/) as an admin.

2.  Click **Select** against the required organization.

3.  From the **Jira Software** product, click **Manage product access**.

    A new window is opened and the URL is in this format: `https://admin.atlassian.com/s/<Cloud-ID>/apps`.

4.  Copy the value of the Cloud ID for later use.


## Configure a connection for the Jira Service Management spoke

Add and configure a Jira Service Management connection to authenticate ServiceNow requests in a Jira Service Management spoke.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Under **Connections**, the **Outbound** connections are displayed by default.

4.  Locate the **Jira\_SM** connection alias and click **View Details**.

    -   To configure the default connection and credential alias record that is shipped along with the Jira Service Management spoke, click **View Details**.
    -   To manage more than one Jira Service Management spoke connection records, you should create a new child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](../../integrationhub/concept/support-multiple-connections.md).
    If you are configuring the spoke for the first time, click **Configure**. Otherwise, click **Edit**.

5.  On the **Connection** form, fill in the fields.

<table id="table_tfv_3d5_h5b"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Name to uniquely identify the connection. For example, `Jira Spoke OAuth basic conn`.

</td></tr><tr><td>

Connection URL

</td><td>

URL of your Jira instance in this format: `https://api.atlassian.com/ex/jira/{cloud-id}/`. Replace `{cloud-id}` with value of the Cloud ID you had obtained previously.

</td></tr><tr><td>

Scopes

</td><td>

By default, these scopes are provided `read:jira-user, read:servicedesk-request, write:servicedesk-request, manage:servicedesk-customer, read:jira-work, read:me, read:account, offline_access`. You can modify the scopes as per your requirement.**Note:** After the scopes are modified and saved, whenever you edit the connection record, the scopes are reset to the default scopes.

</td></tr></tbody>
</table>    ![](../image/jira-sm-conn-temp.jpg)

6.  Click **Save and Get OAuth Token**.


