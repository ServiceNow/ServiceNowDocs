---
title: Integrating with Calendly
description: Integrating your Software Asset Management application with the Calendly service enables you to track your software subscriptions and to reclaim unused licenses.Register a public application with the Calendly service so that you can access the Calendly API using OAuth 2.0.Create an integration profile to track software subscriptions and optimize stale licenses for the Calendly service.
locale: en-US
release: australia
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Integrate with SaaS applications, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Integrating with Calendly

Integrating your Software Asset Management application with the Calendly service enables you to track your software subscriptions and to reclaim unused licenses.

**Important:** Minimize security risks and protect information by granting access only to the necessary user or API permissions.

|Process|Required user role in the Calendly application|Authentication scopes|
|-------|----------------------------------------------|---------------------|
|Download subscriptions|admin|None|
|Pull user activity|admin|None|
|Reclaim subscription|admin|None|

## Create a Calendly OAuth application

Register a public application with the Calendly service so that you can access the Calendly API using OAuth 2.0.

### Before you begin

Calendly Role required: admin

You must have a Google or GitHub account to sign up for a Calendly developer.

### Procedure

1.  Navigate to [Calendly developer portal](https://developer.calendly.com/).

    -   If you already have a Calendly developer account, sign in with your credentials and go to step 3.
    -   If you don't have a Calendly developer account account, complete step 2.
2.  Sign up for a Calendly developer account through your GitHub or Google account by selecting **Sign Up** on the top-right corner of the Calendly Developer Site page.

    This account isn't associated with your Calendly Google user account.

3.  Navigate to **Account** &gt; **My Apps** to create a OAuth application.

4.  Select **Create a new app**.

5.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name of app|Name of your application.|
    |Kind of app|The application type such as Web or Native.|
    |Environment type|The environment type that you want to associate your application to, such as Sandbox or Production.|
    |Redirect URI|ServiceNow redirect URL. For example, `https://app.example.com/auth`.|

6.  Select **Save &amp; Continue**.


### What to do next

Copy your Client ID and Client Secret.

**Important:**

You must copy these values as you can't access the Client Secret again.

## Create a Calendly integration profile

Create an integration profile to track software subscriptions and optimize stale licenses for the Calendly service.

### Before you begin

To create a Calendly integration profile, request the Software Asset Management - SaaS License Management \(sn\_sam\_saas\_int\) from the [ServiceNow Store](https://store.servicenow.com/).

ServiceNow Role required: sam\_integrator

**Important:** You must select the **Calendly Spoke** check box for this integration while installing optional features on the [Application Manager](https://www.servicenow.com/docs/access?context=application-manager&version=australia&pubname=australia-platform-administration&ft:locale=en-US) page. For more information about choosing the required SaaS applications, see [Request SaaS License Management](../task/request-saas-license-management.md).

### About this task

If you’re using Software Asset Workspace, the option to create the Calendly integration profile in Core UI is inactive.

### Procedure

1.  Navigate to the integration profile.

<table id="choicetable_o3p_z3k_qtb"><thead><tr><th align="left" id="d89110e472">

Interface

</th><th align="left" id="d89110e475">

Action

</th></tr></thead><tbody><tr><td id="d89110e481">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.
2.  Select **New**.
3.  Select **Calendly Integration Profile**.


</td></tr><tr><td id="d89110e523">

**Software Asset Workspace**

</td><td>

1.  Navigate to **License operations** &gt; **User Subscriptions** &gt; **Direct integration profiles**.
2.  Select **New**.
3.  Select **Calendly** from the drop-down list.
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

Name of the integration profile. For example, `Calendly Integration`.

</td></tr><tr><td>

Status

</td><td>

Status of the integration profile.-   If you have not published the integration profile, this field is automatically set to **Draft**.
-   If you have already published the integration profile, this field is automatically set to **Published**.


</td></tr><tr><td>

Profile Type

</td><td>

Type of integration profile.This field is automatically set to **Calendly Subscription**.

</td></tr></tbody>
</table>3.  Review the required user roles or API permissions specified in the **Vendor configuration** field for each process to minimize security risks and optimize SaaS licenses.

    **Note:** For more information, see [Minimal user permissions](integrate-with-calendly.md#) table.

    1.  In the Download Subscription Subflow section, verify that the **Subflow** field is set to **Calendly Download Subscriptions**.

        **Note:** The **Download subscriptions** check box is selected by default and you can't clear it.

    2.  In the Calculate Activity Subflow section, verify that the **Subflow** field is set to **Calendly Update User Activity**.

        **Note:** The **Download Activity** check box is selected by default. If you clear it, the activity scheduled job **SAM - Refresh &lt;displayname&gt; Activity** isn't created.

        In the **Analyze user activity** field, you can also select the date and time starting from when you want to analyze the user activity. By default, you can analyze user activity up to 60 days prior to the current date and view events performed by individual users from the time you create this profile.

        **Note:** Software Asset Management pulls the events from the time that you start analyzing user activity irrespective of the profile creation date.

        You can modify this value in the Last activity threshold field of your software reclamation rules. For more information, see [Review a software reclamation rule](../task/add-reclamation-rule-sub.md).

    3.  In the Reclaim Subscription Subflow section, verify that the **Subflow** field is set to **Calendly Reclaim Subscription**.

        **Note:** The **Reclaim subscriptions** check box is selected by default. If you don't want to reclaim subscriptions, you can clear this check box. If you clear it, the removal candidates are created but the reclaim subscription subflow isn't triggered or the reclamation process isn't initiated.

4.  Select **Save**.

    Your ServiceNow instance creates a draft integration profile.

    The **Connection &amp; Credential** field appears and is automatically set to **sn\_calendly\_spoke.Calendly**.

5.  Open the connection &amp; credential aliases record by selecting the preview icon ![](../image/preview-icon.png) next to the **Connection &amp; Credential** field and then selecting **Open Record** in the record preview.

6.  On the Connection &amp; Credential Aliases form, select the **Create New Connection &amp; Credential** related link.

7.  In the dialog box, fill in the fields.

<table id="table_ujr_ps1_wmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Name of the connection.

</td></tr><tr><td>

Connection URL

</td><td>

Base URL for the Calendly API. This field is automatically set to `https://api.calendly.com`.

</td></tr><tr><td>

OAuth Client ID

</td><td>

Client ID that is assigned to the public application that you registered with the Calendly service.

</td></tr><tr><td>

OAuth Client Secret

</td><td>

Client secret that is assigned to the public application that you registered with the Calendly service.

</td></tr><tr><td>

OAuth Redirect URL

</td><td>

URL of the OAuth provider that users are redirected to after authentication. This field populates automatically based on your instance name.

</td></tr></tbody>
</table>8.  Select **Create and Get OAuth Token**.

    **Note:** For the role required to perform this step, refer to the [Minimal user permissions](integrate-with-calendly.md#) table.

9.  In the Authorize App dialog box, log in to your Calendly account.

    The dialog box closes and then you automatically return to the integration profile form.

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

