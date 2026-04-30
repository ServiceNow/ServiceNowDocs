---
title: Integrating with Google Workspace
description: Integrating your Software Asset Management application with the Google Workspace service enables you to track your software subscriptions and to reclaim unused licenses.Create a new project in the Google API Console.Create an integration profile to track software subscriptions and optimize licensing for the Google Workspace service.
locale: en-US
release: xanadu
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2025-08-12"
reading_time_minutes: 6
breadcrumb: [Integrate with SaaS applications, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Integrating with Google Workspace

Integrating your Software Asset Management application with the Google Workspace service enables you to track your software subscriptions and to reclaim unused licenses.

**Note:** The Google Workspace integration supports the following products:

-   Google Apps
-   Google Vault SKUs
-   Archived User SKUs

For additional information about the Google Workspace service, see [Google Workspace Admin Help](https://support.google.com/a/?hl=en#topic=7570177).

**Important:** Minimize security risks and protect information by granting access only to the necessary user or API permissions.

<table id="table_box"><thead><tr><th>

Process

</th><th>

Required user role in the Google Workspace application

</th><th>

Authentication scopes

</th></tr></thead><tbody><tr><td>

Download subscriptions

</td><td>

Admin API privileges: Users Read

</td><td>

-   \[Admin SDK API\] `https://www.googleapis.com/auth/admin.directory.user.readonly`
-   \[Admin SDK API\] `https://www.googleapis.com/auth/admin.directory.domain.readonly`
-   \[Enterprise License Manager API\] `https://www.googleapis.com/auth/apps.licensing`

</td></tr><tr><td>

Pull user activity

</td><td>

Admin API privileges: Users Read

</td><td>

-   \[Admin SDK API\] `https://www.googleapis.com/auth/admin.directory.user.readonly`
-   \[Admin SDK API\] `https://www.googleapis.com/auth/admin.reports.usage.readonly`

</td></tr><tr><td>

Reclaim subscription

</td><td>

Super Administrator

</td><td>

-   \[Admin SDK API\] `https://www.googleapis.com/auth/admin.directory.user.readonly`
-   \[People SDK API\] `https://www.googleapis.com/auth/userinfo.email`
-   \[People SDK API\] `https://www.googleapis.com/auth/userinfo.profile`
-   \[Admin SDK API\]`https://www.googleapis.com/auth/admin.datatransfer.readonly`
-   \[Admin SDK API\]`https://www.googleapis.com/auth/admin.directory.user`

</td></tr></tbody>
</table>## Create a Google Workspace project

Create a new project in the Google API Console.

### Before you begin

Google Workspace Role required: Refer to the [Minimal user permissions](integrate-with-gsuite.md#) table.

### Procedure

1.  Log in to [Google API Console](https://console.developers.google.com).

2.  Select **Select a project** &gt; **New Project**.

3.  Enter a name for your project in the Project name, then select your Organization and Location.

4.  Select **Create**.

5.  Select the OAuth consent screen on the left navigation menu.

6.  Select **User Type** as **Internal** and select **Create**.

7.  Enter the App name and select User support email in the App information section.

8.  In Authorized domains, select the **ADD DOMAIN** button and add `service-now.com`.

9.  Enter Email addresses in the Developer contact information section.

10. Select **Save and Continue** to add scopes.

11. On the Scopes page, select the **Add or Remove Scopes** button.

12. In the Manually add scopes section, enter the following scopes by pasting them to the text area:

    -   `https://www.googleapis.com/auth/apps.licensing`
    -   `https://www.googleapis.com/auth/admin.directory.user`
    -   `https://www.googleapis.com/auth/admin.directory.user.readonly`
    -   `https://www.googleapis.com/auth/admin.directory.domain.readonly`
    -   `https://www.googleapis.com/auth/admin.datatransfer`
    -   `https://www.googleapis.com/auth/admin.datatransfer.readonly`
    -   `https://www.googleapis.com/auth/admin.reports.usage.readonly`
    -   `https://www.googleapis.com/auth/userinfo.profile`
    -   `https://www.googleapis.com/auth/userinfo.email`
13. Select **ADD TO TABLE** and then select **Update**.

14. Select **Save and Continue**.

15. Select **Credentials** on the left navigation menu and select **CREATE CREDENTIALS**.

16. Select **OAuth client ID**.

17. Fill out the form as shown and select **Create**.

<table id="table_tgs_fjf_1hb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Application type**Note:** Selecting a value for this field causes the remaining fields to be displayed.

</td><td>

Web application

</td></tr><tr><td>

Name

</td><td>

Any name of your choice

</td></tr><tr><td>

Authorized JavaScript origins

</td><td>

https://*instance*.service-now.com, where *instance* is the name of your ServiceNow instance

</td></tr><tr><td>

Authorized redirect URIs

</td><td>

https://*instance*.service-now.com/oauth\_redirect.do, where *instance* is the name of your ServiceNow instance

</td></tr></tbody>
</table>18. Select **OK**.

    You can now view your client ID and client secret that you would use in your ServiceNow instance.

    **Note:** Your client ID and client secret are sensitive. Don't share them.

19. Select **Library** on the left navigation menu.

    Search for and enable the following APIs:

    -   Enterprise License Manager API
    -   Admin SDK
    -   Google People API

## Create a Google Workspace integration profile

Create an integration profile to track software subscriptions and optimize licensing for the Google Workspace service.

### Before you begin

To create a Google Workspace integration profile, request the Software Asset Management - SaaS License Management plugin \(sn\_sam\_saas\_int\) from the [ServiceNow Store](https://store.servicenow.com/).

ServiceNow Role required: sam\_integrator or admin

### About this task

If you’re using Software Asset Workspace, the option to create the Google Workspace integration profile in Core UI is inactive.

### Procedure

1.  Navigate to the integration profile.

<table id="choicetable_o3p_z3k_qtb"><thead><tr><th align="left" id="d43496e698">

Interface

</th><th align="left" id="d43496e701">

Action

</th></tr></thead><tbody><tr><td id="d43496e707">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.
2.  Select **New**.
3.  Select **Google Workspace Integration Profile**.


</td></tr><tr><td id="d43496e749">

**Software Asset Workspace**

</td><td>

1.  Navigate to **License operations** &gt; **User Subscriptions** &gt; **Direct integration profiles**.
2.  Select **New**.
3.  Select **Google Workspace** from the drop-down list.
4.  Select **Continue**.


</td></tr></tbody>
</table>2.  On the form, fill in the fields.

    |Field|Value|
    |-----|-----|
    |Display name|Name of the integration profile. For example, `Google Workspace Integration`|
    |Client Id|Client ID for the OAuth application created in the SaaS admin account.|
    |Redirect url|URL of the OAuth provider that you're redirected to after authentication. This value is automatically populated.|
    |Client secret|Password associated with the client ID.|
    |Profile type|Type of integration profile. This value is automatically set to **Google Workspace Subscription**.|

3.  Select **Submit**.

4.  On the integration profile, select **Get OAuth Token**.

    **Note:** For the role required to perform this step, refer to the [Minimal user permissions](integrate-with-gsuite.md#) table.

5.  In the pop-up window, select your Google admin account and select **Allow**.

    **Note:** When user subscriptions are reclaimed, files from the reclaimed accounts are transferred to the admin account selected in this step. This account can be a different admin account than the one used to set up the integration. If you have to start transferring files to a new admin, you can select the **Get OAuth Token** related link again at any time to select a different admin account. After selecting a new admin, you can reclaim the old admin account to transfer all of their files to the new admin, including all previously reclaimed user files.


### Result

You can view events performed by individual users up to one year prior to the current date. For more information, see [Review a software reclamation rule](../task/add-reclamation-rule-sub.md).

**Note:** Software Asset Management pulls the events from the time that you start downloading user subscriptions irrespective of the profile creation date.

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

