---
title: Set up the Jira Service Management spoke
description: Integrate the ServiceNow instance and Jira Service Management by using the Basic Auth credentials to authenticate ServiceNow requests.Integrate the ServiceNow instance with your Jira Service Management account using OAuth to authenticate ServiceNow requests.Obtain the value of Cloud ID of the Jira Cloud instance. This value is required during the configuration of the connection record in your ServiceNow instance.Add and configure a Jira Service Management connection to authenticate ServiceNow requests in a Jira Service Management spoke.Integrate the ServiceNow instance and Jira Service Management by using the Basic Auth credentials to authenticate ServiceNow requests.Generate an Atlassian account API token to authenticate requests for spokes associated with an Atlassian account.Create a credential record for the Jira account. The Jira Service Management spoke connection and credential alias uses this credential to authorize actions.Create a connection record for the Jira account. The connection and credential alias uses this connection to perform actions in Jira Service Management.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/integrate-applications/integration-hub/setup-jira-serv-mgmt.html
release: zurich
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Jira Service Management Spoke, Integration Hub spokes, Build integrations, Integration Hub, Workflow Data Fabric]
---

# Set up the Jira Service Management spoke

Integrate the ServiceNow instance and Jira Service Management by using the Basic Auth credentials to authenticate ServiceNow requests.

## Before you begin

-   Request an Integration Hub subscription.
-   Activate the Jira Service Management spoke.
-   Role required: admin.

## Option 1: Using OAuth authentication

Integrate the ServiceNow instance with your Jira Service Management account using OAuth to authenticate ServiceNow requests.

### Before you begin

Role required: admin

### Obtain the value of Cloud ID

Obtain the value of Cloud ID of the Jira Cloud instance. This value is required during the configuration of the connection record in your ServiceNow instance.

#### Before you begin

Role required: admin

#### Procedure

1.  Log in to [Atlassian Administration](https://admin.atlassian.com/) as an admin.

2.  Click **Select** against the required organization.

3.  From the **Jira Software** product, click **Manage product access**.

    A new window is opened and the URL is in this format: `https://admin.atlassian.com/s/<Cloud-ID>/apps`.

4.  Copy the value of the Cloud ID for later use.


### Configure a connection for a Jira Service Management spoke

Add and configure a Jira Service Management connection to authenticate ServiceNow requests in a Jira Service Management spoke.

#### Before you begin

Role required: admin

#### Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  Click the **Integrations** tab.

3.  Under **Connections**, the **Outbound** connections are displayed by default.

4.  Locate the **Jira\_SM** connection alias and click **View Details**.

    -   To configure the default connection and credential alias record that is shipped along with the Jira Service Management spoke, click **View Details**.
    -   To manage more than one Jira Service Management spoke connection records, you should create a new child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/integration-hub/support-multiple-connections.md).
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


## Option 2: Using Atlassian API token

Integrate the ServiceNow instance and Jira Service Management by using the Basic Auth credentials to authenticate ServiceNow requests.

### Before you begin

**Important:** Apps that collect API tokens to create individual 3LO apps don't comply with Atlassian security requirements for cloud apps and Atlassian acceptable use policy.

Role required: admin

### Generate an Atlassian account API token

Generate an Atlassian account API token to authenticate requests for spokes associated with an Atlassian account.

#### Before you begin

Make sure you have an Atlassian account.

Role required: Atlassian administrator credentials

#### About this task

Complete these steps from your Atlassian account. See the [Atlassian Developer](https://developer.atlassian.com/docs/) portal documentation for instructions on generating your API token.

**Note:** This procedure is applicable only if you're using the Jira Cloud subscription.

#### Procedure

1.  Log in to [Atlassian Start](https://start.atlassian.com/) as an admin.

2.  Go to your account profile photo and select **Account Settings**.

    \[Omitted image "jira-basic-settings.png"\] Alt text: Atlassian Start page with the drop down menu of the selected profile picture. Account Settings option emphasized.

3.  Go to **Security**.

4.  In the API token section, select **Create and manage API tokens**.

5.  Select **API token**.

6.  On the form, provide an integration name for the **Label** field.

7.  Select **Create**.

    \[Omitted image "jira-token.png"\] Alt text: The Create an API token modal with the Create button emphasized.

    The API token is generated.

8.  Select **Copy** and record the value of the API token for later use.

    \[Omitted image "jira-api-token.png"\] Alt text: Confirmation modal of Your new API token with the Copy button emphasized.


#### What to do next

Use your API token to configure the cloud connection for a Jira or Jira Service Management spoke.

### Create credential record for the Jira Service Management spoke

Create a credential record for the Jira account. The Jira Service Management spoke connection and credential alias uses this credential to authorize actions.

#### Before you begin

Role required: admin

#### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

    The system displays the message `What type of Credentials would you like to create?`

3.  Select **Basic Auth Credentials**.

4.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Name|Name to identify the credential record for the Jira Service Management spoke. For example, `Jira SM Basic Auth Token cred`.|
    |User name|Enter the email address of the user.|
    |API Key|Enter the API token you generated for your Jira Cloud instance.|

5.  Right-click the form header and click **Save**.


### Create a connection record for the Jira Service Management spoke

Create a connection record for the Jira account. The connection and credential alias uses this connection to perform actions in Jira Service Management.

#### Before you begin

Role required: admin

#### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Open the alias record **Jira\_SM** that shipped with the spoke.

3.  On the **Connections** tab, click **New**.

    The system displays a blank HTTP\(s\) Connection form.

4.  Enter these values and click **Submit**.

<table id="table_vsw_lkv_4fb"><thead><tr><th>

Field

</th><th>

Value required

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter any name to uniquely identify the connection record. For example, enter `Jira cloud Basic Auth Token Connection`.

</td></tr><tr><td>

Credential

</td><td>

Select the Credential record created for Jira. For example, select **Jira SM Basic Auth Token cred**.

</td></tr><tr><td>

Connection URL

</td><td>

Enter the URL of your Jira instance in this format: `https://api.atlassian.com/ex/jira/<Cloud-ID>`.For information about obtaining the value of Cloud ID, see [Obtain the value of Cloud ID](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/integrate-applications/integration-hub/setup-jira-spk-opt2.md).

</td></tr></tbody>
</table>5.  Click **Submit**.

    The Jira Service Management spoke is configured to use basic credentials via the service account.


