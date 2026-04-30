---
title: Integrating with Rally
description: Integrating your Software Asset Management application with the Broadcom Rally application enables you to track your software subscriptions and to reclaim unused licenses.Register the Rally OAuth application to access the Rally API 2.0 and to receive a Client ID and Client secret.Create a connection between your Rally applications and your ServiceNow instance so that your instance can retrieve user data from your applications.Create a Rally integration profile to track software subscriptions and optimize licensing for your Rally solutions.
locale: en-US
release: xanadu
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Integrate with SaaS applications, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Integrating with Rally

Integrating your Software Asset Management application with the Broadcom Rally application enables you to track your software subscriptions and to reclaim unused licenses.

**Important:** Minimize security risks and protect information by granting access only to the necessary user or API permissions.

|Process|Required user role in the Rally application|Authentication scopes|
|-------|-------------------------------------------|---------------------|
|Download subscriptions|Workspace admin|None|
|Pull user activity|Workspace admin|None|
|Reclaim subscription|Workspace admin|None|

## Register a Rally OAuth application

Register the Rally OAuth application to access the Rally API 2.0 and to receive a Client ID and Client secret.

### Before you begin

The Rally Integration Hub spoke must be active. For more information, see [Rally spoke](https://www.servicenow.com/docs/access?context=rally-spoke&version=xanadu&pubname=xanadu-integrate-applications&ft:locale=en-US).

Rally Role required: Refer to the [Minimal user permissions](integrate-with-rally.md#) table.

### Procedure

1.  Log in to [CA Agile Central](https://rally1.rallydev.com/login/accounts/index.html) by using your admin credentials.

2.  On the page header, select your profile and then select **My Settings**.

3.  Navigate to **Access** &gt; **OAUTH CLIENTS**.

4.  Select **Create**.

5.  In the dialog box, fill in the fields.

    |Field|Value|
    |-----|-----|
    |Application Name|Provide a name for the application.|
    |Callback URL|Callback URL of the ServiceNow instance to which the application is to be integrated. For example, `https://<instance_url>/oauth_redirect.do`.|

6.  Select **Next**.

7.  Copy the Client ID and Client secret for later use.


## Create a Rally connection

Create a connection between your Rally applications and your ServiceNow instance so that your instance can retrieve user data from your applications.

### Before you begin

Role required: admin

### Procedure

1.  Log in to your ServiceNow instance.

2.  Navigate to **Connection &amp; Credentials** &gt; **Connection &amp; Credentials Aliases**.

3.  Locate your Rally connection and select **Create New Connection &amp; Credential**.

4.  In the Create Connection and Credential dialog box, fill in the fields.

    |Field|Value|
    |-----|-----|
    |Connection Information|
    |Connection Name|Name of the Rally connection. This field populates automatically.|
    |Connection URL|URL for the connection. This field is automatically set to `https://rally1.rallydev.com/slm/webservice`.|
    |Credential Information|
    |OAuth Client ID|Client ID that you generated while configuring Rally API settings.|
    |OAuth Client Secret|Client Secret that you generated while configuring Rally API settings.|
    |OAuth Redirect URL|`https://<instance_name>/oauth_redirect.do`, where instance name is the name of your ServiceNow instance.|

5.  Select **Create and Get OAuth Token**.

    **Note:** For the role required to perform this step, refer to the [Minimal user permissions](integrate-with-rally.md#) table.


## Create a Rally integration profile

Create a Rally integration profile to track software subscriptions and optimize licensing for your Rally solutions.

### Before you begin

The Software Asset Management - SaaS License Management plugin \(sn\_sam\_saas\_int\) must be installed from the [ServiceNow Store](https://store.servicenow.com/).

Role required: admin or sam\_integrator

### About this task

If you are using Software Asset Workspace, the option to create the Rally integration profile in Core UI is inactive.

### Procedure

1.  Navigate to the integration profile.

<table id="choicetable_o3p_z3k_qtb"><thead><tr><th align="left" id="d187216e631">

Interface

</th><th align="left" id="d187216e634">

Action

</th></tr></thead><tbody><tr><td id="d187216e640">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.
2.  Select **New**.
3.  Select **Rally Integration Profile**.


</td></tr><tr><td id="d187216e682">

**Software Asset Workspace**

</td><td>

1.  Navigate to **License operations** &gt; **User Subscriptions** &gt; **Direct integration profiles**.
2.  Select **New**.
3.  Select **Rally** from the drop-down list.
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

Name of the integration profile. For example, Rally integration.

</td></tr><tr><td>

Connection &amp; Credential

</td><td>

Connection and credential alias for the Rally spoke. This field is automatically set to sn\_rally\_spoke.Rally.

</td></tr><tr><td>

Status

</td><td>

Status of the integration profile. -   If you have not published the integration profile, this field is automatically set to  Draft.
-   If you have already published the integration profile, this field is automatically set to  Published.


</td></tr><tr><td>

Profile type

</td><td>

Type of integration profile. This field is automatically set to Rally Subscription.

</td></tr></tbody>
</table>3.  On the **Download Subscription Subflow** tab, verify that the **Subflow** field is set to Rally Download Subscriptions.

    You can view events performed by individual users up to one year prior to the current date. For more information, see [Review a software reclamation rule](../task/add-reclamation-rule-sub.md).

    **Note:** Software Asset Management pulls the events from the time that you start downloading user subscriptions irrespective of the profile creation date.

4.  On the **Reclaim Subscription Subflow** tab, verify that the **Subflow** field is set to Rally Reclaim Subscription.

5.  Select **Save**.

    A draft integration profile is created. The integration profile uses the Rally Download Subscriptions and Rally Reclaim Subscription subflows to retrieve user data from the Rally application.

6.  After the page reloads, select **Publish**.


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

