---
title: Integrating with Trello
description: Integrating your Software Asset Management application with the Trello service enables you to track your software subscriptions and to reclaim unused licenses.Generate a Trello API key and token to get access to the Trello portal.Create an integration profile to track software subscriptions and optimize licensing for the Trello service.
locale: en-US
release: australia
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 6
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


## Create a Trello integration profile

Create an integration profile to track software subscriptions and optimize licensing for the Trello service.

### Before you begin

To create a Trello integration profile, request the Software Asset Management - SaaS License Management plugin \(sn\_sam\_saas\_int\) from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

ServiceNow Role required: sam\_integrator and sn\_trello\_spoke.trello\_admin

**Important:** You must select the **Trello Spoke** check box for this integration while installing optional features on the [Application Manager](https://www.servicenow.com/docs/access?context=application-manager&version=australia&pubname=australia-platform-administration&ft:locale=en-US) page. For more information about choosing the required SaaS applications, see [Request SaaS License Management](../task/request-saas-license-management.md).

### About this task

If you’re using Software Asset Workspace, the option to create the Trello integration profile in Core UI is inactive.

### Procedure

1.  Navigate to the integration profile.

<table id="choicetable_o3p_z3k_qtb"><thead><tr><th align="left" id="d93462e380">

Interface

</th><th align="left" id="d93462e383">

Action

</th></tr></thead><tbody><tr><td id="d93462e389">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.
2.  Select **New**.
3.  Select **Trello Enterprise Integration Profile**.


</td></tr><tr><td id="d93462e431">

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

Status of the integration profile.-   If you haven’t published the integration profile, this field is automatically set to  **Draft**.
-   If you’ve already published the integration profile, this field is automatically set to  **Published**.


</td></tr><tr><td>

Profile Type

</td><td>

This field is automatically set to **Trello Enterprise Subscription**.

</td></tr></tbody>
</table>3.  Review the required user roles or API permissions to minimize security risks and optimize SaaS licenses.

    **Note:** For more information, see [Minimal user permissions](integrate-with-trello.md#) table.

    1.  In the Download Subscription Subflow section, verify that the **Subflow** field is set to **Trello Download Subscriptions**.

        **Note:** The **Download subscriptions** check box is selected by default and you can't clear it.

    2.  In the Reclaim Subscription Subflow section, verify that the **Subflow** field is set to **Trello Reclaim Subscription**.

        **Note:** The **Reclaim subscriptions** check box is selected by default. If you don't want to reclaim subscriptions, you can clear this check box. If you clear it, the removal candidates are created but the reclaim subscription subflow isn't triggered or the reclamation process isn't initiated.

4.  Select **Save**.

    A draft integration profile is created.

    The **Connection &amp; Credential** field appears and is automatically set to **sn\_trello\_spoke.Trello\_Alias**.

5.  In the **Download Subscription Subflow** tab, select the preview icon \(![Preview icon](../../../common/image/Form_ReferenceLookupIcon.png)\) next to the **Connection &amp; Credential** field and then select **Open Record** in the record preview.

6.  Select the **Create New Connection &amp; Credential** related link.

7.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Connection Name|Name to identify the connection record.|
    |Connection URL|Enter the URL as `https://api.trello.com/`.|
    |API Key|The API key that you copied from the Trello portal.|
    |API Token|The API token that you copied from the Trello portal.|

8.  Select **Create**.

9.  On the integration profile form, select **Validate Connection** to verify the connection and credential details of this integration.

    Validating the connection verifies the Download Subscriptions APIs, but not the Reclaim Subscriptions APIs.

10. Select **Publish**.

11. In the Publish Confirmation dialog box, select **OK**


### What to do next

After the integration connects, your ServiceNow instance automatically creates software models, reclamation rules, and software subscriptions that are refreshed daily.

After creating an integration profile, view information about the profile in the Software Asset Workspace by navigating to **License operations** &gt; **User subscription** &gt; **Direct integration profiles**. You can select an integration profile to view the following related lists. If all of the following related lists aren't visible for an integration profile in the default view, you can select the custom integration view from the Details tab:

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

