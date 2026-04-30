---
title: Integrating with Trello
description: Integrating your Software Asset Management application with the Trello service enables you to track your software subscriptions and to reclaim unused licenses.Generate a Trello API key and token to get access to the Trello portal.Set up your ServiceNow instance to add the Trello API key and API token.Create an integration profile to track software subscriptions and optimize licensing for the Trello service.
locale: en-US
release: xanadu
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Integrate with SaaS applications, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Integrating with Trello

Integrating your Software Asset Management application with the Trello service enables you to track your software subscriptions and to reclaim unused licenses.

For more information about the Trello service, see [the Trello Developer guide](https://developer.atlassian.com/cloud/trello/).

**Important:** Minimize security risks and protect information by granting access only to the necessary user or API permissions.

|Process|Required user role in the Trello application|Authentication scopes|
|-------|--------------------------------------------|---------------------|
|Download subscriptions|Product admin|None|
|Pull user activity|Product admin|None|
|Reclaim subscription|Product admin|None|

## Generate Trello API key and token

Generate a Trello API key and token to get access to the Trello portal.

### Before you begin

Trello Role required: Refer to the [Minimal user permissions](integrate-with-trello.md#) table.

Verify that you have a managed user account and Atlassian admin access.

### Procedure

1.  Go to [Trello](https://trello.com/).

2.  Log in as an enterprise admin.

3.  Go to [Developer API Keys](https://trello.com/app-key).

4.  Copy the API key from Personal Key on the Developer API keys page.

5.  In the following link, replace \{YourAPIKey\} with the API key that you copied in the last step and open the link.

    `https://trello.com/1/authorize?expiration=never&scope=read,write,account&response_type=token&name=ServerToken&key={YourAPIKey}`

    For example, if your API key is 123xyz, then open the following link- `https://trello.com/1/authorize?expiration=never&scope=read,write,account&response_type=token&name=ServerToken&key=123xyz`

    The MyPersonalToken page appears and asks if you want to give access to your account.

6.  Select **Allow**.

    An API token is generated. Copy this API token and store it securely.


## Create a Trello connection

Set up your ServiceNow instance to add the Trello API key and API token.

### Before you begin

ServiceNow Role required: admin

### Procedure

1.  Log in to your ServiceNow instance.

2.  Navigate to **Process Automation** &gt; **Flow Designer**.

3.  Select the **Connections** tab.

4.  Locate the Trello Alias connection alias and select **View Details**.

5.  Configure the Trello spoke.

    -   If you’re configuring the spoke for the first time, select **Configure**.
    -   If you aren't configuring the spoke for the first time, select **Edit**.
6.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Connection Name|Name to identify the connection record.|
    |Connection URL|Enter the URL as `https://api.trello.com/`.|
    |API Key|The API key that you copied from the Trello portal.|
    |API Token|The API token that you copied from the Trello portal.|

7.  Select **Configure Connection**.


## Create a Trello integration profile

Create an integration profile to track software subscriptions and optimize licensing for the Trello service.

### Before you begin

To create a Trello integration profile, request the Software Asset Management - SaaS License Management plugin \(sn\_sam\_saas\_int\) from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

ServiceNow Role required: admin or sam\_integrator and sn\_trello\_spoke.trello\_admin

### About this task

If you’re using Software Asset Workspace, the option to create the Trello integration profile in Core UI is inactive.

### Procedure

1.  Navigate to the integration profile.

<table id="choicetable_o3p_z3k_qtb"><thead><tr><th align="left" id="d79779e570">

Interface

</th><th align="left" id="d79779e573">

Action

</th></tr></thead><tbody><tr><td id="d79779e579">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.
2.  Select **New**.
3.  Select **Trello Enterprise Integration Profile**.


</td></tr><tr><td id="d79779e621">

**Software Asset Workspace**

</td><td>

1.  Navigate to **License operations** &gt; **User Subscriptions** &gt; **Direct integration profiles**.
2.  Select **New**.
3.  Select **Trello Enterprise** from the drop-down list.
4.  Select **Continue**.


</td></tr></tbody>
</table>2.  On the form, fill in the fields.

<table id="table_qzs_lcy_gpb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display Name

</td><td>

Name of the integration profile.For example, `Trello Integration`.

</td></tr><tr><td>

Status

</td><td>

Status of the integration profile.-   If you haven’t published the integration profile, this field is automatically set to  Draft.
-   If you’ve already published the integration profile, this field is automatically set to  Published.


</td></tr><tr><td>

Profile Type

</td><td>

This field is automatically set to **Trello Enterprise Subscription**.

</td></tr><tr><td>

Download Subscription Subflow

</td><td>

This field is automatically set to `Trello Download Subscriptions`.You can view events performed by individual users up to one year prior to the current date. For more information, see [Review a software reclamation rule](../task/add-reclamation-rule-sub.md).

**Note:** Software Asset Management pulls the events from the time that you start downloading user subscriptions irrespective of the profile creation date.

</td></tr><tr><td>

Reclaim Subscription Subflow

</td><td>

This field is automatically set to `Trello Reclaim Subscription`.

</td></tr></tbody>
</table>3.  Select **Save**.

4.  After the Trello form is saved, select **Publish**.


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

