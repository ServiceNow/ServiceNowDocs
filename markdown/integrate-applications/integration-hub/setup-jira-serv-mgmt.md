---
title: Set up the Jira Service Management spoke
description: Integrate the ServiceNow instance and Jira Service Management by using the Basic Auth credentials to authenticate ServiceNow requests.Generate an Atlassian account API token to authenticate requests for spokes associated with an Atlassian account.Add and configure a Jira Service Management connection to authenticate ServiceNow requests in a Jira Service Management spoke.
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

Integrate the ServiceNow instance and Jira Service Management by using the Basic Auth credentials to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Jira Service Management spoke.
-   Role required: admin.

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

    ![Atlassian Start page with the drop down menu of the selected profile picture. Account Settings option emphasized.](../image/jira-basic-settings.png)

3.  Go to **Security**.

4.  In the API token section, select **Create and manage API tokens**.

5.  Click **Create API token**.

6.  On the form, provide an integration name for the **Label** field.

7.  Click **Create**.

    ![The Create an API token modal with the Create button emphasized.](../image/jira-token.png)

    The API token is generated.

8.  Click **Copy** and record the value of the API token for later use.

    ![Confirmation modal of Your new API token with the Copy button emphasized.](../image/jira-api-token.png)


### What to do next

Use your API token to configure the cloud connection for the Jira spoke.

## Configure a connection for a Jira Service Management spoke

Add and configure a Jira Service Management connection to authenticate ServiceNow requests in a Jira Service Management spoke.

### Before you begin

Role required: admin

### Procedure

1.  Navigate to **Process Automation** &gt; **Workflow Studio**.

2.  Select **Integrations**.

3.  Select the **Connections** tab.

4.  Use the search box to find the **Jira\_SM** connection alias.

5.  Select **View Details**.

    ![Jira Service Management alias.](../image/jira-sm-alias.png)

6.  Configure a cloud connection.

    1.  Add or edit a cloud connection.

        -   To set up an existing connection, select **Configure** or **Edit**.

            ![Jira Service Management connection button.](../image/jira-sm-alias-configure.png)

        -   To create and configure a new connection, select **Add Connection**.

        **Note:** To support multiple connections through a spoke, see [Supporting multiple connections](../../integrationhub/concept/support-multiple-connections.md).

    2.  On the configuration form, fill in the fields for a cloud connection.

<table id="table_hhb_hxk_nzb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

For example, `jira_sm_cloud_conn`.

</td></tr><tr><td>

Connection URL

</td><td>

The instance URL in this format: `<provider-domain-name>.atlassian.net`.

</td></tr><tr><td>

User Name

</td><td>

Your Atlassian admin account email address.

</td></tr><tr><td>

Password

</td><td>

The API token generated in [Generate an Atlassian account API token](setup-jira-serv-mgmt.md#).

</td></tr></tbody>
</table>        ![Jira Service Management connection form.](../image/jira-sm-connection-form.png)

    3.  Confirm your configuration.

        -   For an existing connection, select **Edit Connection**.
        -   For a new connection, select **Create Connection**.
    4.  Repeat these steps for a server connection with the following information.

<table id="table_tfv_3d5_h5b"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

For example, `jira_sm_server_conn`.

</td></tr><tr><td>

Connection URL

</td><td>

The Jira server instance URL.

</td></tr><tr><td>

User Name

</td><td>

The admin user's user name.

</td></tr><tr><td>

Password

</td><td>

The admin user's password.

</td></tr></tbody>
</table>
