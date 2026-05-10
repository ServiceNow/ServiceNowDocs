---
title: Integrating with Smartsheet
description: Integrating your Software Asset Management application with the Smartsheet application enables you to track your software subscriptions and to reclaim unused licenses.Create an API access token for authenticating Smartsheet API requests.Create a Smartsheet integration profile to track software subscriptions and optimize licensing for your Smartsheet applications.
locale: en-US
release: australia
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
keywords: [smartsheet, integration profile, saas]
breadcrumb: [Integrate with SaaS applications, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Integrating with Smartsheet

Integrating your Software Asset Management application with the Smartsheet application enables you to track your software subscriptions and to reclaim unused licenses.

**Important:** Minimize security risks and protect information by granting access only to the necessary user or API permissions.

|Process|Required user role in the Smartsheet application|Authentication scopes|
|-------|------------------------------------------------|---------------------|
|Download subscriptions|admin|None|
|Pull user activity|admin|None|
|Reclaim subscription|admin|None|

## Create a Smartsheet API access token

Create an API access token for authenticating Smartsheet API requests.

### Before you begin

Smartsheet Role required: admin

### Procedure

1.  From a web browser, open [Smartsheet](https://app.smartsheet.com/b/home).

2.  Log in using your Smartsheet credentials.

3.  On the side navigation bar, select the account icon \(![Account icon.](../image/account-menu-icon.png)\) and then select **Apps &amp; Integrations**.

4.  In the Personal Settings dialog box, select **API Access**.

5.  Under Manage API Access Tokens, select **Generate new access token**.

6.  When prompted, enter a name for your API access token in the **API Access Token Name** field and then select **OK**.

    Smartsheet automatically generates and displays your API access token. For security purposes, this API access token appears only once.

7.  Copy your API access token and save it in a secure location for later use.

8.  Select **OK**.


## Create a Smartsheet integration profile

Create a Smartsheet integration profile to track software subscriptions and optimize licensing for your Smartsheet applications.

### Before you begin

To create a Smartsheet integration profile, request the Software Asset Management - SaaS License Management plugin \(sn\_sam\_saas\_int\) from the [ServiceNow Store](https://store.servicenow.com/).

ServiceNow Role required: sam\_integrator

**Important:** You must select the **Smartsheet Spoke** check box for this integration while installing optional features on the [Application Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/application-manager/application-manager.md) page. For more information about choosing the required SaaS applications, see [Request SaaS License Management](../task/request-saas-license-management.md).

### About this task

If you’re using Software Asset Workspace, the option to create the Smartsheet integration profile in Core UI is inactive.

### Procedure

1.  Navigate to the integration profile.

<table id="choicetable_o3p_z3k_qtb"><thead><tr><th align="left" id="d234908e384">

Interface

</th><th align="left" id="d234908e387">

Action

</th></tr></thead><tbody><tr><td id="d234908e393">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.
2.  Select **New**.
3.  Select **Smartsheet Integration Profile**.


</td></tr><tr><td id="d234908e435">

**Software Asset Workspace**

</td><td>

1.  Navigate to **License operations** &gt; **User Subscriptions** &gt; **Direct integration profiles**.
2.  Select **New**.
3.  Select **Smartsheet** from the drop-down list.
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

Name of the integration profile. For example, `Smartsheet Integration`.

</td></tr><tr><td>

Status

</td><td>

Status of the integration profile.-   If you have not published the integration profile, this field is automatically set to **Draft**.
-   If you have already published the integration profile, this field is automatically set to **Published**.


</td></tr><tr><td>

Profile Type

</td><td>

Type of integration profile. This field is automatically set to **Smartsheet Subscription**.

</td></tr></tbody>
</table>3.  View the required user roles or API permissions to minimize security risks and optimize SaaS licenses.

    **Note:** For more information, see [Minimal user permissions](integrate-with-smartsheet.md#) table.

    1.  In the Download Subscription Subflow section, verify that the **Subflow** field is set to **Smartsheet Download Subscriptions**.

        **Note:** The **Download subscriptions** check box is selected by default and you can't clear it.

    2.  In the Calculate Activity Subflow section, verify that the **Subflow** field is set to **Smartsheet Update User Activity**.

        The **Download Activity** check box is selected by default. If you clear it, the activity scheduled job **SAM - Refresh &lt;displayname&gt; Events** isn't created.

        **Important:** To enable detailed event tracking, procure an Event Reporting add-on from Smartsheet.

        In the **Analyze user activity** field, you can also select the date and time starting from when you want to analyze the user activity. By default, you can analyze user activity up to 60 days prior to the current date and view events performed by individual users from the time you create this profile.

        **Note:** Software Asset Management pulls the events from the time that you start analyzing user activity irrespective of the profile creation date.

        You can modify this value in the Last activity threshold field of your software reclamation rules. For more information, see [Review a software reclamation rule](../task/add-reclamation-rule-sub.md).

    3.  In the Reclaim Subscription Subflow section, verify that the **Subflow** field is set to **Smartsheet Reclaim Subscription**.

        **Note:** The **Reclaim subscriptions** check box is selected by default. If you don't want to reclaim subscriptions, you can clear this check box. If you clear it, the removal candidates are created but the reclaim subscription subflow isn't triggered or the reclamation process isn't initiated.

4.  Select **Save** after completing all the required fields.

    Your ServiceNow instance creates a draft integration profile. The integration profile uses the Smartsheet Download Subscriptions, Smartsheet Update User Activity, and Smartsheet Reclaim Subscription subflows to retrieve user data from the Smartsheet application.

    The **Connection &amp; Credential** field appears and is automatically set to **sn\_smrtsheet\_spoke.Smartsheet**.

5.  Open the connection &amp; credential aliases record by selecting the preview icon ![](../image/preview-icon.png) next to the **Connection &amp; Credential** field and then selecting **Open Record** in the record preview.

6.  On the Connection &amp; Credential Aliases form, select the **Create New Connection &amp; Credential** related link.

7.  In the dialog box, fill in the fields.

<table id="table_ujr_ps1_wmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the connection.

</td></tr><tr><td>

Connection URL

</td><td>

This field is automatically set to `https://api.smartsheet.com`. **Note:** Based on regions, replace the Connection URL with these respective URLs:

-   Smartsheet Gov: `https://api.smartsheetgov.com/`
-   Smartsheet Regions Europe: `https://api.smartsheet.eu/`
-   Smartsheet Regions Australia: `https://api.smartsheet.au/`


</td></tr><tr><td>

API Key

</td><td>

API key for your Smartsheet application. Enter an API key in the `api-access-token` format, where &lt;*api-access-token*&gt; is the API access token that you created in Smartsheet.

</td></tr></tbody>
</table>8.  Select **Create**.

    You automatically return to the integration profile.

9.  On the integration profile form, select **Validate Connection** to verify the connection and credential details of this integration.

10. After the connection is verified, select **Publish**.

11. In the Publish Confirmation dialog box, select **OK**.

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

