---
title: Integrating with Workplace from Facebook
description: Integrating your Software Asset Management application with the Workplace from Facebook application enables you to track your software subscriptions and reclaim unused licenses.Create an integration profile to track software subscriptions and optimize licensing for the Workplace from Facebook application.
locale: en-US
release: xanadu
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [Integrate with SaaS applications, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Integrating with Workplace from Facebook

Integrating your Software Asset Management application with the Workplace from Facebook application enables you to track your software subscriptions and reclaim unused licenses.

**Important:** Minimize security risks and protect information by granting access only to the necessary user or API permissions.

<table id="table_box"><thead><tr><th>

Process

</th><th>

Required user role in the Workplace from Facebook application

</th><th>

Authentication scopes

</th></tr></thead><tbody><tr><td>

Download subscriptions

</td><td>

System admin

</td><td>

-   Read group membership
-   Manage work profiles

</td></tr><tr><td>

Pull user activity

</td><td>

System admin

</td><td>

-   Read group
-   Read group membership
-   Read group content
-   Read All messages
-   Read Knowledge Library content

</td></tr><tr><td>

Reclaim subscription

</td><td>

System admin

</td><td>

Provision User Accounts

</td></tr></tbody>
</table>## Create a Workplace from Facebook integration profile

Create an integration profile to track software subscriptions and optimize licensing for the Workplace from Facebook application.

### Before you begin

To create a Workplace from Facebook integration profile, request the Software Asset Management - SaaS License Management plugin \(sn\_sam\_saas\_int\) from the [ServiceNow Store](https://store.servicenow.com/).

ServiceNow Role required: admin or sam\_integrator

### About this task

If you’re using Software Asset Workspace, the option to create the Workplace from Facebook integration profile in Core UI is inactive.

### Procedure

1.  Navigate to the integration profile.

<table id="choicetable_o3p_z3k_qtb"><thead><tr><th align="left" id="d142195e236">

Interface

</th><th align="left" id="d142195e239">

Action

</th></tr></thead><tbody><tr><td id="d142195e245">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.
2.  Select **New**.
3.  Select **Workplace from Facebook Integration Profile**.


</td></tr><tr><td id="d142195e287">

**Software Asset Workspace**

</td><td>

1.  Navigate to **License operations** &gt; **User Subscriptions** &gt; **Direct integration profiles**.
2.  Select **New**.
3.  Select **Workpace from Facebook** from the drop-down list.
4.  Select **Continue**.


</td></tr></tbody>
</table>2.  On the form, fill in the fields.

<table id="table_m4c_prp_qqb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Display name

</td><td>

Name of the integration profile. For example, Workplace from Facebook integration.

</td></tr><tr><td>

Connection and Credential

</td><td>

Connection and credential alias for  Workplace from Facebook. This field is automatically set to **sn\_fb\_wp\_spoke.FB\_Workplace\_Alias**.

</td></tr><tr><td>

Status

</td><td>

Status of the integration profile.-   If you have not published the integration profile, this field is automatically set to  **Draft**.
-   If you have already published the integration profile, this field is automatically set to  **Published**.


</td></tr><tr><td>

Profile type

</td><td>

Type of integration profile. This field is automatically set to Workplace from Facebook Subscription.

</td></tr></tbody>
</table>3.  On the **Download Subscription Subflow** tab, verify that the **Subflow** field is set to **Workplace from Facebook Download Subscriptions Subflow**.

4.  On the **Calculate Activity Subflow** tab, verify that the **Subflow** field is set to **Workplace from Facebook Update User Activity Subflow**.

    You can also select the date and time that you want to analyze user activity from in the Analyze user activity from field. By default, you can analyze user activity up to 60 days prior to the current date and view events performed by individual users from the time you create this profile.

    **Note:** Software Asset Management pulls the events from the time that you start analyzing user activity irrespective of the profile creation date.

    You can modify this value in the Last activity threshold field of your software reclamation rules. For more information, see [Review a software reclamation rule](../task/add-reclamation-rule-sub.md).

5.  On the **Reclaim Subscription Subflow** tab, verify that the **Subflow** field is set to **Workplace from Facebook Reclaim Subscription**.

6.  Select the preview icon \(![Preview icon.](../image/preview-icon.png)\) next to the **Connection &amp; Credential** field and select **Open Record** in the record preview to open the connection &amp; credential aliases record.

7.  On the **Connection &amp; Credential Aliases** form, select **FB\_Workplace\_Credentials** under the **Credential** column in the **Connections** list.

8.  On the **Workplace from Facebook Credentials** form, select **Install on your Workplace**.

    You get redirected to the [Workplace sign-up/sign-in](https://work.workplace.com/) page.

9.  Log in to your  Workplace from Facebook account using your credentials.

    The **Add ServiceNow Spoke to Workplace** pop-up window gets displayed.

10. Select **Add to Workplace**.

11. Select **Done**.

    You are redirected back to your  ServiceNow   instance and the relevant fields are updated.

12. Return to the integration profile and select **Publish**.


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

