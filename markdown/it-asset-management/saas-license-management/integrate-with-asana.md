---
title: Integrating with Asana
description: Integrating your Software Asset Management application with the Asana application enables you to track your software subscriptions and to reclaim unused licenses.Register an Asana OAuth application to access the Asana API 1.0 and to receive a Client ID and Client secret.Create an Asana integration profile to track software subscriptions and optimize licensing for your Asana solutions.
locale: en-US
release: australia
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Integrate with SaaS applications, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Integrating with Asana

Integrating your Software Asset Management application with the Asana application enables you to track your software subscriptions and to reclaim unused licenses.

**Note:** This integration supports all plans of Asana at organization level only.

**Important:** Minimize security risks and protect information by granting access only to the necessary user or API permissions.

|Process|Required user role in the Asana application|Authentication scopes|
|-------|-------------------------------------------|---------------------|
|Download subscriptions|admin|default|
|Pull user activity|admin|default|
|Reclaim subscription|admin|default|

## Register an Asana OAuth 2.0 application

Register an Asana OAuth application to access the Asana API 1.0 and to receive a Client ID and Client secret.

### Before you begin

Asana Role required: admin

### Procedure

1.  Log in to your Asana account.

2.  Select the user's profile icon.

3.  Select **Settings**.

4.  Select the **Apps** tab.

5.  Navigate to the developer console window by selecting the **View developer console** link.

6.  Select **+ Create new app**.

7.  On the **Create new app** page, provide a name for your application and then select the **Integrate Asana and another tool** check box.

8.  Select the **I agree to the Asana API Terms** check box and then select **Create app**.

9.  Provide basic information about your application.

10. Select **OAuth**.

11. Copy the Client ID and Client secret for later use.

12. In the **Redirect URLs** field, select **+ Add redirect URL**.

13. Enter `https://<instance>.service-now.com/oauth_redirect.do` where &lt;instance&gt; is the name of your ServiceNow instance.


## Create an Asana integration profile

Create an Asana integration profile to track software subscriptions and optimize licensing for your Asana solutions.

### Before you begin

The Software Asset Management - SaaS License Management Integrations plugin \(sn\_sam\_saas\_int\) must be installed from the [ServiceNow Store](https://store.servicenow.com/).

Role required: sam\_integrator

**Important:** You must select the **Asana Spoke** check box for this integration while installing optional features on the [Application Manager](https://www.servicenow.com/docs/access?context=application-manager&version=australia&pubname=australia-platform-administration&ft:locale=en-US) page. For more information about choosing the required SaaS applications, see [Request SaaS License Management](../task/request-saas-license-management.md).

### Procedure

1.  Navigate to the integration profile.

<table id="choicetable_o3p_z3k_qtb"><thead><tr><th align="left" id="d152516e397">

Interface

</th><th align="left" id="d152516e400">

Action

</th></tr></thead><tbody><tr><td id="d152516e406">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.
2.  Select **New**.
3.  Select **Asana Integration Profile**.


</td></tr><tr><td id="d152516e448">

**Software Asset Workspace**

</td><td>

1.  Navigate to **License operations** &gt; **User Subscriptions** &gt; **Direct integration profiles**.
2.  Select **New**.
3.  Select **Asana** from the drop-down list.
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

Name of the integration profile. For example, Asana integration.

</td></tr><tr><td>

Status

</td><td>

Status of the integration profile. -   If you have not published the integration profile, this field is automatically set to  **Draft**.
-   If you have already published the integration profile, this field is automatically set to  **Published**.


</td></tr><tr><td>

Profile type

</td><td>

Type of integration profile. This field is automatically set to Asana Subscription.

</td></tr></tbody>
</table>3.  Review the required user roles or API permissions specified in the **Vendor configuration** field for each process to minimize security risks and optimize SaaS licenses.

    **Note:** For more information, see [Minimal user permissions](integrate-with-asana.md#) table.

    1.  In the Download Subscription Subflow section, verify that the **Subflow** field is set to **Asana Download Subscriptions**.

        **Note:** The **Download subscriptions** check box is selected by default and you can't clear it.

    2.  In the Calculate Activity Subflow section, verify that the **Subflow** field is set to **Asana Update User Activity**.

        **Note:** The **Download Activity** check box is selected by default. If you clear it, the activity scheduled job **SAM - Refresh &lt;displayname&gt; Activity** isn't created.

        In the **Analyze user activity** field, you can also select the date and time starting from when you want to analyze the user activity. By default, you can analyze user activity up to 60 days prior to the current date and view events performed by individual users from the time you create this profile.

        **Note:** Software Asset Management pulls the events from the time that you start analyzing user activity irrespective of the profile creation date.

        You can modify this value in the Last activity threshold field of your software reclamation rules. For more information, see [Review a software reclamation rule](../task/add-reclamation-rule-sub.md).

    3.  In the Reclaim Subscription Subflow section, verify that the **Subflow** field is set to **Asana Reclaim Subscription**.

        **Note:** The **Reclaim subscriptions** check box is selected by default. If you don't want to reclaim subscriptions, you can clear this check box. If you clear it, the removal candidates are created but the reclaim subscription subflow isn't triggered or the reclamation process isn't initiated.

4.  Select **Save**.

    A draft integration profile is created.

    The **Connection &amp; Credential** field appears and is automatically set to **sn\_asana\_spoke.Asana**.

5.  Open the connection &amp; credential aliases record by selecting the preview icon ![](../image/preview-icon.png) beside the **Connection &amp; Credential** field.

6.  Select **Open Record** in the record preview.

7.  Select the **Create New Connection &amp; Credential** related link.

8.  In the Create Connection and Credential dialog box, fill in the fields.

    |Field|Value|
    |-----|-----|
    |Connection Name|Name of the Asana connection. This field populates automatically.|
    |Connection URL|URL for the connection. This field is automatically set to `https://app.asana.com`.|
    |Client ID|Client ID that you created while registering Asana OAuth application.|
    |Client Secret|Client secret that you created while registering Asana OAuth application.|
    |OAuth Redirect URL|This field is automatically populated to`https://<instance name>.service-now.com/oauth_redirect.do`, where instance name is the name of your ServiceNow instance.|

9.  Select **Create and Get OAuth Token**.

10. On the integration profile form, select **Validate Connection** to verify the connection and credential details of this integration.

    Validating the connection verifies the Download Subscriptions and Calculate Activity APIs, but not the Reclaim Subscriptions APIs.

11. After the connection is verified, select **Publish**.

12. In the Publish Confirmation dialog box, select **OK**.

    **Note:** If you clear the **Download Activity** check box after the integration profile is published, you must revalidate the connections and then republish the integration profile because the following events occur:

    -   The **Status** field on the integration profile form changes to **Draft**.
    -   The **Validate connection** button shows up on the form.
    -   The current **SAM - Refresh &lt;displayname&gt; Activity** job gets deleted.

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

