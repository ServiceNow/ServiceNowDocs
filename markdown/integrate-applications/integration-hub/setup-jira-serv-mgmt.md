---
title: Set up the Jira Service Management spoke
description: Integrate the ServiceNow instance and Jira Service Management by using OAuth 2.0 to authenticate ServiceNow requests.Generate an Atlassian account API token to authenticate requests for spokes associated with an Atlassian account.Add and configure a Jira Service Management connection to authenticate ServiceNow requests in a Jira Service Management spoke.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/integration-hub/setup-jira-serv-mgmt.html
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

## Generate an Atlassian account API token

Generate an Atlassian account API token to authenticate requests for spokes associated with an Atlassian account.

### Before you begin

Make sure you have an Atlassian account.

Role required: Atlassian administrator credentials

### About this task

Complete these steps from your Atlassian account. See the [Atlassian Developer](https://developer.atlassian.com/docs/) portal documentation for instructions on generating your API token.

**Note:** This procedure is applicable only if you are using the Jira Cloud subscription.

### Procedure

1.  Log in to [Atlassian Start](https://start.atlassian.com/) as an admin.

2.  Go to your account profile photo and select **Account Settings**.

    \[Omitted image "jira-basic-settings.png"\] Alt text: Atlassian Start page with the drop down menu of the selected profile picture. Account Settings option emphasized.

3.  Go to **Security**.

4.  In the API token section, select **Create and manage API tokens**.

5.  Click **Create API token**.

6.  On the form, provide an integration name for the **Label** field.

7.  Click **Create**.

    \[Omitted image "jira-token.png"\] Alt text: The Create an API token modal with the Create button emphasized.

    The API token is generated.

8.  Click **Copy** and record the value of the API token for later use.

    \[Omitted image "jira-api-token.png"\] Alt text: Confirmation modal of Your new API token with the Copy button emphasized.


### What to do next

Use your API token to configure the cloud connection for the Jira spoke.

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
    -   To manage more than one Jira Service Management spoke connection records, you should create a new child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/support-multiple-connections.md).
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
</table>    \[Omitted image "jira-sm-conn-temp.jpg"\] Alt text:

6.  Click **Save and Get OAuth Token**.


