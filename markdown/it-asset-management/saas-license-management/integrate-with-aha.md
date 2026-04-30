---
title: Integrating with Aha!
description: Integrating your Software Asset Management application with the Aha! service enables you to track your software subscriptions and to reclaim unused licenses.Create an Aha! OAuth2 application to get access to the Aha! API.Set up your ServiceNow instance to add the Aha! Client ID and Client Secret keys.Create an integration profile to track software subscriptions and optimize licensing for the Aha! service.
locale: en-US
release: xanadu
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Integrate with SaaS applications, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Integrating with Aha!

Integrating your Software Asset Management application with the Aha! service enables you to track your software subscriptions and to reclaim unused licenses.

For more information about the Aha! service, see [Aha! Product management guide](https://www.aha.io/roadmapping/guide).

**Important:** Minimize security risks and protect information by granting access only to the necessary user or API permissions.

|Process|Required user role in the Aha! application|Authentication scopes|
|-------|------------------------------------------|---------------------|
|Download subscriptions|admin|None|
|Pull user activity|admin|None|
|Reclaim subscription|admin|None|

## Create an Aha! OAuth2 application

Create an Aha! OAuth2 application to get access to the Aha! API.

### Before you begin

Aha! Role required: admin

### Procedure

1.  Go to [OAuth2 Authentication](https://www.aha.io/api/oauth2).

2.  Log in to the Aha! site using your admin credentials.

3.  On the Personal settings page, select **Developer**.

4.  Select the **OAuth applications** tab.

5.  Select **Register OAuth application**.

6.  On the Register new OAuth application form, enter `https://*instance*/oauth_redirect.do` as the Redirect URI, where *instance* is the name of your ServiceNow instance.

7.  Select **Create**.

    The **OAuth applications** tab shows Client ID and Client Secret keys.

8.  Note down the values in the Client ID and Client Secret fields.


## Set up ServiceNow instance for Aha!

Set up your ServiceNow instance to add the Aha! Client ID and Client Secret keys.

### Before you begin

ServiceNow Role required: admin or sam\_integrator

### Procedure

1.  Log in to your ServiceNow instance.

2.  Navigate to **Connection &amp; Credentials** &gt; **Connection &amp; Credentials Aliases**.

    Connection &amp; Credentials Aliases page appears and shows the list of apps.

3.  Locate and open the Connection &amp; Credentials record for Aha!.

4.  Select the **Create New Connection &amp; Credential** related link.

5.  On the Create Connection and add Credential form, fill in the details.

    |Fields|Descriptions|
    |------|------------|
    |Connection Name|Name of the integration profile.|
    |Connection URL|Connection URL for Aha!.|
    |OAuth Client ID|OAuth2 key that you received while creating an OAuth2 authentication from the Aha! site.|
    |OAuth Client Secret|OAuth Client Secret key that you received while creating an OAuth2 authentication from the Aha! site.|
    |OAuth Redirect URL|ServiceNow redirect URL.|

6.  Select **Configure and get OAuth Token** and then select **Authorize**.

    **Note:** For the role required to perform this step, refer to the [Minimal user permissions](integrate-with-aha.md#) table.


## Create an Aha! integration profile

Create an integration profile to track software subscriptions and optimize licensing for the Aha! service.

### Before you begin

To create an Aha! integration profile, request the Software Asset Management - SaaS License Management plugin \(sn\_sam\_saas\_int\) from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

ServiceNow Role required: sam\_integrator or admin

### About this task

If you’re using Software Asset Workspace, the option to create the Aha! integration profile in Core UI is inactive.

### Procedure

1.  Navigate to the integration profile.

<table id="choicetable_o3p_z3k_qtb"><thead><tr><th align="left" id="d246371e583">

Interface

</th><th align="left" id="d246371e586">

Action

</th></tr></thead><tbody><tr><td id="d246371e592">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.
2.  Select **New**.
3.  Select **Aha Integration Profile**.


</td></tr><tr><td id="d246371e634">

**Software Asset Workspace**

</td><td>

1.  Navigate to **License operations** &gt; **User Subscriptions** &gt; **Direct integration profiles**.
2.  Select **New**.
3.  Select **Aha!** from the drop-down list.
4.  Select **Continue**.


</td></tr></tbody>
</table>2.  In the **Display name** field, enter a display name of your choice.

    On the form, the following fields are automatically populated.

<table id="table_qzs_lcy_gpb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Connection &amp; Credential Alias

</td><td>

sn\_aha\_spoke.Aha\_

</td></tr><tr><td>

Status

</td><td>

Draft

</td></tr><tr><td>

Profile Type

</td><td>

Aha! Subscription

</td></tr><tr><td>

Download Subscription Subflow

</td><td>

Aha! Download SubscriptionYou can view events performed by individual users up to one year prior to the current date. For more information, see [Review a software reclamation rule](../task/add-reclamation-rule-sub.md).

**Note:** Software Asset Management pulls the events from the time that you start downloading user subscriptions irrespective of the profile creation date.

</td></tr><tr><td>

Reclaim Subscription Subflow

</td><td>

Aha! Reclaim Subscription

</td></tr></tbody>
</table>3.  Select **Create and Get OAuth Token**.

4.  After the Aha! form is saved, select **Publish**.


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

