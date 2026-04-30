---
title: Integrating with Looker
description: Integrating your Software Asset Management application with the Looker, a Google Cloud application enables you to track your software subscriptions and to reclaim unused licenses.Configure API key settings to manage and retrieve Looker API keys.Create a connection between your Looker applications and your ServiceNow instance so that your instance can retrieve user data from your applications.Create a Looker integration profile to track software subscriptions and optimize licensing for your Looker solutions.
locale: en-US
release: xanadu
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Integrate with SaaS applications, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Integrating with Looker

Integrating your Software Asset Management application with the Looker, a Google Cloud application enables you to track your software subscriptions and to reclaim unused licenses.

**Important:** Minimize security risks and protect information by granting access only to the necessary user or API permissions.

|Process|Required user role in the Box application|Authentication scopes|
|-------|-----------------------------------------|---------------------|
|Download subscriptions|User with see\_users permission|None|
|Pull user activity|User with see\_users permission|None|
|Reclaim subscription|admin|None|

## Configure Looker API key settings

Configure API key settings to manage and retrieve Looker API keys.

### Before you begin

Looker Role required: admin

### Procedure

1.  Log in to your Looker \(`https://<instancename>.looker.com/`\) instance.

2.  Select the gear icon to open Admin settings.

3.  Select **Users** &gt; **Open the admin user account**.

4.  Select **Edit API3 Keys** under the Profile tab.

5.  Select **New API3 Key**.

6.  Copy the Client ID and Client secret for later use.


## Create a Looker connection

Create a connection between your Looker applications and your ServiceNow instance so that your instance can retrieve user data from your applications.

### Before you begin

ServiceNow Role required: admin

### Procedure

1.  Log in to your ServiceNow instance.

2.  Navigate to **Connection &amp; Credentials** &gt; **Connection &amp; Credentials Aliases**.

3.  Locate your Looker connection and select **Create New Connection &amp; Credential**.

4.  In the dialog box, fill in the fields.

    |Field|Value|
    |-----|-----|
    |Connection Information|
    |Connection Name|Name of the Looker connection. This field populates automatically.|
    |Connection URL|URL for the connection. This field is automatically set to `https://<instance name>.looker.com`.|
    |Credential Information|
    |OAuth Client ID|Client ID that you generated while configuring the Looker API settings.|
    |OAuth Client Secret|Client Secret that you generated while configuring the Looker API settings.|
    |OAuth Redirect URL|`https://<instance name>/oauth_redirect.do`, where instance name is the name of your ServiceNow instance.|

5.  Select **Create and Get OAuth Token**.

    **Note:** For the role required to perform this step, refer to the [Minimal user permissions](integrate-with-looker.md#) table.


## Create a Looker integration profile

Create a Looker integration profile to track software subscriptions and optimize licensing for your Looker solutions.

### Before you begin

The Software Asset Management - SaaS License Management plugin \(sn\_sam\_saas\_int\) must be installed from the [ServiceNow Store](https://store.servicenow.com/).

ServiceNow Role required: admin or sam\_integrator

### About this task

If you are using Software Asset Workspace, the option to create the Looker integration profile in Core UI is inactive.

### Procedure

1.  Navigate to the integration profile.

<table id="choicetable_o3p_z3k_qtb"><thead><tr><th align="left" id="d138278e544">

Interface

</th><th align="left" id="d138278e547">

Action

</th></tr></thead><tbody><tr><td id="d138278e553">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.
2.  Select **New**.
3.  Select **Looker Integration Profile**.


</td></tr><tr><td id="d138278e595">

**Software Asset Workspace**

</td><td>

1.  Navigate to **License operations** &gt; **User Subscriptions** &gt; **Direct integration profiles**.
2.  Select **New**.
3.  Select **Looker** from the drop-down list.
4.  Select **Continue**.


</td></tr></tbody>
</table>2.  On the form, fill in the fields.

<table id="table_tzy_rt5_pqb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Display name

</td><td>

Name of the integration profile. For example, Looker integration.

</td></tr><tr><td>

Connection &amp; Credential

</td><td>

Connection and credential alias for the Looker spoke. This field is automatically set to sn\_looker\_spoke.Looker.

</td></tr><tr><td>

Status

</td><td>

Status of the integration profile. -   If you have not published the integration profile, this field is automatically set to  Draft.
-   If you have already published the integration profile, this field is automatically set to  Published.


</td></tr><tr><td>

Profile type

</td><td>

Type of integration profile. This field is automatically set to Looker Subscription.

</td></tr></tbody>
</table>3.  On the **Download Subscription Subflow** tab, verify that the **Subflow** field is set to Looker Download Subscriptions.

    You can view events performed by individual users up to one year prior to the current date. For more information, see [Review a software reclamation rule](../task/add-reclamation-rule-sub.md).

    **Note:** Software Asset Management pulls the events from the time that you start downloading user subscriptions irrespective of the profile creation date.

4.  On the **Reclaim Subscription Subflow** tab, verify that the **Subflow** field is set to Looker Reclaim Subscription.

5.  Select **Save**.

    A draft integration profile is created. The integration profile uses the Looker Download Subscriptions and Looker Reclaim Subscription subflows to retrieve user data from the Looker application.

6.  Select **Save**.

7.  After the page reloads, select **Publish**.


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

