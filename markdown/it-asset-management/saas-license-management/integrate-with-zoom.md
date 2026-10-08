---
title: Integrating with Zoom Workplace
description: Integrating your Software Asset Management application with the Zoom Workplace application enables you to track your software subscriptions and to reclaim unused licenses.Create an application in the Zoom App Marketplace.Create an integration profile to track software subscriptions and optimize licensing for the Zoom Workplace service.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-asset-management/saas-license-management/integrate-with-zoom.html
release: zurich
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 9
breadcrumb: [Integrate with SaaS applications, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Integrating with Zoom Workplace

Integrating your Software Asset Management application with the Zoom Workplace application enables you to track your software subscriptions and to reclaim unused licenses.

A suite is a bundle of Zoom Workplace products and add-ons licensed together under a single subscription, rather than assigned to users individually. When a user is licensed through a suite, the Software Asset Management application tracks the suite subscription as a whole. When products or add-ons are assigned individually rather than through a suite, the Software Asset Management application tracks each one separately.

With this integration, you can retrieve and analyze licensing information for Zoom Workplace applications. These applications include the Zoom account \(not a Master or Master-sub account\) for Meetings and Webinar, along with the Workplace products and add-ons mentioned in the following table. Reclamation applies to all the following Zoom Workplace products and add-ons.

|Application|Type|
|-----------|----|
|Meetings|Product|
|Webinar|Product|
|Team Chat|Product|
|Mail &amp; Calendar|Product|
|Phone|Product|
|Scheduler|Product|
|Docs|Product|
|Visitor Management|Product|
|Whiteboard Plus|Add-on|
|Clips Plus|Add-on|
|Webinars Plus|Add-on|
|Translated Captions|Add-on|
|Large Meeting|Add-on|
|Customer Managed Key|Add-on|

**Note:** The enhanced Zoom Workplace offering is available starting from the Software Asset Management - SaaS License Management application version 16.10.0.

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

-   meeting:read:list\_meetings:admin
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
</table>## Create a Zoom Workplace application

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
    -   meeting:read:list\_meetings:admin
    -   webinar:read:list\_webinars:admin
    -   user:update:settings:admin
    -   user:update:user:admin
    -   user:delete:user:admin

## Create a Zoom Workplace integration profile

Create an integration profile to track software subscriptions and optimize licensing for the Zoom Workplace service.

### Before you begin

To create a Zoom Workplace integration profile, request and install the Software Asset Management - SaaS License Management plugin \(sn\_sam\_saas\_int\) from the [ServiceNow Store](https://store.servicenow.com/).

ServiceNow Role required: sam\_integrator or admin

### About this task

If you’re using Software Asset Workspace, the option to create the Zoom Workplace integration profile in Core UI is inactive.

### Procedure

1.  Navigate to the integration profile.

<table id="choicetable_o3p_z3k_qtb"><thead><tr><th align="left" id="d70781e614">

Interface

</th><th align="left" id="d70781e617">

Action

</th></tr></thead><tbody><tr><td id="d70781e623">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.
2.  Select **New**.
3.  Select **Zoom Integration Profile**.


</td></tr><tr><td id="d70781e666">

**Software Asset Workspace**

</td><td>

1.  Navigate to **License operations** &gt; **User Subscriptions** &gt; **Direct integration profiles**.
2.  Select **New**.
3.  Select **Zoom Workplace** from the drop-down list.
4.  Select **Continue**.


</td></tr></tbody>
</table>2.  On the form, fill in the fields.

<table id="table_gnm_whv_5fb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr id="row_ksq_rt5_bgb"><td id="display-name">

Display name

</td><td id="display-name-def">

Name of the integration profile. For example, `Zoom Workplace Integration`.

</td></tr><tr><td>

Status

</td><td>

Status of the integration profile. -   If you have not published the integration profile, this field is set to  **Draft**.
-   If you have already published the integration profile, this field is set to  **Published**.


</td></tr><tr id="row_nn5_st5_bgb"><td id="profile-type">

Profile type

</td><td id="profile-type-def">

Type of integration profile. This value is automatically set to `Zoom Workplace Subscription`.**Note:**

-   If you have an existing Zoom integration profile, the `Zoom Subscription` profile type will continue to work for the profile. For a new Zoom integration profile, select the `Zoom Workplace Subscription` profile type instead.
-   You existing `Zoom Subscription` profiles don't recognize the new Workplace products and add-ons. Create a `Zoom Workplace Subscription` profile to track these products and add-ons.


</td></tr></tbody>
</table>3.  In the Process configuration section, review the required user roles or API permissions in the **Vendor configuration** field for each process to minimize security risks and optimize SaaS licenses.

    **Note:** For more information about the required roles and scopes, see the [Minimal user permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/saas-license-management/integrate-with-zoom.md) table.

    -   The **Download subscriptions** check box is selected by default and you can't clear it.

    -   The **Download Activity** check box is selected by default. If you clear it, the activity scheduled job **SAM - Refresh &lt;displayname&gt; Events** isn't created.

        In the **Analyze user activity** field, you can also select the date and time starting from when you want to analyze the user activity. By default, you can analyze user activity up to 60 days prior to the current date and view events performed by individual users from the time you create this profile.

        **Note:** Software Asset Management pulls the events from the time that you start analyzing user activity irrespective of the profile creation date.

        You can modify this value in the Last activity threshold field of your software reclamation rules. For more information, see [Review a software reclamation rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/saas-license-management/add-reclamation-rule-sub.md).

    -   The **Reclaim subscriptions** check box is selected by default. If you don't want to reclaim subscriptions, you can clear this check box. If you clear it, the removal candidates are created but the reclaim subscription subflow isn't triggered or the reclamation process isn't initiated.

4.  Select **Submit**.

    Your ServiceNow instance creates a draft integration profile.

    The **Connection &amp; Credential** field appears and is automatically set to **sn\_zoom\_spoke.Zoom**.

5.  Open the connection &amp; credential aliases record by selecting the preview icon \[Omitted image "preview-icon.png"\] next to the **Connection &amp; Credential** field and then selecting **Open Record** in the record preview.

6.  On the Connection &amp; Credential Aliases form, select the **Create New Connection &amp; Credential** related link.

7.  In the Create Connection and Credential dialog box, fill in or verify the following fields.

    |Field|Description|
    |-----|-----------|
    |Connection Information|
    |Connection Name|Name of the Zoom Workplace connection. This field populates automatically.|
    |Connection URL|URL for the connection. This field is automatically set to `https://zoom.us`.|
    |Credential Information|
    |OAuth Client ID|Client ID for the OAuth 2.0 application created in [step 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/saas-license-management/integrate-with-zoom.md).|
    |OAuth Client Secret|Password associated with the client ID created in [step 5](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/saas-license-management/integrate-with-zoom.md).|
    |OAuth Redirect URL|`https://<instance_name>/oauth_redirect.do`, where instance name is the name of your ServiceNow instance.|

8.  Select **Configure and Get OAuth Token**.

    **Note:** For the role required to perform this step, see the [Minimal user permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/saas-license-management/integrate-with-zoom.md) table.

9.  On the integration profile form, select **Validate Connection** to verify the connection and credential details of this integration.

    Validating the connection verifies the Download Subscriptions and Calculate Activity APIs, but not the Reclaim Subscriptions APIs.

    **Note:** If you clear the **Download Activity** check box after the integration profile is validated and scheduled jobs are created, you must revalidate the connections because the following events occur:

    -   The **Status** field on the integration profile form changes to **Draft**.
    -   The **Validate connection** button shows up on the form.
    -   The current **SAM - Refresh &lt;displayname&gt; Events** job gets deleted.
10. After the connection is verified, select **Publish**.

11. In the Publish Confirmation dialog box, select **OK**.


### Result

You can view events performed by individual users up to one year prior to the current date. For more information, see [Review a software reclamation rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/saas-license-management/add-reclamation-rule-sub.md). Software Asset Management pulls the events from the time that you start downloading user subscriptions irrespective of the profile creation date.

### What to do next

After the integration connects, your ServiceNow instance automatically creates software models, reclamation rules, and software subscriptions that are refreshed daily.

After creating an integration profile, view information about the profile in the Software Asset Workspace by navigating to **License operations** &gt; **User subscription** &gt; **Direct integration profiles**. You can select an integration profile to view the following related lists. If the following related lists aren't visible for an integration profile in the default view, you can select the custom integration view from the Details tab:

-   Software Models
-   Unrecognized Subscription Identifiers
-   Scheduled Jobs
-   Scheduled Job Results
-   Software Subscriptions
-   Subscription Identifier Exclusion Rule
-   Subscription User Exclusion Rule

After creating an integration profile, you can define subscription exclusion rules to keep certain subscriptions from license cost calculations. For more information, see [Subscription exclusions for SaaS and SSO applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/saas-license-management/subscription-exclusions.md).

If you want to set up multiple integration profiles with unique connections, create child aliases to manage different configurations and settings for each integration profile. For more information, see [Create a child alias to set up multiple integration profiles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/saas-license-management/create-child-alias-saas.md).

Review all automatically generated reclamation rules to reclaim user subscriptions. For more information, see [Review a software reclamation rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/saas-license-management/add-reclamation-rule-sub.md).

Create software entitlements for the automatically generated software models to track used software against owned software.

-   For more information on creating software entitlements in the Software Asset Management Core UI, see [Create entitlements in Software Asset Management classic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/software-asset-management/track-software-rights.md).
-   For more information on creating software entitlements in the Software Asset Workspace, see [Create entitlements in workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/software-asset-management/create-entitlements-workspace.md).
-   For more information on creating software entitlements using the Software Asset Management Playbook, see [Create entitlements using the guided walk-through](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/software-asset-management/guidedwalk-workspace.md).

Reconciliation also runs on your subscriptions as a scheduled job or on-demand. You can view your reconciliation results in the [License Workbench](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/software-asset-management/sam-license-workbench.md) \(Software Asset Management classic application\) or the [License usage view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/software-asset-management/sam-workspace-workbench.md) \(Software Asset Workspace\). Use these results to determine your license compliance position and to remediate any non-compliance.

-   For more information on running reconciliation in the Software Asset Management classic application, see [Run software reconciliation in Software Asset Management classic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/software-asset-management/t_RunReconciliation.md).
-   For more information on running reconciliation in the Software Asset Workspace, see [Run software reconciliation in the workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/software-asset-management/run-recon-workspace.md).

