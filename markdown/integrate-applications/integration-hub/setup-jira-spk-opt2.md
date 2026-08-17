---
title: Set up the Jira spoke for Jira Cloud
description: Integrate your ServiceNow instance with the Jira Cloud instance to authenticate the requests from ServiceNow.Integrate the ServiceNow instance with your Jira account using OAuth to authenticate ServiceNow requests.Create an OAuth 2.0 integration in Atlassian Developer console to authenticate the requests.Obtain the value of Cloud ID of the Jira Cloud instance. This value is required during the configuration of the connection record in your ServiceNow instance.Use the information generate while creating the OAuth 2.0 integration to create an application registry record in your ServiceNow instance.Create a credential record for the Jira account. The Jira spoke connection and credential alias uses this credential to authorize actions.Create a connection record for the Jira account. The connection and credential alias uses this connection to perform actions in Jira.Integrate the ServiceNow instance and Jira Cloud instance using an API key to authenticate ServiceNow requests.Generate an Atlassian account API token to authenticate requests for spokes associated with an Atlassian account.Add and configure a Jira connection to authenticate ServiceNow requests in Jira spoke.Integrate the ServiceNow instance and Jira Cloud instance using an API key with scopes to authenticate ServiceNow requests.Generate an Atlassian account API token with the required scopes to authenticate requests for spokes associated with an Atlassian account.Add and configure a Jira connection to authenticate ServiceNow requests in Jira spoke.API token scopes needed to use the required spoke action are listed here.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/integrate-applications/integration-hub/setup-jira-spk-opt2.html
release: australia
product: Integration Hub
classification: integration-hub
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 17
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

### Create an OAuth 2.0 integration in Jira account

Create an OAuth 2.0 integration in Atlassian Developer console to authenticate the requests.

#### Before you begin

Role required: admin

#### Procedure

