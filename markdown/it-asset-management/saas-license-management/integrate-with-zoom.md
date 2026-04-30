---
title: Integrating with Zoom
description: Integrating your Software Asset Management application with the Zoom service enables you to track your software subscriptions and to reclaim unused licenses.Create an application in the Zoom App Marketplace.Create an integration profile to track software subscriptions and optimize licensing for the Zoom service.
locale: en-US
release: xanadu
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 6
breadcrumb: [Integrate with SaaS applications, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Integrating with Zoom

Integrating your Software Asset Management application with the Zoom service enables you to track your software subscriptions and to reclaim unused licenses.

With this integration, you can retrieve and analyze licensing information for the following Zoom applications:

-   Zoom Regular account \(not a Master / Master-sub account\) for Meetings
-   Zoom Regular account \(not a Master / Master-sub account\) for Webinar

For additional information about Zoom, see [Zoom Developer Documentation](https://marketplace.zoom.us/docs).

**Important:** Minimize security risks and protect information by granting access only to the necessary user or API permissions.

<table id="table_kcp_jts_nbc"><thead><tr><th>

Process

</th><th>

Required user role in the Zoom application

</th><th>

Authentication scopes

</th></tr></thead><tbody><tr><td>

Download subscriptions

</td><td>

View or edit user information \(e.g. assigning licenses and groups to users\): View

</td><td>

-   user:read:list\_users:admin
-   user:read:settings:admin

</td></tr><tr><td>

Pull user activity

</td><td>

View detailed usage reports for the account: View

</td><td>

-   report:read:user:admin

**Note:** If your installed Software Asset Management - SaaS License Management version is 14.0.4 or lower, use this scope. You mustn't use the meeting:read:list\_meetings:admin scope.

-   meeting:read:list\_meetings:admin

**Note:** If your installed Software Asset Management - SaaS License Management version is higher than 14.0.4, use this scope. You must not use the report:read:user:admin scope.

-   webinar:read:list\_webinars:admin

</td></tr><tr><td>

Reclaim subscription

</td><td>

View or edit user information \(e.g. assigning licenses and groups to users\): Edit

</td><td>

-   user:update:settings:admin
-   user:update:user:admin
-   user:delete:user:admin

</td></tr></tbody>
</table>## Create a Zoom application

Create an application in the Zoom App Marketplace.

### Before you begin

Zoom Role required: Zoom for developers: Edit

### Procedure

1.  Navigate to [Zoom App Marketplace](https://marketplace.zoom.us/) and sign in to your account.

2.  Select **Develop** &gt; **Build App**.

3.  In the **Select how the app is managed** section on the Basic Information page, select the **Admin-managed** option.

4.  Select **Save**.

5.  In the App Credentials section, obtain the Client ID and Client Secret.

    Copy and save these values in a secure location for later use.

    **Note:** Your Client ID and Client secret are sensitive. Don’t share them.

6.  Enter `https://*instance*.service-now.com/oauth_redirect.do` in the **OAuth Redirect URL** and **OAuth Allow Lists** fields, where *instance* is the name of your ServiceNow instance.

7.  Select the **Scopes** tab on the left navigation menu.

8.  Add the following scopes for enabling the integration to get a list of users, track meeting and webinar activity for users, and reclaim unused subscriptions.

    -   user:read:list\_users:admin
    -   user:read:settings:admin
    -   report:read:user:admin

        **Note:** If your installed Software Asset Management - SaaS License Management version is 14.0.4 or lower, use this scope. You mustn't use the meeting:read:list\_meetings:admin scope.

    -   meeting:read:list\_meetings:admin

        **Note:** If your installed Software Asset Management - SaaS License Management version is higher than 14.0.4, use this scope. You mustn't use the report:read:user:admin scope.

    -   webinar:read:list\_webinars:admin
    -   user:update:settings:admin
    -   user:update:user:admin
    -   user:delete:user:admin

## Create a Zoom integration profile

Create an integration profile to track software subscriptions and optimize licensing for the Zoom service.

### Before you begin

To create a Zoom integration profile, request the Software Asset Management - SaaS License Management plugin \(sn\_sam\_saas\_int\) from the [ServiceNow Store](https://store.servicenow.com/).

ServiceNow Role required: sam\_integrator or admin

### About this task

If you’re using Software Asset Workspace, the option to create the Zoom integration profile in Core UI is inactive.

### Procedure

1.  Navigate to the integration profile.

<table id="choicetable_o3p_z3k_qtb"><thead><tr><th align="left" id="d84991e482">

Interface

</th><th align="left" id="d84991e485">

Action

</th></tr></thead><tbody><tr><td id="d84991e491">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.
2.  Select **New**.
3.  Select **Zoom Integration Profile**.


</td></tr><tr><td id="d84991e533">

**Software Asset Workspace**

</td><td>

1.  Navigate to **License operations** &gt; **User Subscriptions** &gt; **Direct integration profiles**.
2.  Select **New**.
3.  Select **Zoom** from the drop-down list.
4.  Select **Continue**.


</td></tr></tbody>
</table>2.  On the form, fill in the fields.

    |Field|Value|
    |-----|-----|
    |Display name|Name of the integration profile. For example, `Zoom Integration`|
    |Client Id|Client ID for the OAuth application created in the SaaS admin account in [step 5](integrate-with-zoom.md#step5).|
    |Redirect url|This value is automatically populated.|
    |Client secret|Password related with the client ID created in the SaaS admin account in [step 5](integrate-with-zoom.md#step5).|
    |Profile type|Type of integration profile. This value is automatically set to `Zoom Subscription`.|
    |Analyze user activity from|You can choose to start analyzing data from the current date or from up to 30 days in the past. Choosing a date in the past enables you to detect stale subscriptions without waiting in real time because you can see subscriptions that haven't been used recently. Because choosing a date in the past increases the amount of data that is analyzed, it could take several hours for you to be able to view the results.|

3.  Select **Submit**.

4.  On the integration profile, select the **Get OAuth Token** related link and follow the steps to get an OAuth token.

    **Note:** For the role required to perform this step, refer to the [Minimal user permissions](integrate-with-zoom.md#) table.


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

