---
title: Integrating with monday.com
description: Integrating your Software Asset Management application with monday.com enables you to track your software subscriptions and to reclaim unused licenses.Create a monday OAuth2 application to authorize access to the monday.com API.Create a monday.com integration profile to track software subscriptions and optimize licensing for your monday applications.
locale: en-US
release: xanadu
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Integrate with SaaS applications, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Integrating with monday.com

Integrating your Software Asset Management application with monday.com enables you to track your software subscriptions and to reclaim unused licenses.

**Important:** Minimize security risks and protect information by granting access only to the necessary user or API permissions.

|Process|Required user role in the monday.com application|Authentication scopes|
|-------|------------------------------------------------|---------------------|
|Download subscriptions|Member|users:read|
|Pull user activity|Member|users:read|

## Create a monday OAuth2 application

Create a monday OAuth2 application to authorize access to the monday.com API.

### Before you begin

monday.com Role required: Refer to the [Minimal user permissions](integrate-with-monday.md#) table.

### About this task

A monday application enables you to build workflows, user experiences, and products on top of the existing monday.com work operating system \(Work OS\). When you configure a monday application to use OAuth2, access is granted to the monday.com API so that it can read and modify user data.

### Procedure

1.  From a web browser, go to [monday.com](https://monday.com/).

2.  Log in using your admin credentials.

3.  Select your profile icon and then select **Developers**.

    The My Apps page opens.

4.  Select **Create App**.

    The Basic Information page for the new application opens.

5.  In the Display Information section, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the monday application.|
    |Short Description|Description of the application.|

6.  In the same section, add your own application icon by selecting the auto-generated icon and then selecting an icon image.

    You can also change the icon color by selecting **App Color** and then selecting either a preset or custom color. If you don’t add your own application icon or select an icon color, the application uses the auto-generated icon and default icon color.

7.  In the App Credentials section, copy the values in the **Client ID** and **Client Secret** fields.

    Save them in a secure location for later use.

8.  Select **Save App**.

9.  From the left navigation menu of the new application, navigate to **General** &gt; **OAuth**.

    The **Scopes** tab of the OAuth &amp; Permissions page opens.

10. In the Scopes section, specify how the application can access or use different types of user data by selecting the check box for the **users:read** OAuth scope.

11. Select **Save Feature**.

12. Select the **Redirect URLs** tab of the OAuth &amp; Permissions page.

13. In the Redirect URLs section, enter the URL of the OAuth provider that users are redirected to after authentication.

    Enter `https://*instance*.service-now.com/oauth_redirect.do`, where &lt;*instance*&gt; is the name of your ServiceNow instance.

14. Select **Save Feature**.


## Create a monday.com integration profile

Create a monday.com integration profile to track software subscriptions and optimize licensing for your monday applications.

### Before you begin

To create a monday.com integration profile, request the Software Asset Management - SaaS License Management plugin \(sn\_sam\_saas\_int\) from the [ServiceNow Store](https://store.servicenow.com/).

ServiceNow Role required: sam\_integrator or admin

### About this task

If you’re using Software Asset Workspace, the option to create the monday.com integration profile in Core UI is inactive.

### Procedure

1.  Navigate to the integration profile.

<table id="choicetable_o3p_z3k_qtb"><thead><tr><th align="left" id="d250394e500">

Interface

</th><th align="left" id="d250394e503">

Action

</th></tr></thead><tbody><tr><td id="d250394e509">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.
2.  Select **New**.
3.  Select **monday.com Integration Profile**.


</td></tr><tr><td id="d250394e551">

**Software Asset Workspace**

</td><td>

1.  Navigate to **License operations** &gt; **User Subscriptions** &gt; **Direct integration profiles**.
2.  Select **New**.
3.  Select **monday.com** from the drop-down list.
4.  Select **Continue**.


</td></tr></tbody>
</table>2.  On the form, fill in the fields.

<table id="table_v44_nq1_wmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display Name

</td><td>

Name of the integration profile. For example, `monday.com Integration`.

</td></tr><tr><td>

Connection &amp; Credential

</td><td>

Connection and credential alias for the monday.com spoke. This field is automatically set to **sn\_monday\_com\_spok.Monday**.

</td></tr><tr><td>

Status

</td><td>

Status of the integration profile.-   If you have not published the integration profile, this field is automatically set to **Draft**.
-   If you have already published the integration profile, this field is automatically set to **Published**.


</td></tr><tr><td>

Profile Type

</td><td>

Type of integration profile.This field is automatically set to **monday.com Subscription**.

</td></tr></tbody>
</table>3.  On the **Download Subscription Subflow** tab, verify that the **Subflow** field is set to **monday.com Download Subscriptions Subflow**.

4.  Select **Save**.

    Your ServiceNow instance creates a draft integration profile. The integration profile uses the monday.com Download Subscriptions and monday.com Update User Activity subflows to retrieve user data from your monday applications.

5.  Open the connection &amp; credential aliases record by selecting the preview icon \(![Preview icon.](../image/preview-icon.png)\) next to the **Connection &amp; Credential** field and then selecting **Open Record** in the record preview.

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

Base URL for the monday.com API. This field is automatically set to `https://api.monday.com/`.

</td></tr><tr><td>

OAuth Client ID

</td><td>

Client ID that is assigned to your monday application.

</td></tr><tr><td>

OAuth Client Secret

</td><td>

Client secret that is assigned to your monday application.

</td></tr><tr><td>

OAuth Redirect URL

</td><td>

URL of the OAuth provider that users are redirected to after authentication. This field populates automatically based on the redirect URL that you specified in [Create a monday OAuth2 application](integrate-with-monday.md#).

</td></tr></tbody>
</table>8.  Select **Create and Get OAuth Token**.

    **Note:** For the role required to perform this step, refer to the [Minimal user permissions](integrate-with-monday.md#) table.

9.  In the Authorize App dialog box, sign in using the same monday.com credentials that you used to create your monday application.

10. Select **Allow**.

    The dialog box closes and then you automatically return to the integration profile form.

11. Select **Publish**.


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

