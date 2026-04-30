---
title: Integrating with Dropbox
description: Integrating your Software Asset Management application with the Dropbox service enables you to track your software subscriptions and to reclaim unused licenses.Create an application on the DBX Platform for Developers.Create an integration profile to track software subscriptions and optimize licensing for the Dropbox service.
locale: en-US
release: yokohama
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 8
breadcrumb: [Integrate with SaaS applications, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Integrating with Dropbox

Integrating your Software Asset Management application with the Dropbox service enables you to track your software subscriptions and to reclaim unused licenses.

For more information about the Dropbox service, see the [Dropbox Business User and Admin Guides](https://www.dropbox.com/guide).

**Important:** Minimize security risks and protect information by granting access only to the necessary user or API permissions.

<table id="table_box"><thead><tr><th>

Process

</th><th>

Required user role in the Dropbox application

</th><th>

Authentication scopes

</th></tr></thead><tbody><tr><td>

Download subscriptions

</td><td>

Security Admin

</td><td>

-   members.read
-   team\_data.member

</td></tr><tr><td>

Pull user activity

</td><td>

Security Admin

</td><td>

-   events.read
-   team\_data.member

</td></tr><tr><td>

Reclaim subscription

</td><td>

Security Admin

</td><td>

-   team\_info.read
-   members.write
-   members.delete

</td></tr></tbody>
</table>## Create a Dropbox application for user subscriptions

Create an application on the DBX Platform for Developers.

### Before you begin

Dropbox Role required: Refer to the [Minimal user permissions](integrate-with-dropbox.md#) table.

### Procedure

1.  Navigate to [Dropbox Developer Apps](https://www.dropbox.com/login?cont=https%3A%2F%2Fwww.dropbox.com%2Fdevelopers%2Fapps) and sign in to your account.

2.  On the My Apps page, select **Create App**.

3.  Select scoped access API.

4.  Specify the type of access to **Full Dropbox**.

5.  Enter a name for your application and select **Create app**.

6.  Select the **Permission** tab.

7.  Select these permission check boxes:

    -   team\_info.read
    -   members.write
    -   members.delete
    -   groups.read
    -   events.read
    -   team\_data.member
8.  Select **Submit** to save the changes.

9.  Navigate to the **Settings** tab.

10. Obtain the App key and App secret.

    You will need to copy and paste these values into the Client ID and Client Secret fields in your ServiceNow instance in the following steps.

    **Note:** Your App key \(client ID\) and App secret \(client secret\) are sensitive. Do not share them.

11. Enter `https://*instance*.service-now.com/oauth_redirect.do` as the redirect URI, where *instance* is the name of your ServiceNow instance.

12. Click the **Branding** tab and then click **Save changes**.


## Create a Dropbox integration profile

Create an integration profile to track software subscriptions and optimize licensing for the Dropbox service.

### Before you begin

To create a Dropbox integration profile, request the Software Asset Management - SaaS License Management plugin \(sn\_sam\_saas\_int\) from the [ServiceNow Store](https://store.servicenow.com/).

ServiceNow Role required: sam\_integrator or admin

### About this task

If you’re using Software Asset Workspace, the option to create the Dropbox integration profile in Core UI is inactive.

### Procedure

1.  Using the information from the application with the permissions set to **Team member file access**, return to your ServiceNow instance to create an integration profile.

2.  Navigate to the integration profile.

<table id="choicetable_o3p_z3k_qtb"><thead><tr><th align="left" id="d285328e470">

Interface

</th><th align="left" id="d285328e473">

Action

</th></tr></thead><tbody><tr><td id="d285328e479">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.
2.  Select **New**.
3.  Select **Dropbox Integration Profile**.


</td></tr><tr><td id="d285328e521">

**Software Asset Workspace**

</td><td>

1.  Navigate to **License operations** &gt; **User Subscriptions** &gt; **Direct integration profiles**.
2.  Select **New**.
3.  Select **Dropbox** from the drop-down list.
4.  Select **Continue**.


</td></tr></tbody>
</table>3.  On the form, fill in the fields.

<table id="table_gnm_whv_5fb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr id="row_ksq_rt5_bgb"><td id="display-name">

Display name

</td><td id="display-name-def">

Name of the integration profile. For example, `DropBox Integration`

</td></tr><tr id="row_qnx_rt5_bgb"><td id="client-id">

Client Id

</td><td id="client-id-def">

Client ID for the OAuth application created in the SaaS admin account.

</td></tr><tr><td id="redirect-url">

Redirect url

</td><td id="redirect-url-def">

URL of the OAuth provider that you're redirected to after authentication. This value is automatically populated.

</td></tr><tr id="row_lvc_st5_bgb"><td id="client-secret">

Client secret

</td><td id="client-secret-def">

Password associated with the client ID.

</td></tr><tr id="row_nn5_st5_bgb"><td id="profile-type">

Profile type

</td><td id="profile-type-def">

Type of integration profile. This value is automatically set to **DropBox Subscription**.

</td></tr><tr><td id="activity-date">

Analyze user activity from

</td><td id="activity-date-def">

In the **Analyze user activity** field, you can also select the date and time starting from when you want to analyze the user activity. By default, you can analyze user activity up to 60 days prior to the current date and view events performed by individual users from the time you create this profile.

**Note:** Software Asset Management pulls the events from the time that you start analyzing user activity irrespective of the profile creation date.

You can modify this value in the Last activity threshold field of your software reclamation rules. For more information, see [Review a software reclamation rule](../task/add-reclamation-rule-sub.md).

</td></tr></tbody>
</table>4.  In the Process configuration section, review the required user roles or API permissions specified in the **Vendor configuration** field for each process to minimize security risks and optimize SaaS licenses.

    **Note:** For more information about the required roles and scopes, see [Minimal user permissions](integrate-with-dropbox.md#) table.

    -   The **Download subscriptions** check box is selected by default and you can't clear it.

    -   The **Download Activity** check box is selected by default. If you clear it, the activity scheduled job **SAM - Refresh &lt;displayname&gt; Events** isn't created.

        In the **Analyze user activity** field, you can also select the date and time starting from when you want to analyze the user activity. By default, you can analyze user activity up to 60 days prior to the current date and view events performed by individual users from the time you create this profile.

        **Note:** Software Asset Management pulls the events from the time that you start analyzing user activity irrespective of the profile creation date.

        You can modify this value in the Last activity threshold field of your software reclamation rules. For more information, see [Review a software reclamation rule](../task/add-reclamation-rule-sub.md).

    -   The **Reclaim subscriptions** check box is selected by default. If you don't want to reclaim subscriptions, you can clear this check box. If you clear it, the removal candidates are created but the reclaim subscription subflow isn't triggered or the reclamation process isn't initiated.

5.  Select **Submit** after completing all the required fields.

    Your ServiceNow instance creates a draft integration profile.

6.  On the integration profile form, select **Get OAuth Token**.

    **Note:** For the role required to perform this step, refer to the [Minimal user permissions](integrate-with-dropbox.md#) table.

7.  Navigate to the Dropbox application.

    -   Select **Allow** if you have already logged in to the Dropbox application.
    -   If you haven't logged in to the Dropbox application, log in with your admin credentials and then continue with the next steps.
    **Note:** When user subscriptions are reclaimed, files from the reclaimed accounts are transferred to the admin account selected in this step. This account can be a different admin account than the one used to set up the integration. If you have to start transferring files to a new admin, you can select the **Get OAuth Token** related link again at any time to select a different admin account. After selecting a new admin, you can reclaim the old admin account to transfer all of their files to the new admin, including all previously reclaimed user files.

8.  On the integration profile form, select **Validate Connection** to verify the connection and credential details of this integration.

    Validating the connection verifies the Download Subscriptions and Calculate Activity APIs, but not the Reclaim Subscriptions APIs.

    **Note:** If you clear the **Download Activity** check box after the integration profile is validated and scheduled jobs are created, you must revalidate the connections because the following events occur:

    -   The **Status** field on the integration profile form changes to **Draft**.
    -   The **Validate connection** button shows up on the form.
    -   The current **SAM - Refresh &lt;displayname&gt; Events** job gets deleted.

### What to do next

After the integration connects, your ServiceNow instance automatically creates software models, reclamation rules, and software subscriptions that are refreshed daily.

If you want to set up multiple integration profiles with unique connections, create child aliases to manage different configurations and settings for each integration profile. For more information, see [Create a child alias to set up multiple integration profiles](../reuse/create-child-alias-saas.md).

Review all automatically generated reclamation rules to reclaim user subscriptions. For more information, see [Review a software reclamation rule](../task/add-reclamation-rule-sub.md).

Create software entitlements for the automatically generated software models to track used software against owned software.

-   For more information on creating software entitlements in the Software Asset Management Core UI, see [Create entitlements in Software Asset Management classic](../task/track-software-rights.md).
-   For more information on creating software entitlements in the Software Asset Workspace, see [Create entitlements in workspace](../task/create-entitlements-workspace.md).
-   For more information on creating software entitlements using the Software Asset Management Playbook, see [Create entitlements using the guided walk-through](../task/guidedwalk-workspace.md).

Reconciliation also runs on your subscriptions as a scheduled job or on-demand. You can view your reconciliation results in the [License Workbench](sam-license-workbench.md) \(Software Asset Management classic application\) or the [License usage view](sam-workspace-workbench.md) \(Software Asset Workspace\). Use these results to determine your license compliance position and to remediate any non-compliance.

-   For more information on running reconciliation in the Software Asset Management classic application, see [Run software reconciliation in Software Asset Management classic](../task/t_RunReconciliation.md).
-   For more information on running reconciliation in the Software Asset Workspace, see [Run software reconciliation in the workspace](../task/run-recon-workspace.md).