1.  Log in to [Atlassian Developer console](https://developer.atlassian.com/console/myapps/) as an admin.

2.  Under **My apps**, click **Create** and select **OAuth 2.0 integration**.

    \[Omitted image "jira-oauth-int.png"\] Alt text: Create an OAuth 2.0 integration.

3.  On the form, provide name of the integration and click **Create**.

    \[Omitted image "jira-create-oauth.png"\] Alt text: Provide integration name.

    The integration is created and the value of **App ID** is displayed.

4.  Click **Authorization**.

    1.  Click **Add** under **Action**.

        \[Omitted image "jira-auth-add.png"\] Alt text: Authorization to access APIs.

    2.  In **Callback URL**, provide URL of your ServiceNow instance in this format: `https://<ServiceNow-Instance-Name>.service-now.com/oauth_redirect.do`.

        For example, `https://example.service-now.com/oauth_redirect.do`

        \[Omitted image "jira-callback-url.png"\] Alt text: Add Callback URL.

    3.  Click **Save Changes**.

5.  Click **Settings**.

    Under **Authentication details**, copy the values of **Client ID** and **Client Secret**.

    \[Omitted image "jira-client-id.png"\] Alt text: Copy the values of Client ID and Client Secret.

6.  Click **Permissions**.

    1.  In **Classic scopes**, ensure that you select these scopes.

        -   manage:jira-configuration
        -   manage:jira-project
        -   manage:jira-webhook
        -   read:jira-work
        -   read:jira-user
        -   write:jira-work
    2.  In **Granular scopes**, ensure that you select these scopes.

        -   delete:sprint:jira-software
        -   read:issue-details:jira
        -   read:jql:jira
        -   read:sprint:jira-software
        -   write:sprint:jira-software
        -   read:board-scope:jira-software
        -   read:project:jira
    You can configure other scopes as per your requirement.


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


### Create an application registry in ServiceNow instance

Use the information generate while creating the OAuth 2.0 integration to create an application registry record in your ServiceNow instance.

#### Before you begin

Role required: admin

#### Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Click **New**.

    The system displays the message `What kind of OAuth application?`.

3.  Select **Connect to a third party OAuth Provider**.

4.  On the form, fill these values.

<table id="table_pcv_pfs_gwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to identify the application registry record. For example, `Jira cloud OAuth app registry`.

</td></tr><tr><td>

Client ID

</td><td>

Client ID generated when the OAuth 2.0 integration was created in Atlassian Developer console.

</td></tr><tr><td>

Client Secret

</td><td>

Client secret generated when the OAuth 2.0 integration was created in Atlassian Developer console.

</td></tr><tr><td>

Default Grant type

</td><td>

Grant type used to establish the token. Select **Authorization Code**.

</td></tr><tr><td>

Authorization URL

</td><td>

OAuth authorization code endpoint. Enter: `https://auth.atlassian.com/authorize`.

</td></tr><tr><td>

Token URL

</td><td>

OAuth server token endpoint. Enter: `https://auth.atlassian.com/oauth/token`.

</td></tr><tr><td>

Redirect URL

</td><td>

OAuth callback endpoint. System generates the URL upon saving the application registry.

</td></tr><tr><td>

Refresh Token URL

</td><td>

URL to refresh a token. Enter: `https://auth.atlassian.com/oauth/token`.**Note:** This field is hidden in the form layout. Configure the form layout to show this field.

</td></tr></tbody>
</table>5.  In the **OAuth Entity Scopes** tab, create these entity scope records.

    |Name|OAuth scope|
    |----|-----------|
    |`delete:sprint:jira-software`|`delete:sprint:jira-software`|
    |`manage:jira-configuration`|`manage:jira-configuration`|
    |`manage:jira-project`|`manage:jira-project`|
    |`manage:jira-webhook`|`manage:jira-webhook`|
    |`offline_access`|`offline_access`|
    |`read:issue-details:jira`|`read:issue-details:jira`|
    |`read:jira-user`|`read:jira-user`|
    |`read:jira-work`|`read:jira-work`|
    |`read:jql:jira`|`read:jql:jira`|
    |`read:sprint:jira-software`|`read:sprint:jira-software`|
    |`write:jira-work`|`write:jira-work`|
    |`write:sprint:jira-software`|`write:sprint:jira-software`|
    |`read:board-scope:jira-software`|`read:board-scope:jira-software`|
    |`read:project:jira`|`read:project:jira`|

6.  Right-click the form header and click **Save**.

7.  Click the **OAuth Entity Profiles** tab and open the default record.

    For example, **Jira OAuth Profile**.

8.  In **OAuth Entity Profile Scopes**, ensure that the same entity scopes are provided.

    Else, insert new rows and select the same entity scopes you had earlier provided in the **OAuth Entity Scopes** tab.

9.  Right-click the form header and click **Save**.


### Create credential record for the Jira spoke

Create a credential record for the Jira account. The Jira spoke connection and credential alias uses this credential to authorize actions.

#### Before you begin

Role required: admin

#### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Click **New**.

    The system displays the message `What type of Credentials would you like to create?`

3.  Select **OAuth 2.0 Credentials**.

4.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Name|Name to identify the credential record for the Jira spoke. For example, `Jira cloud OAuth credential`.|
    |OAuth Entity Profile|Default OAuth entity profile record created when the application registry record is configured.|

5.  Click **Submit**.


### Create a connection record for the Jira spoke

Create a connection record for the Jira account. The connection and credential alias uses this connection to perform actions in Jira.

#### Before you begin

Role required: admin.

#### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Open the alias record for **Jira** that shipped with the spoke.

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

Enter any name to uniquely identify the connection record. For example, enter `Jira cloud OAuth Connection`.

</td></tr><tr><td>

Credential

</td><td>

Select the Credential record created for Jira. For example, select **Jira cloud OAuth credential**.

</td></tr><tr><td>



</td><td>



</td></tr><tr><td>

Connection URL

</td><td>

Enter the URL of your Jira instance in this format: `https://api.atlassian.com/ex/jira/<Cloud-ID>`.For information about obtaining the value of Cloud ID, see [Obtain the value of Cloud ID](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/setup-jira-spk-opt2.md).

</td></tr></tbody>
</table>5.  In the Attributes related list, provide these values.

    1.  Enter the value `2` for **api\_version**.

    2.  Enter the value `cloud` for **server\_type**.

    \[Omitted image "jira-cloud-api-attribute.png"\] Alt text: Attribute values.

6.  Click **Submit**.

7.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

8.  Open the credential record you had created for the Jira spoke.

    For example, **Jira OAuth credential**.

9.  Click the Get OAuth Token related link.

    In a new window, system requests access to your Atlassian account.

10. Click **Accept**.

    Access is granted to Atlassian account and a confirmation message is displayed in your ServiceNow instance that the refresh token is available.


## Option 2: Using basic authentication and API token \(does not comply with Atlassian security requirements\)

Integrate the ServiceNow instance and Jira Cloud instance using an API key to authenticate ServiceNow requests.

### Before you begin

**Important:** Apps that collect API tokens to create individual 3LO apps don't comply with Atlassian security requirements for cloud apps and Atlassian acceptable use policy.

Role required: admin.

### About this task

You can integrate a ServiceNow instance with multiple Jira instances. For this integration, create a connection and credential alias record and a connection record for each Jira instance.

### Generate an Atlassian account API token

Generate an Atlassian account API token to authenticate requests for spokes associated with an Atlassian account.

#### Before you begin

Make sure you have an Atlassian account.

Role required: Atlassian administrator credentials

#### About this task

Complete these steps from your Atlassian account. See the [Atlassian Developer](https://developer.atlassian.com/docs/) portal documentation for instructions on generating your API token.

**Note:** This procedure is applicable only if you are using the Jira Cloud subscription.

#### Procedure

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


#### What to do next

Use your API token to configure the cloud connection for the Jira spoke.

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
    -   To manage more than one Jira spoke connection records, you should create a new child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/support-multiple-connections.md).
    If you are configuring the spoke for the first time, click **Configure**. Otherwise, click **Edit**.

5.  On the **Connection** form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Connection Name|Name to uniquely identify the connection. For example, `Jira spoke cloud basic conn`.|
    |Connection URL|URL of your Jira instance in this format: `https://<provider-domain-name>.atlassian.net`.|
    |Server Type|Select **cloud**.|
    |User name|Enter the email address of the user.|
    |API Key|Enter the API token you generated for your Jira Cloud instance.|

    \[Omitted image "jira-cloud-basic.png"\] Alt text: Connection configuration for Jira Cloud.

6.  Click **Create Connection**.


## Option 3: Using basic authentication with API token and scopes \(does not comply with Atlassian security requirements\)

Integrate the ServiceNow instance and Jira Cloud instance using an API key with scopes to authenticate ServiceNow requests.

### Before you begin

**Important:** Apps that collect API tokens to create individual 3LO apps don't comply with Atlassian security requirements for cloud apps and Atlassian acceptable use policy.

Role required: admin.

### About this task

You can integrate a ServiceNow instance with multiple Jira instances. For this integration, create a connection and credential alias record and a connection record for each Jira instance.

### Generate an Atlassian account API token with scopes

Generate an Atlassian account API token with the required scopes to authenticate requests for spokes associated with an Atlassian account.

#### Before you begin

Make sure you have an Atlassian account.

Role required: Atlassian administrator credentials

#### About this task

Complete these steps from your Atlassian account. See the [Atlassian Developer](https://developer.atlassian.com/docs/) portal documentation for instructions on generating your API token.

**Note:** This procedure is applicable only if you are using the Jira Cloud subscription.

#### Procedure

1.  Log in to [Atlassian Start](https://start.atlassian.com/) as an admin.

2.  Go to your account profile photo and select **Account Settings**.

    \[Omitted image "jira-basic-settings.png"\] Alt text: Atlassian Start page with the drop down menu of the selected profile picture. Account Settings option emphasized.

3.  Go to **Security**.

4.  In the API token section, select **Create and manage API tokens**.

5.  Click **Create API token with scopes**.

    \[Omitted image "jira-new-api-token.jpg"\] Alt text: Create API token with scopes.

6.  On the Name API token form, enter **Name**, select an expiry date for the token, and click **Next**.

    \[Omitted image "jira-new-token-name.jpg"\] Alt text: Provide details to create token.

7.  On the Select the app form, select **Jira** and click **Next**.

    \[Omitted image "jira-new-select-jira-app.jpg"\] Alt text: Select the Jira app.

8.  On the Select Jira scopes form, select the required scopes and click **Next**.

    \[Omitted image "jira-new-scopes.jpg"\] Alt text: Select the required scopes.

    For details about scopes needed to use the required spoke actions, see [Required API token scopes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/setup-jira-spk-opt2.md).

9.  Review the API token scopes and click **Create token**.

    \[Omitted image "jira-new-token-scopes.jpg"\] Alt text: Review details and create token.

    API token is generated and displayed. Copy and record the token value for later use.

    \[Omitted image "jira-new-copy-token.jpg"\] Alt text: Copy the token value.


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
    -   To manage more than one Jira spoke connection records, you should create a new child alias record by clicking **Add Connection**. For more information about using multiple connections, see [Supporting multiple connections](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/support-multiple-connections.md).
    If you are configuring the spoke for the first time, click **Configure**. Otherwise, click **Edit**.

5.  On the **Connection** form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Connection Name|Name to uniquely identify the connection. For example, `Jira spoke cloud basic conn`.|
    |Connection URL|URL of your Jira instance in this format: `https://<provider-domain-name>.atlassian.net`.|
    |Server Type|Select **cloud**.|
    |User name|Enter the email address of the user.|
    |API Key|Enter the API token you generated for your Jira Cloud instance.|

    \[Omitted image "jira-cloud-basic.png"\] Alt text: Connection configuration for Jira Cloud.

6.  Click **Create Connection**.


### Required API token scopes

API token scopes needed to use the required spoke action are listed here.

These scopes are needed when you set up Jira spoke for Jira Cloud using API token with scope. For more information, see [Option 3: Using basic authentication with API token and scopes \(does not comply with Atlassian security requirements\)](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/setup-jira-spk-opt2.md).

<table id="table_pvx_v4s_qwb"><thead><tr><th>

Category

</th><th>

Action

</th><th>

Description

</th><th>

Scope required \(Classic\)

</th><th>

Scopes required \(Granular\)

</th></tr></thead><tbody><tr><td rowspan="2">

Audit Management

</td><td>

Look up Audit Logs Stream

</td><td>

Retrieves login activity for the AtlassianJira user subscriptions.**Note:** This action is supported on Jira Server 9 and earlier versions, and Jira Cloud.

</td><td>

manage:jira-configuration

</td><td>

read:audit-log:jira, read:user:jira

</td></tr><tr><td>

Look up Audit Logs Stream \(Server 10+\)

</td><td>

Retrieves audit log records from the Jira instance within a specified date range.**Note:** This action is supported on Jira Server 9 and later versions.

</td><td colspan="2">

This action is supported only on Jira Server.

</td></tr><tr><td rowspan="6">

Group Management

</td><td>

Add User to Group

</td><td>

Adds given user to a group in Jira.

</td><td>

manage:jira-configuration

</td><td>

write:group:jira, read:avatar:jira, read:group:jira, read:user:jira

</td></tr><tr><td>

Create Group

</td><td>

Creates a group in Jira.

</td><td>

manage:jira-configuration

</td><td>

read:group:jira, read:user:jira, write:group:jira, read:avatar:jira

</td></tr><tr><td>

Look up Groups Stream

</td><td>

Retrieves all groups in the Atlassian account, including the default groups.**Note:** This action can be used with Jira Cloud subscription only.

</td><td>

read:jira-user

</td><td>

read:group:jira

</td></tr><tr><td>

Look up Users by Group Name Stream

</td><td>

Retrieves details of all members in an Atlassian group.

</td><td>

manage:jira-configuration

</td><td>

read:group:jira, read:user:jira, read:avatar:jira

</td></tr><tr><td>

Remove Group

</td><td>

Removes the given group from Jira.

</td><td>

manage:jira-configuration

</td><td>

delete:group:jira

</td></tr><tr><td>

Remove User from Group

</td><td>

Removes the given user from a group in Jira.

</td><td>

manage:jira-configuration

</td><td>

write:group:jira

</td></tr><tr><td rowspan="17">

Issue Management

</td><td>

Add Comment

</td><td>

Adds a comment to the specified issue in Jira.

</td><td>

write:jira-work

</td><td>

read:comment:jira, read:comment.property:jira, read:group:jira, read:project:jira, read:project-role:jira, read:user:jira, write:comment:jira, read:avatar:jira

</td></tr><tr><td>

Add Watcher

</td><td>

Adds the specified user as a watcher for the specified issue.

</td><td>

write:jira-work

</td><td>

write:issue.watcher:jira

</td></tr><tr><td>

Assign Issue

</td><td>

Assigns the issue in Jira to the user.

</td><td>

write:jira-work

</td><td>

write:issue:jira

</td></tr><tr><td>

Copy Attachment

</td><td>

Copies the required attachment associated with the ServiceNow record to the required issue in Jira.

</td><td>

write:jira-work

</td><td>

read:user:jira, write:attachment:jira, read:attachment:jira, read:avatar:jira

</td></tr><tr><td>

Create Issue

</td><td>

Creates an issue in Jira. Depending on how your organization is using Jira, an issue could represent a software bug, a project task, a help desk ticket, or more. An issue in Jira represents a task in the ServiceNow AI Platform.

</td><td>

write:jira-work, read:jira-work

</td><td>

write:issue:jira, write:comment:jira, write:comment.property:jira, write:attachment:jira, read:issue:jira

</td></tr><tr><td>

Delete Attachment

</td><td>

Deletes the required attachment in Jira.

</td><td>

write:jira-work

</td><td>

delete:attachment:jira

</td></tr><tr><td>

Delete Issue

</td><td>

Deletes an issue in Jira.

</td><td>

write:jira-work

</td><td>

delete:issue:jira

</td></tr><tr><td>

Delete Watcher

</td><td>

Deletes the user as a watcher for the specified issue.

</td><td>

write:jira-work

</td><td>

write:issue.watcher:jira

</td></tr><tr><td>

Do Transition

</td><td>

Transitions an issue in Jira from one state to another.

</td><td>

write:jira-work

</td><td>

write:issue:jira, write:issue.property:jira

</td></tr><tr><td>

Look up Issue Type Statuses by Project

</td><td>

Retrieves details of the statuses in a project.

</td><td>

read:jira-work

</td><td>

read:issue-status:jira, read:issue-type:jira, read:status:jira

</td></tr><tr><td>

Look up Issue

</td><td>

Retrieves the details for an issue.

</td><td>

read:jira-work

</td><td>

read:issue-meta:jira, read:issue-security-level:jira, read:issue.vote:jira, read:issue.changelog:jira, read:avatar:jira, read:issue:jira, read:status:jira, read:user:jira, read:field-configuration:jira

</td></tr><tr><td>

Look up Issue Priorities

</td><td>

Retrieves the list of issue priorities and details for individual issue priorities.

</td><td>

write:jira-work, read:jira-work

</td><td>

read:priority:jira

</td></tr><tr><td>

Look up Issues Stream

</td><td>

Retrieves a list of issues matching a JQL query string.

</td><td>

read:jira-work

</td><td>

read:issue-details:jira, read:audit-log:jira, read:avatar:jira, read:field-configuration:jira, read:issue-meta:jira

</td></tr><tr><td>

Look up Sprint Issues Stream

</td><td>

Retrieves the details of all issues for the given sprint.

</td><td>

No classic scopes available.

</td><td>

read:sprint:jira-software , read:issue-details:jira, read:jql:jira

</td></tr><tr><td>

Look up Transitions

</td><td>

Retrieves information about all Transitions for a given Issue ID.

</td><td>

read:jira-work

</td><td>

read:issue.transition:jira, read:status:jira, read:field-configuration:jira

</td></tr><tr><td>

Look up Watchers

</td><td>

Retrieves the list of watchers for the specified issue.

</td><td>

read:jira-work

</td><td>

read:issue.watcher:jira, read:user:jira, read:avatar:jira

</td></tr><tr><td>

Update Issue

</td><td>

Updates a set number of fields of an issue in Jira with values passed as input.

</td><td>

write:jira-work, read:jira-work

</td><td>

write:issue:jira

</td></tr><tr><td rowspan="3">

Metadata Retrieval

</td><td>

Get Creatable Fields \(Metadata\)

</td><td>

Retrieves the list of all fields in a required Jira project.

</td><td>

write:jira-work, read:jira-work

</td><td>

read:issue-meta:jira, read:avatar:jira, read:field-configuration:jira

</td></tr><tr><td>

Get Editable Fields \(Metadata\)

</td><td>

Retrieves the list of all editable fields in a required Jira issue.

</td><td>

write:jira-work, read:jira-work

</td><td>

read:issue-meta:jira, read:field-configuration:jira

</td></tr><tr><td>

Get Issue Types \(Metadata\)

</td><td>

Retrieves the list of all issue types in a required Jira project.

</td><td>

write:jira-work, read:jira-work

</td><td>

read:issue-meta:jira, read:avatar:jira, read:field-configuration:jira

</td></tr><tr><td rowspan="5">

Project Management

</td><td>

Create Project

</td><td>

Creates a project in Jira.

</td><td>

manage:jira-configuration

</td><td>

write:project:jira, read:project:jira

</td></tr><tr><td>

Look up Project

</td><td>

Retrieves details of the specified project by its ID or key.

</td><td>

write:jira-work, read:jira-work

</td><td>

read:issue-type:jira, read:project:jira, read:project.property:jira, read:user:jira, read:application-role:jira, read:avatar:jira, read:group:jira, read:issue-type-hierarchy:jira, read:project-category:jira, read:project-version:jira, read:project.component:jira

</td></tr><tr><td>

Look up Projects

</td><td>

Retrieves details of all projects.**Note:** This action only works for the Jira server.

</td><td colspan="2">

This action is supported only on Jira Server.

</td></tr><tr><td>

Look up Projects Stream

</td><td>

Retrieves details of all projects.**Note:** This action only works for the Jira Cloud.

</td><td>

read:jira-work

</td><td>

read:issue-type:jira, read:project:jira, read:project.property:jira, read:user:jira, read:application-role:jira, read:avatar:jira, read:group:jira, read:issue-type-hierarchy:jira, read:project-category:jira, read:project-version:jira, read:project.component:jira

</td></tr><tr><td>

Look up Users Assignable to Projects

</td><td>

Retrieves a list of users that can be assigned to issues in one or more projects.

</td><td>

read:jira-user

</td><td>

read:project:jira, read:user:jira, read:application-role:jira, read:avatar:jira, read:group:jira

</td></tr><tr><td rowspan="5">

Sprint Management

</td><td>

Create Sprint

</td><td>

Creates a sprint in Jira.

</td><td>

No classic scopes are available.

</td><td>

read:board-scope:jira-software , read:project:jira Create Sprint - write:sprint:jira-software

</td></tr><tr><td>

Delete Sprint

</td><td>

Deletes a sprint in Jira.

</td><td>

No classic scopes are available.

</td><td>

delete:sprint:jira-software

</td></tr><tr><td>

Look up Sprint

</td><td>

Retrieves the details of the required sprint as a complex object.

</td><td>

No classic scopes are available.

</td><td>

read:sprint:jira-software

</td></tr><tr><td>

Look up Sprints by Board

</td><td>

Retrieves the details of all sprints in the required board.

</td><td>

No classic scopes are available.

</td><td>

read:sprint:jira-software

</td></tr><tr><td>

Update Sprint

</td><td>

Updates the details of a sprint in Jira.

</td><td>

No classic scopes are available.

</td><td>

write:sprint:jira-software

</td></tr><tr><td rowspan="3">

Story Management

</td><td>

Create Story

</td><td>

Creates a story in the Jira Cloud instance. This is comparable to story in the ServiceNow Agile Development plugin.

</td><td>

write:jira-work

</td><td>

write:issue:jira, write:comment:jira, write:comment.property:jira, write:attachment:jira, read:issue:jira

</td></tr><tr><td>

Look up Stories Stream

</td><td>

Retrieves details of all stories.

</td><td>

read:jira-work

</td><td>

read:issue-details:jira, read:field.default-value:jira, read:field.option:jira, read:field:jira, read:group:jira

</td></tr><tr><td>

Update Story

</td><td>

Updates a set number of fields of a story in Jira Cloud with the provided input values.

</td><td>

write:jira-work

</td><td>

write:issue:jira

</td></tr><tr><td rowspan="6">

User Management

</td><td>

Create User

</td><td>

Creates a user in Jira.**Note:** This action isn’t supported when OAuth 2.0 authentication is used.

</td><td colspan="2">

Scoped API token is not supported for this action.

</td></tr><tr><td>

Look up Authenticated User

</td><td>

Retrieves details of the authenticated user account.

</td><td>

read:jira-user

</td><td>

read:application-role:jira, read:group:jira, read:user:jira, read:avatar:jira

</td></tr><tr><td>

Look up Group Memberships for User

</td><td>

Retrieves details of all groups of an Atlassian user.

</td><td>

read:jira-user

</td><td>

read:group:jira

</td></tr><tr><td>

Look up Users Stream

</td><td>

Retrieves details of all Atlassian Jira user subscriptions.**Note:** This action can be used with a Jira Cloud subscription only.

</td><td>

read:jira-user

</td><td>

read:user:jira, read:application-role:jira, read:avatar:jira, read:group:jira

</td></tr><tr><td>

Look up Users Stream by Name

</td><td>

Retrieves a list of users that match the search string.**Note:** This action can be used with a Jira server subscription only.

</td><td colspan="2">

This action is supported only on Jira Server.

</td></tr><tr><td>

Remove User

</td><td>

Removes a user from Jira.**Note:** This action isn’t supported when OAuth 2.0 authentication is used.

</td><td colspan="2">

Scoped API token is not supported for this action.

</td></tr><tr><td rowspan="6">

Utility Actions

</td><td>

Copy Issue Attachment to Record

</td><td>

Copies Attachment from Jira to any record in ServiceNow instance. When you use this action in a subflow, make sure that the Content URL data pill is specified in the Attachment URL field.

</td><td colspan="2">

No applicable scopes as Jira endpoint is not used in this action.

</td></tr><tr><td>

Look up Fields

</td><td>

Retrieves the internal name and other details of the required field label in Jira.

</td><td>

read:jira-work

</td><td>

read:field:jira, read:avatar:jira, read:project-category:jira, read:project:jira, read:field-configuration:jira

</td></tr><tr><td>

Look up Issue from Comment

</td><td>

Retrieves the details of the issue by parsing the payload for the specified comment. You can use this action in the Process Jira Webhook subflow for Jira on-prem server when only comment related information is specified without any details about the Jira issue. For example, when only comment information is specified, this action parses the payload and extracts the issue details.

</td><td colspan="2">

No applicable scopes as Jira endpoint is not used in this action.

</td></tr><tr><td>

Look up Latest Attachment on Issue

</td><td>

Retrieves the latest attachment for the specified issue from Jira. You can use this action in a flow or subflow for validation. For example, a subflow adds an additional attachment only when the latest attachment of an issue in Jira isn’t as the same specified attachment.

</td><td>

read:jira-work

</td><td>

read:issue-meta:jira, read:issue-security-level:jira, read:issue.vote:jira, read:issue.changelog:jira, read:avatar:jira, read:issue:jira, read:status:jira, read:user:jira, read:field-configuration:jira

</td></tr><tr><td>

Look up Latest Comment on Issue

</td><td>

Retrieves the latest comment for the specified issue from Jira. You can use this action in a flow or subflow for validation. For example, a subflow adds an additional comment only when the latest comment of an issue in Jira isn’t as the same specified comment.

</td><td>

read:jira-work

</td><td>

read:comment:jira, read:comment.property:jira, read:group:jira, read:project:jira, read:project-role:jira, read:user:jira, read:avatar:jira

</td></tr><tr><td>

Look up Server

</td><td>

Retrieves general information about the current Jira instance.

</td><td>

Any scope

</td><td>

Any scope

</td></tr><tr><td rowspan="4">

Webhook Management

</td><td>

Look up Webhooks

</td><td>

Retrieves details of all registered webhooks from the Jira instance.

</td><td colspan="2">

Scoped API token is not supported for this action.

</td></tr><tr><td>

Subscribe Webhook

</td><td>

Registers a webhook in the Jira instance.

</td><td colspan="2">

Scoped API token is not supported for this action.

</td></tr><tr><td>

Unsubscribe Webhook

</td><td>

Deletes the registered webhook in Jira instance.

</td><td colspan="2">

Scoped API token is not supported for this action.

</td></tr><tr><td>

Update Webhook

</td><td>

Updates webhook with the given ID in Jira.**Note:** This action isn’t supported when OAuth 2.0 authentication is used.

</td><td colspan="2">

Scoped API token is not supported for this action.

</td></tr></tbody>
</table>