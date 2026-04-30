---
title: Integrating with Jira Software Cloud
description: Integrating your Software Asset Management application with Atlassian Jira Software Cloud enables you to track your software subscriptions and to reclaim unused licenses.Integrate the Software Asset Management application and Jira using an API key to authenticate ServiceNow requests.Create an API token in Jira to authenticate requests.Configure the default connection and credential alias record to authenticate the requests from ServiceNow.Integrate the Software Asset Management application with your Jira account using OAuth to authenticate ServiceNow requests.Create an OAuth 2.0 integration in the Atlassian Developer console to authenticate the requests.Obtain the value of the Cloud ID of the Jira cloud instance. This value is required during the configuration of the connection record in your ServiceNow instance.Use the generated information while creating the OAuth 2.0 integration to create an application registry record in your ServiceNow instance.Create a credential record for the Jira account. The Jira spoke connection and credential alias uses this credential to authorize actions.Create a connection record for the Jira account. The connection and credential alias uses this connection to perform actions in Jira.Create an integration profile to track software subscriptions and optimize licensing for Atlassian Jira Software Cloud.
locale: en-US
release: xanadu
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 12
breadcrumb: [Integrate with SaaS applications, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Integrating with Jira Software Cloud

Integrating your Software Asset Management application with Atlassian Jira Software Cloud enables you to track your software subscriptions and to reclaim unused licenses.

**Note:** Currently this integration supports only one site integration per profile.

-   If your installed Jira spoke version is 4.1.0 or higher, you can integrate Jira with your ServiceNow instance by using one of the following methods:
    -   [Using basic authentication](integrate-with-jira.md#)

    -   [Using OAuth authentication](integrate-with-jira.md#)

-   If your installed Jira spoke version is lower than 4.1.0, integrate Jira with your ServiceNow instance by [Using basic authentication](integrate-with-jira.md#) method.

**Important:** Minimize security risks and protect information by granting access only to the necessary user or API permissions.

<table id="table_box"><thead><tr><th>

Process

</th><th>

Required user role in the Jira Software Cloud application

</th><th>

Authentication scopes

</th></tr></thead><tbody><tr><td>

Download subscriptions

</td><td>

Permission to access Jira

</td><td>

-   read:application-role:jira
-   read:group:jira
-   read:user:jira
-   read:avatar:jira

</td></tr><tr><td>

Pull user activity

</td><td>

-   Administer Jira global permission
-   Browse projects permission for the project containing the issue.

If issue-level security is configured, issue-level security permission to view the issue.


</td><td>

-   read:user:jira
-   read:issue-details:jira
-   read:audit-log:jira
-   read:avatar:jira
-   read:field-configuration:jira
-   read:issue-meta:jira

</td></tr><tr><td>

Reclaim subscription

</td><td>

Site administration, that is, member of the site-admin group

</td><td>

-   read:group:jira
-   write:group:jira

</td></tr></tbody>
</table>## Using basic authentication

Integrate the Software Asset Management application and Jira using an API key to authenticate ServiceNow requests.

You can integrate a ServiceNow instance with multiple Jira instances. For this integration, create a connection and credential alias record and a connection record for each Jira instance.

### Create an Jira account API token

Create an API token in Jira to authenticate requests.

#### Before you begin

Jira Role required: Refer the [Minimal user permissions](integrate-with-jira.md#) table.

#### Procedure

1.  Navigate to [Atlassian API Tokens](https://id.atlassian.com/manage/api-tokens).

2.  Select **Create API token**.

3.  Enter a name for your API token, then select **Create**.

4.  Copy the API token and save it.

    You’ll use the token later.


### Configure the connection and credential record

Configure the default connection and credential alias record to authenticate the requests from ServiceNow.

#### Before you begin

Role required: admin

#### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Open the alias record for Jira that is shipped with the spoke.

3.  Select the **Create New Connection &amp; Credential** related link.

4.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Connection URL|URL of your Jira instance in `https://<provider-domain-name>.atlassian.net` format.|
    |User Name|Enter the email address of the user.|
    |API Key|Enter the API token that you generated for Jira.|

5.  Select **Create**.


## Using OAuth authentication

Integrate the Software Asset Management application with your Jira account using OAuth to authenticate ServiceNow requests.

### Create an OAuth 2.0 integration in Jira account

Create an OAuth 2.0 integration in the Atlassian Developer console to authenticate the requests.

#### Before you begin

Jira Role required: Refer the [Minimal user permissions](integrate-with-jira.md#) table.

#### Procedure

1.  Log in to [Atlassian Developer console](https://id.atlassian.com/login?continue=https%3A%2F%2Fdeveloper.atlassian.com%2Fconsole%2Fmyapps%2F).

2.  Under **My apps**, select **Create** and select **OAuth 2.0 integration**.

3.  On the form, provide a name for the integration and select **Create**.

    The integration is created and the value of App ID is displayed.

4.  Select **Authorization**.

    1.  Select **Add** under **Action**.

    2.  In **Callback URL**, provide the URL of your ServiceNow instance in this format: `https://<ServiceNow-Instance-Name>.service-now.com/oauth_redirect.do`.

        For example, `https://example.service-now.com/oauth_redirect.do`.

    3.  Select **Save changes**.

5.  Select **Settings**.

6.  Under **Authentication details**, copy the values of Client ID and Client Secret.

7.  Select **Permissions** &gt; **Jira API** &gt; **Configure**.

8.  Select the **Granular scopes** tab.

9.  Select **Edit Scopes** to add the following scopes:

    -   read:application-role:jira
    -   read:group:jira
    -   read:user:jira
    -   read:avatar:jira
    -   read:audit-log:jira
    -   read:issue-details:jira
    -   read:field-configuration:jira
    -   read:issue-meta:jira
    -   write:group:jira
    You can configure other scopes according to your requirement.


### Obtain the Cloud ID value of Jira instance

Obtain the value of the Cloud ID of the Jira cloud instance. This value is required during the configuration of the connection record in your ServiceNow instance.

#### Before you begin

Jira Role required: admin

#### Procedure

1.  Log in to [Atlassian Administration](https://admin.atlassian.com/).

2.  Select the **Select** button against the required organization.

3.  Select the **Products** tab.

4.  On the Products page, select **Manage product** on the Jira product row.

    The URL is in the following format in a new window: `https://admin.atlassian.com/o/<orgID>/products/jira-software/<Cloud-Id>`.

5.  Copy the value of the Cloud ID for later use.


### Create an application registry in ServiceNow instance

Use the generated information while creating the OAuth 2.0 integration to create an application registry record in your ServiceNow instance.

#### Before you begin

Role required: admin

#### Procedure

1.  Navigate to **All** &gt; **System OAuth** &gt; **Application Registry**.

2.  Select **New**.

    The system displays a message as `What kind of OAuth application?`.

3.  Select **Connect to a third party OAuth Provider**.

4.  On the form, fill these values.

<table id="table_smt_hg5_mwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name to identify the application registry record.

</td></tr><tr><td>

Client ID

</td><td>

Client ID generated when the OAuth 2.0 integration was created in the Atlassian Developer console.

</td></tr><tr><td>

Client Secret

</td><td>

Client secret generated when the OAuth 2.0 integration was created in the Atlassian Developer console.

</td></tr><tr><td>

Default Grant type

</td><td>

Grant type used to establish the token. Select **Authorization Code**.

</td></tr><tr><td>

Authorization URL

</td><td>

OAuth authorization code endpoint. Enter `https://auth.atlassian.com/authorize`.

</td></tr><tr><td>

Token URL

</td><td>

OAuth server token endpoint. Enter `https://auth.atlassian.com/oauth/token`.

</td></tr><tr><td>

Redirect URL

</td><td>

OAuth callback endpoint. System generates the URL while saving the application registry.

</td></tr><tr><td>

Refresh Token URL

</td><td>

URL to refresh a token. Enter `https://auth.atlassian.com/oauth/token`.**Note:** This field is hidden in the form layout. Configure the form layout to show this field.

</td></tr></tbody>
</table>5.  Select and hold \(or right-click\) the form header and select **Save**.

    A default OAuth entity profile record is created in the **OAuth Entity Profiles** tab.

6.  In the OAuth Entity Scopes, create the following entity scope records.

    |Name|OAuth scope|
    |----|-----------|
    |read:application-role:jira|read:application-role:jira|
    |read:group:jira|read:group:jira|
    |read:user:jira|read:user:jira|
    |read:avatar:jira|read:avatar:jira|
    |read:audit-log:jira|read:audit-log:jira|
    |read:issue-details:jira|read:issue-details:jira|
    |read:field-configuration:jira|read:field-configuration:jira|
    |read:issue-meta:jira|read:issue-meta:jira|
    |write:group:jira|write:group:jira|
    |offline\_access|offline\_access|


#### Result

An application registry record is created in your ServiceNow instance.

### Create a credential record for Jira

Create a credential record for the Jira account. The Jira spoke connection and credential alias uses this credential to authorize actions.

#### Before you begin

Role required: admin

#### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

2.  Select **New**.

    The system displays a message as `What type of Credentials would you like to create?`.

3.  Select **OAuth 2.0 Credentials**.

4.  On the form, fill these values.

    |Field|Description|
    |-----|-----------|
    |Name|Name to identify the credential record for the Jira spoke. For example, `Jira OAuth credential`.|
    |OAuth Entity Profile|Default OAuth entity profile record created when the application registry record is configured.|

5.  Select **Submit**.


### Create a connection record for Jira

Create a connection record for the Jira account. The connection and credential alias uses this connection to perform actions in Jira.

#### Before you begin

Role required: admin

#### Procedure

1.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Connection &amp; Credential Aliases**.

2.  Open the alias record for Jira that is shipped with the spoke.

3.  On the **Connections** tab, select **New**.

4.  On the HTTP\(s\) Connection form, fill in these fields.

<table id="table_eqh_1n5_mwb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter any unique name to identify the connection record. For example, enter Jira OAuth Connection.

</td></tr><tr><td>

Credential

</td><td>

Select the Credential record created for Jira. For example, select Jira OAuth Credentials.

</td></tr><tr><td>

Connection alias

</td><td>

Search for and select **sn\_jira\_spoke.Jira** alias.

</td></tr><tr><td>

Connection URL

</td><td>

Enter the URL of your Jira instance in the `https://api.atlassian.com/ex/jira/<Cloud-ID>` format.For information about getting the value of Cloud ID, see [Obtain the Cloud ID value of Jira instance](integrate-with-jira.md#).

</td></tr></tbody>
</table>5.  In the Attributes related list, provide these values.

    1.  Enter the value of `2` for **api\_version**.
    2.  Enter the value `cloud` for **server\_type**.
6.  Select **Submit**.

7.  Navigate to **All** &gt; **Connections &amp; Credentials** &gt; **Credentials**.

8.  Open the credential record that you had created for the Jira spoke.

    For example, Jira OAuth credential.

9.  Select the **Get OAuth Token** related link.

    In a new window, the system asks access to your Atlassian account.

    **Note:** For the role required to perform this step, refer to the [Minimal user permissions](integrate-with-jira.md#) table.

10. Select **Accept**.

    Access is granted to the Atlassian account and a confirmation message is displayed in your ServiceNow instance that the refresh token is available.


## Create a Jira Software Cloud integration profile

Create an integration profile to track software subscriptions and optimize licensing for Atlassian Jira Software Cloud.

### Before you begin

To create a Jira integration profile, request the Software Asset Management - SaaS License Management plugin \(sn\_sam\_saas\_int\) from the [ServiceNow Store](https://store.servicenow.com/).

To enable the integration profile to retrieve and update user activity through the Jira Update User Activity subflow, set the **com.glide.transform.json.max-partial-length** system property **Value** to `32768`.

Atlassian Role required: site admin

ServiceNow Role required:

-   Starting with version 5.0.1 of Software Asset Management - SaaS License Management and version 3.0.4 of the Jira spoke, either of the following ServiceNow roles is required:

    -   sam\_integrator and sn\_jira\_spoke.jira\_admin
    -   admin
-   Prior to version 5.0.1 of Software Asset Management - SaaS License Management and version 3.0.4 of the Jira spoke, the sam\_integrator or admin ServiceNow role is required.


### About this task

If you’re using Software Asset Workspace, the option to create the Jira integration profile in Core UI is inactive.

### Procedure

1.  Navigate to the integration profile.

<table id="choicetable_o3p_z3k_qtb"><thead><tr><th align="left" id="d157901e1991">

Interface

</th><th align="left" id="d157901e1994">

Action

</th></tr></thead><tbody><tr><td id="d157901e2000">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.
2.  Select **New**.
3.  Select **Jira Integration Profile**.


</td></tr><tr><td id="d157901e2042">

**Software Asset Workspace**

</td><td>

1.  Navigate to **License operations** &gt; **User Subscriptions** &gt; **Direct integration profiles**.
2.  Select **New**.
3.  Select **Jira** from the drop-down list.
4.  Select **Continue**.


</td></tr></tbody>
</table>2.  On the form, fill in the fields.

    |Field|Value|
    |-----|-----|
    |Display name|Name of your choice. For example, Jira integration.|
    |Connection &amp; Credential|sn\_jira\_spoke.Jira. This field is automatically populated.|
    |Status|Status of the integration profile. The options are **Draft** and **Published**. This field is automatically populated.|
    |Profile type|Jira Subscription. This field is automatically populated.|

3.  In the **Calculate Activity Subflow** form section, choose a value for the **Analyze user activity from** field.

    You can also select the date and time that you want to analyze user activity from in the Analyze user activity from field. By default, you can analyze user activity up to 60 days prior to the current date and view events performed by individual users from the time you create this profile.

    **Note:** Software Asset Management pulls the events from the time that you start analyzing user activity irrespective of the profile creation date.

    You can modify this value in the Last activity threshold field of your software reclamation rules. For more information, see [Review a software reclamation rule](../task/add-reclamation-rule-sub.md).

    **Note:** After you save the integration profile, the **Analyze user activity from** field becomes read only.

4.  Select **Save**.

    A draft integration profile is created. The integration profile uses the Jira Download Subscriptions, Jira Update User Activity, and Jira Reclaim Subscription subflows to get user data from the Jira Software application.

5.  Specify the groups that have access to Jira products.

    **Important:** This step is applicable only starting with version 5.0.1 of Software Asset Management - SaaS License Management Integrations and version 3.0.4 of the Jira spoke.

    By specifying these groups on your ServiceNow instance, you can retrieve data and manage licenses for only the users within these groups.

    1.  In a new tab, open the [Atlassian Administration portal](https://admin.atlassian.com/).

    2.  Log in to your site admin account.

    3.  Select the **Select** button against the required organization.

    4.  Select the **Products** tab.

    5.  On the Products page, select **Manage product** on the Jira product row.

    6.  View the list of groups that have access to Jira Software.

        Take note of this information for later use.

    7.  Return to your ServiceNow instance and navigate to **Jira** &gt; **Jira Groups**.

    8.  On the Jira Groups form, select the **Add Groups** related link.

        The Add Jira Groups dialog box opens.

    9.  In the Available list, select the groups that have access to Jira products.

        **Tip:** The Available list includes all groups that are associated with your Atlassian account. Select only the groups that have access to Jira products.

    10. Select the right arrow button to move the groups from the Available list to the Selected list.

    11. Select **OK**.

6.  Return to your integration profile and then select the integration profile.

7.  Select **Publish**.

8.  In the Publish Confirmation dialog box, select **OK**.


### What to do next

After the integration connects, your ServiceNow instance automatically creates software models, reclamation rules, and software subscriptions that are refreshed daily.

If you want to set up multiple integration profiles with unique connections, create child aliases to manage different configurations and settings for each integration profile. For more information, see [Create a child alias to set up multiple integration profiles](../task/create-child-alias-saas.md).

Review all automatically generated reclamation rules to reclaim user subscriptions. For more information, see [Review a software reclamation rule](../task/add-reclamation-rule-sub.md).

Create software entitlements for the automatically generated software models to track used software against owned software.

-   For more information on creating software entitlements in the Software Asset Management Core UI, see [Create entitlements in Software Asset Management classic](../task/track-software-rights.md).
-   For more information on creating software entitlements in the Software Asset Workspace, see [Create entitlements in workspace](../task/create-entitlements-workspace.md).
-   For more information on creating software entitlements using the Software Asset Management Playbook, see [Create entitlements using the guided walk-through](../task/guidedwalk-workspace.md).

Reconciliation also runs on your subscriptions as a scheduled job or on-demand. You can view your reconciliation results in the [License Workbench](sam-license-workbench.md) \(Software Asset Management classic application\) or the [License usage view](sam-workspace-workbench.md) \(Software Asset Workspace\). Use these results to determine your license compliance position and to remediate any non-compliance.

-   For more information on running reconciliation in the Software Asset Management classic application, see [Run software reconciliation](../task/t_RunReconciliation.md).
-   For more information on running reconciliation in the Software Asset Workspace, see [Run software reconciliation in the workspace](../task/run-recon-workspace.md).

