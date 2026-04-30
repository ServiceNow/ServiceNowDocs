---
title: Integrating with PagerDuty
description: Integrating your Software Asset Management application with the PagerDuty application enables you to track your software subscriptions and to reclaim unused licenses.Create a PagerDuty application to integrate with your ServiceNow instance.After you create a PagerDuty application, configure OAuth 2.0 to authorize your application to administer PagerDuty and access user-specific data on user login.Create a PagerDuty integration profile to track software subscriptions and optimize licensing for your PagerDuty applications.
locale: en-US
release: zurich
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 10
breadcrumb: [Integrate with SaaS applications, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Integrating with PagerDuty

Integrating your Software Asset Management application with the PagerDuty application enables you to track your software subscriptions and to reclaim unused licenses.

**Important:** Minimize security risks and protect information by granting access only to the necessary user or API permissions.

<table id="table_kcp_jts_nbc"><thead><tr><th>

Process

</th><th>

Required user role in the PagerDuty application

</th><th>

Authentication scopes

</th></tr></thead><tbody><tr><td>

Download subscriptions

</td><td>

-   Create OAuth app: Manager
-   Token generation: Observer

</td><td>

-   Scoped OAuth: users:read
-   Classic User OAuth: Read

</td></tr><tr><td>

Pull user activity

</td><td>

-   Create OAuth app: Manager
-   Token generation: Observer

</td><td>

-   Scoped OAuth: oncalls:read
-   Classic User OAuth: Read

</td></tr><tr><td>

Reclaim subscription

</td><td>

Create OAuth app and token generation: Global admin

</td><td>

-   Scoped OAuth: users:write
-   Classic User OAuth: Read/Write

</td></tr></tbody>
</table>## Create a PagerDuty application

Create a PagerDuty application to integrate with your ServiceNow instance.

### Before you begin

-   Activate the PagerDuty spoke. For more information, see [PagerDuty Spoke](https://www.servicenow.com/docs/access?context=pagerduty-spoke&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US).
-   PagerDuty Role required: Refer to the [Minimal user permissions](integrate-with-pagerduty.md#) table.

### Procedure

1.  From a web browser, log in to the [PagerDuty portal](https://app.pagerduty.com/) using your account credentials.

2.  Log in to your PagerDuty account.

3.  Enable Developer Mode.

    -   If you’re logged in with a developer account, you can access Developer Mode automatically.
    -   If you’re logged in with a customer account, you must enable Developer Mode manually by following these steps.
    1.  Select the INTEGRATIONS tab.

    2.  In the DEVELOPER TOOLS section, navigate to **App Registration**.

        You’re redirected to the Add New App page in Developer Mode.

4.  On the Add New App page, select **New App**.

5.  On the App Information form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the PagerDuty application. For example, `ServiceNow Integration`.|
    |Description|Brief description of the application.|

6.  Select **OAuth 2.0** in the Functionality section.

7.  Select **Next**.

    PagerDuty registers your application and then returns you to the Add New App page.


## Configure OAuth 2.0 for your PagerDuty application

After you create a PagerDuty application, configure OAuth 2.0 to authorize your application to administer PagerDuty and access user-specific data on user login.

### Before you begin

PagerDuty Role required: Refer to the [Minimal user permissions](integrate-with-pagerduty.md#) table.

### Procedure

1.  On the Add New App page of your PagerDuty account, select **Scoped OAuth** or **Classic User OAuth** in the Authorization section.

    For more information about the permission scopes, refer to the [Minimal user permissions](integrate-with-pagerduty.md#) table.

2.  In the **Redirect URL** field, enter the URL of the OAuth provider that users are redirected to after authentication.

    For example, `https://<*instance-name*>/oauth_redirect.do`, where &lt;*instance-name*&gt; is the name of your ServiceNow instance.

3.  In the **Permission Scope** field, select the required permission.

4.  Select **Register App**.

5.  From the OAuth 2.0 Client Information window, copy the values in the **Client ID** and **Client Secret** fields.

    Save them in a secure location for later use.

6.  Select **Continue**.


## Create a PagerDuty integration profile

Create a PagerDuty integration profile to track software subscriptions and optimize licensing for your PagerDuty applications.

### Before you begin

To create a PagerDuty integration profile, request the Software Asset Management - SaaS License Management plugin \(sn\_sam\_saas\_int\) from the [ServiceNow Store](https://store.servicenow.com/).

ServiceNow Role required: sam\_integrator or admin

**Important:** You must select the **PagerDuty Spoke** check box for this integration while installing optional features on the [Application Manager](https://www.servicenow.com/docs/access?context=application-manager&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) page. For more information about choosing the required SaaS applications, see [Request SaaS License Management](../task/request-saas-license-management.md).

### About this task

If you’re using Software Asset Workspace, the option to create the PagerDuty integration profile in Core UI is inactive.

### Procedure

1.  Navigate to the integration profile.

<table id="choicetable_o3p_z3k_qtb"><thead><tr><th align="left" id="d126470e672">

Interface

</th><th align="left" id="d126470e675">

Action

</th></tr></thead><tbody><tr><td id="d126470e681">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.
2.  Select **New**.
3.  Select **PagerDuty Integration Profile**.


</td></tr><tr><td id="d126470e723">

**Software Asset Workspace**

</td><td>

1.  Navigate to **License operations** &gt; **User Subscriptions** &gt; **Direct integration profiles**.
2.  Select **New**.
3.  Select **PagerDuty** from the drop-down list.
4.  Select **Continue**.


</td></tr></tbody>
</table>2.  On the form, fill in the fields.

<table id="table_rhz_kgr_xnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display Name

</td><td>

Name of the integration profile. For example, `PagerDuty Integration`.

</td></tr><tr><td>

Status

</td><td>

Status of the integration profile.-   If you have not published the integration profile, this field is automatically set to `Draft`.
-   If you have already published the integration profile, this field is automatically set to `Published`.


</td></tr><tr><td>

Profile Type

</td><td>

Type of integration profile. This field is automatically set to `PagerDuty Subscription`.

</td></tr></tbody>
</table>3.  Review the required user roles or API permissions specified in the **Vendor configuration** field for each process to minimize security risks and optimize SaaS licenses.

    **Note:** For more information, see [Minimal user permissions](integrate-with-pagerduty.md#) table.

    1.  In the Download Subscription Subflow section, verify that the **Subflow** field is set to **PagerDuty Download Subscriptions**.

        **Note:** The **Download subscriptions** check box is selected by default and you can't clear it.

    2.  In the Calculate Activity Subflow section, verify that the **Subflow** field is set to **PagerDuty Update User Activity**.

        **Note:** The **Download Activity** check box is selected by default. If you clear it, the activity scheduled job **SAM - Refresh &lt;displayname&gt; Activity** isn't created.

        In the **Analyze user activity** field, you can also select the date and time starting from when you want to analyze the user activity. By default, you can analyze user activity up to 60 days prior to the current date and view events performed by individual users from the time you create this profile.

        **Note:** Software Asset Management pulls the events from the time that you start analyzing user activity irrespective of the profile creation date.

        You can modify this value in the Last activity threshold field of your software reclamation rules. For more information, see [Review a software reclamation rule](../task/add-reclamation-rule-sub.md).

    3.  In the Reclaim Subscription Subflow section, verify that the **Subflow** field is set to **PagerDuty Reclaim Subscription**.

        **Note:** The **Reclaim subscriptions** check box is selected by default. If you don't want to reclaim subscriptions, you can clear this check box. If you clear it, the removal candidates are created but the reclaim subscription subflow isn't triggered or the reclamation process isn't initiated.

4.  Select **Save**.

    Your ServiceNow instance creates a draft integration profile.

    The **Connection &amp; Credential** field appears and is automatically set to **sn\_pagerduty\_spoke.PagerDuty**.

5.  Open the connection &amp; credential aliases record by selecting the preview icon ![](../image/preview-icon.png) next to the **Connection &amp; Credential** field and then selecting **Open Record** in the record preview.

6.  On the Connection &amp; Credential Aliases form, select the **Create New Connection &amp; Credential** related link.

7.  In the dialog box, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the connection. For example, `PagerDuty Connection`.|
    |OAuth Client ID|Client ID that is assigned to your PagerDuty application.|
    |OAuth Client Secret|Client secret that is assigned to your PagerDuty application.|
    |OAuth Redirect URL|URL of the OAuth provider that users are redirected to after authentication. Enter `https://<*instance-name*>/oauth_redirect.do`, where &lt;*instance-name*&gt; is the name of your ServiceNow instance.|

8.  Select **Create and Get OAuth Token**.

    **Note:** For the role required to perform this step, refer to the [Minimal user permissions](integrate-with-pagerduty.md#) table.

    You’re redirected to the PagerDuty Accounts page.

9.  Select the same PagerDuty account that you used to create your PagerDuty application.

10. When you’re prompted to Authorize &lt;*pagerduty-app-name*&gt; to use your account, select **Submit Consent**.

    Your ServiceNow instance creates an OAuth token for PagerDuty and then automatically returns you to the Integration Profile form.

11. On the integration profile form, select **Validate Connection** to verify the connection and credential details of this integration.

    Validating the connection verifies the Download Subscriptions and Calculate Activity APIs, but not the Reclaim Subscriptions APIs.

12. After the connection is verified, select **Publish**.

13. In the Publish Confirmation dialog box, select **OK**.

    **Note:** If you clear the **Download Activity** check box after the integration profile is published, you must revalidate the connections and then republish the integration profile because the following events occur:

    -   The **Status** field on the integration profile form changes to **Draft**.
    -   The **Validate connection** button shows up on the form.
    -   The current **SAM - Refresh &lt;displayname&gt; Activity** job gets deleted.

### What to do next

After the integration connects, your ServiceNow instance automatically creates software models, reclamation rules, and software subscriptions that are refreshed daily.

After creating an integration profile, view information about the profile in the Software Asset Workspace by navigating to **License operations** &gt; **User subscription** &gt; **Direct integration profiles**. You can select an integration profile to view the following related lists. If the following related lists aren't visible for an integration profile in the default view, you can select the custom integration view from the Details tab:

-   Software Models
-   Unrecognized Subscription Identifiers
-   Scheduled Jobs
-   Scheduled Job Results
-   Software Subscriptions
-   Subscription Identifier Exclusion Rule
-   Subscription User Exclusion Rule

After creating an integration profile, you can define subscription exclusion rules to keep certain subscriptions from license cost calculations. For more information, see [Subscription exclusions for SaaS and SSO applications](subscription-exclusions.md#).

If you want to set up multiple integration profiles with unique connections, create child aliases to manage different configurations and settings for each integration profile. For more information, see [Create a child alias to set up multiple integration profiles](../reuse/create-child-alias-saas.md).

Review all automatically generated reclamation rules to reclaim user subscriptions. For more information, see [Review a software reclamation rule](../task/add-reclamation-rule-sub.md).

Create software entitlements for the automatically generated software models to track used software against owned software.

-   For more information on creating software entitlements in the Software Asset Management Core UI, see [Create entitlements in Software Asset Management classic](../task/track-software-rights.md).
-   For more information on creating software entitlements in the Software Asset Workspace, see [Create entitlements in workspace](../task/create-entitlements-workspace.md).
-   For more information on creating software entitlements using the Software Asset Management Playbook, see [Create entitlements using the guided walk-through](../task/guidedwalk-workspace.md).

Reconciliation also runs on your subscriptions as a scheduled job or on-demand. You can view your reconciliation results in the [License Workbench](sam-license-workbench.md) \(Software Asset Management classic application\) or the [License usage view](sam-workspace-workbench.md) \(Software Asset Workspace\). Use these results to determine your license compliance position and to remediate any non-compliance.

-   For more information on running reconciliation in the Software Asset Management classic application, see [Run software reconciliation in Software Asset Management classic](../task/t_RunReconciliation.md).
-   For more information on running reconciliation in the Software Asset Workspace, see [Run software reconciliation in the workspace](../task/run-recon-workspace.md).

