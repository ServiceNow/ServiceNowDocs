---
title: Integrate with Jira Software Cloud using OAuth 2.0
description: Integrate the Software Asset Management application with your Jira account using OAuth to authenticate ServiceNow requests.Create an OAuth 2.0 integration in the Atlassian Developer console to authenticate the requests.Obtain the value of the Cloud ID of the Jira cloud instance. This value is required during the configuration of the connection record in your ServiceNow instance.Create an integration profile to track software subscriptions and optimize licensing for Atlassian Jira Software Cloud.
locale: en-US
release: australia
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 10
breadcrumb: [Integrating with Jira Software Cloud, Integrate with SaaS applications, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Integrate with Jira Software Cloud using OAuth 2.0

Integrate the Software Asset Management application with your Jira account using OAuth to authenticate ServiceNow requests.

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
</table>## Create an OAuth 2.0 integration in Jira account

Create an OAuth 2.0 integration in the Atlassian Developer console to authenticate the requests.

### Before you begin

Jira Role required: Refer the [Minimal user permissions](integrate-with-jira-oauth.md#) table.

### Procedure

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


## Obtain the Cloud ID value of Jira instance

Obtain the value of the Cloud ID of the Jira cloud instance. This value is required during the configuration of the connection record in your ServiceNow instance.

### Before you begin

Jira Role required: admin

### Procedure

1.  Log in to [Atlassian Administration](https://admin.atlassian.com/).

2.  Select the **Select** button against the required organization.

3.  On the side navigation pane, select **Apps** &gt; **Atlassian apps**.

4.  On the Atlassian Apps page, select **Manage product** on the Jira product row.

    The URL is in the following format in a new window: `https://admin.atlassian.com/o/<orgID>/atlassian-apps/jira-software/<Cloud-Id>`.

5.  Copy the value of Cloud ID and secure it for later use.


## Create a Jira Software Cloud integration profile

Create an integration profile to track software subscriptions and optimize licensing for Atlassian Jira Software Cloud.

### Before you begin

To create a Jira integration profile, request the Software Asset Management - SaaS License Management plugin \(sn\_sam\_saas\_int\) from the [ServiceNow Store](https://store.servicenow.com/).

To enable the integration profile to retrieve and update user activity through the Jira Update User Activity subflow, set the **com.glide.transform.json.max-partial-length** system property **Value** to `32768`.

Atlassian Role required: site admin

ServiceNow Role required: sam\_integrator

**Important:** You must select the **Jira Spoke** check box for this integration while installing optional features on the [Application Manager](https://www.servicenow.com/docs/access?context=application-manager&version=australia&pubname=australia-platform-administration&ft:locale=en-US) page. For more information about choosing the required SaaS applications, see [Request SaaS License Management](../task/request-saas-license-management.md).

### About this task

If you’re using Software Asset Workspace, the option to create the Jira integration profile in Core UI is inactive.

### Procedure

1.  Navigate to the integration profile.

<table id="choicetable_o3p_z3k_qtb"><thead><tr><th align="left" id="d205178e690">

Interface

</th><th align="left" id="d205178e693">

Action

</th></tr></thead><tbody><tr><td id="d205178e699">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.
2.  Select **New**.
3.  Select **Jira Integration Profile**.


</td></tr><tr><td id="d205178e741">

**Software Asset Workspace**

</td><td>

1.  Navigate to **License operations** &gt; **User Subscriptions** &gt; **Direct integration profiles**.
2.  Select **New**.
3.  Select **Jira** from the drop-down list.
4.  Select **Continue**.


</td></tr></tbody>
</table>2.  On the form, fill in the fields.

<table id="table_iqh_2y5_mjb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Display name

</td><td>

Name of your choice. For example, Jira integration.

</td></tr><tr><td>

Status

</td><td>

Status of the integration profile.-   If you have not published the integration profile, this field is automatically set to **Draft**.
-   If you have already published the integration profile, this field is automatically set to **Published**.


</td></tr><tr><td>

Profile type

</td><td>

Jira Subscription. This field is automatically populated.

</td></tr></tbody>
</table>3.  Review the required user roles or API permissions specified in the **Vendor configuration** field for each process to minimize security risks and optimize SaaS licenses.

    **Note:** For more information, see the [Minimal user permissions](integrate-with-jira-oauth.md#) table.

    1.  In the Download Subscription Subflow section, verify that the **Subflow** field is set to **Jira Download Subscriptions**.

        **Note:** The **Download subscriptions** check box is selected by default and you can't clear it.

    2.  In the Calculate Activity Subflow section, verify that the **Subflow** field is set to **Jira Update User Activity**.

        **Note:** The **Download Activity** check box is selected by default. If you clear it, the activity scheduled job **SAM - Refresh &lt;displayname&gt; Activity** isn't created.

        In the **Analyze user activity** field, you can also select the date and time starting from when you want to analyze the user activity. By default, you can analyze user activity up to 60 days prior to the current date and view events performed by individual users from the time you create this profile.

        **Note:** Software Asset Management pulls the events from the time that you start analyzing user activity irrespective of the profile creation date.

        You can modify this value in the Last activity threshold field of your software reclamation rules. For more information, see [Review a software reclamation rule](../task/add-reclamation-rule-sub.md).

    3.  In the Reclaim Subscription Subflow section, verify that the **Subflow** field is set to **Jira Reclaim Subscription**.

        **Note:** The **Reclaim subscriptions** check box is selected by default. If you don't want to reclaim subscriptions, you can clear this check box. If you clear it, the removal candidates are created but the reclaim subscription subflow isn't triggered or the reclamation process isn't initiated.

4.  Select **Save**.

    A draft integration profile is created.

    The **Connection &amp; Credential** field appears and is automatically set to **sn\_jira\_spoke.jira\_subscription\_activity\_reclaim**.

    **Note:** The automatically populated value in the **Connection &amp; credential** field changes based on the selection in the **Download activity** and **Reclaim subscriptions** check boxes.

    |Selection|Connection &amp; credential value|
    |---------|---------------------------------|
    |Both **Download activity** and **Reclaim subscriptions** are selected.|sn\_jira\_spoke.jira\_subscription\_activity\_reclaim|
    |Only **Download activity** is selected.|sn\_jira\_spoke.jira\_subscription\_activity|
    |Only **Reclaim subscriptions** is selected.|sn\_jira\_spoke.jira\_subscription\_reclaim|
    |Both **Download activity** and **Reclaim subscriptions** aren’t selected.|sn\_jira\_spoke.jira\_subscription|

5.  Open the connection &amp; credential aliases record by selecting the preview icon ![](../image/preview-icon.png) next to the **Connection &amp; Credential** field and then selecting **Open Record** in the record preview.

6.  On the Connection &amp; Credential Aliases form, select the **Create New Connection &amp; Credential** related link.

7.  In the dialog box, fill in the fields.

<table id="table_ujr_ps1_wmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Name of the connection.

</td></tr><tr><td>

Connection URL

</td><td>

Base URL for the Jira API. This field is automatically set to `https://api.atlassian.com/ex/jira/<Cloud-ID>`.

</td></tr><tr><td>

OAuth Client ID

</td><td>

Client ID that is assigned to your Jira application.

</td></tr><tr><td>

OAuth Client Secret

</td><td>

Client secret that is assigned to your Jira application.

</td></tr><tr><td>

OAuth Redirect URL

</td><td>

URL of the OAuth provider that users are redirected to after authentication. This field populates automatically based and contains the URL of the ServiceNow instance that you specified in [Create an OAuth 2.0 integration in Jira account](integrate-with-jira-oauth.md#).

</td></tr></tbody>
</table>8.  Select **Create and Get OAuth Token**.

9.  On your ServiceNow instance, specify the groups that have access to Jira products.

    By specifying these groups on your ServiceNow instance, you can retrieve data and manage licenses for only the users within these groups.

    1.  In a new tab, open the [Atlassian Administration portal](https://admin.atlassian.com/).

    2.  Log in to your site admin account.

    3.  Select the **Select** button against the required organization.

    4.  Select the **Products** tab.

    5.  On the Products page, select **Manage product** on the Jira product row.

    6.  View the list of groups that have access to Jira Software.

        Secure this information for later use.

    7.  Return to your ServiceNow instance and navigate to **Jira** &gt; **Jira Groups**.

    8.  On the Jira Groups form, select the **Add Groups** related link.

        The Add Jira Groups dialog box opens.

    9.  In the Available list, select the groups that have access to Jira products.

        **Tip:** The Available list includes all groups that are associated with your Atlassian account. Select only the groups that have access to Jira products.

    10. Select the right arrow button to move the groups from the Available list to the Selected list.

    11. Select **OK**.

10. On the integration profile form, select **Validate Connection** to verify the connection and credential details of this integration.

    Validating the connection verifies the Download Subscriptions and Calculate Activity APIs, but not the Reclaim Subscriptions APIs.

11. After the connection is verified, select **Publish**.

12. In the Publish Confirmation dialog box, select **OK**.

    **Note:** If you clear the **Download Activity** check box after the integration profile is published, you must revalidate the connections and then republish the integration profile because the following events occur:

    -   The **Status** field on the integration profile form changes to **Draft**.
    -   The **Validate connection** button shows up on the form.
    -   The current **SAM - Refresh &lt;displayname&gt; Activity** job gets deleted.

### What to do next

After the integration connects, your ServiceNow instance automatically creates software models, reclamation rules, and software subscriptions that are refreshed daily.

After creating an integration profile, view information about the profile in the Software Asset Workspace by navigating to **License operations** &gt; **User subscription** &gt; **Direct integration profiles**. You can select an integration profile to view the following related lists. If all of the following related lists aren't visible for an integration profile in the default view, you can select the custom integration view from the Details tab:

-   Software Models
-   Unrecognized Subscription Identifiers
-   Scheduled Jobs
-   Scheduled Job Results
-   Software Subscriptions
-   Subscription Identifier Exclusion Rule
-   Subscription User Exclusion Rule

After creating an integration profile, you can define subscription exclusion rules to keep certain subscriptions from license cost calculations. For more information, see [Subscription exclusions for SaaS and SSO applications](subscription-exclusions.md#).

If you want to set up multiple integration profiles with unique connections, create child aliases to manage different configurations and settings for each integration profile. For more information, see [Create a child alias to set up multiple Jira integration profiles](../task/create-child-alias-jira.md).

Review all automatically generated reclamation rules to reclaim user subscriptions. For more information, see [Review a software reclamation rule](../task/add-reclamation-rule-sub.md).

Create software entitlements for the automatically generated software models to track used software against owned software.

-   For more information on creating software entitlements in the Software Asset Management Core UI, see [Create entitlements in Software Asset Management classic](../task/track-software-rights.md).
-   For more information on creating software entitlements in the Software Asset Workspace, see [Create entitlements in workspace](../task/create-entitlements-workspace.md).
-   For more information on creating software entitlements using the Software Asset Management Playbook, see [Create entitlements using the guided walk-through](../task/guidedwalk-workspace.md).

Reconciliation also runs on your subscriptions as a scheduled job or on-demand. You can view your reconciliation results in the [License Workbench](sam-license-workbench.md) \(Software Asset Management classic application\) or the [License usage view](sam-workspace-workbench.md) \(Software Asset Workspace\). Use these results to determine your license compliance position and to remediate any non-compliance.

-   For more information on running reconciliation in the Software Asset Management classic application, see [Run software reconciliation in Software Asset Management classic](../task/t_RunReconciliation.md).
-   For more information on running reconciliation in the Software Asset Workspace, see [Run software reconciliation in the workspace](../task/run-recon-workspace.md).

