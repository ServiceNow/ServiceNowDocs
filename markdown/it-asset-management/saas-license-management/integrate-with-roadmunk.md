---
title: Integrating with Roadmunk
description: Integrating your Software Asset Management application with the Roadmunk application enables you to track your software subscriptions and to reclaim unused licenses.Generate an API access token that authorizes access to the Roadmunk GraphQL API.Create a Roadmunk integration profile to track software subscriptions and optimize licensing for your Roadmunk applications.
locale: en-US
release: australia
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 9
breadcrumb: [Integrate with SaaS applications, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Integrating with Roadmunk

Integrating your Software Asset Management application with the Roadmunk application enables you to track your software subscriptions and to reclaim unused licenses.

**Important:** Minimize security risks and protect information by granting access only to the necessary user or API permissions.

|Process|Required user role in the Roadmunk application|Authentication scopes|
|-------|----------------------------------------------|---------------------|
|Download subscriptions|Account Admin|No scopes|
|Pull user activity|Account Admin|No scopes|
|Reclaim subscription|Account Admin|No scopes|

## Generate a Roadmunk API access token

Generate an API access token that authorizes access to the Roadmunk GraphQL API.

### Before you begin

Roadmunk Role required: Account Admin

### Procedure

1.  From a web browser, open [Roadmunk](https://roadmunk.com/).

2.  Log in using your account admin credentials.

3.  On the left navigation menu of the Roadmunk dashboard, select your profile icon and then select **Account Settings**.

4.  On the page header of your account settings, select the **Integrations** tab.

5.  Under Existing Integrations, select **Add an integration**.

6.  When prompted to select an integration to configure, select **API Tokens**.

7.  On the Roadmunk API Tokens form, enter a name for your API access token in the **Application Name** field.

8.  Select **Create API Token**.

    The API access token is generated and then the API Token Created dialog box opens.

9.  On the API Token Created dialog box, copy your API access token by selecting **Copy To Clipboard**.

    Save it in a secure location for later use.


## Create a Roadmunk integration profile

Create a Roadmunk integration profile to track software subscriptions and optimize licensing for your Roadmunk applications.

### Before you begin

To create a Roadmunk integration profile, request the Software Asset Management - SaaS License Management plugin \(sn\_sam\_saas\_int\) from the [ServiceNow Store](https://store.servicenow.com/).

ServiceNow Role required: sam\_integrator

**Important:** You must select the **Roadmunk Spoke** check box for this integration while installing optional features on the [Application Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/application-manager/application-manager.md) page. For more information about choosing the required SaaS applications, see [Request SaaS License Management](../task/request-saas-license-management.md).

### About this task

If you’re using Software Asset Workspace, the option to create the Roadmunk integration profile in Core UI is inactive.

### Procedure

1.  Navigate to the integration profile.

<table id="choicetable_o3p_z3k_qtb"><thead><tr><th align="left" id="d314661e378">

Interface

</th><th align="left" id="d314661e381">

Action

</th></tr></thead><tbody><tr><td id="d314661e387">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.
2.  Select **New**.
3.  Select **Roadmunk Integration Profile**.


</td></tr><tr><td id="d314661e429">

**Software Asset Workspace**

</td><td>

1.  Navigate to **License operations** &gt; **User Subscriptions** &gt; **Direct integration profiles**.
2.  Select **New**.
3.  Select **Roadmunk** from the drop-down list.
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

Name of the integration profile. For example, `Roadmunk Integration`.

</td></tr><tr><td>

Status

</td><td>

Status of the integration profile.-   If you have not published the integration profile, this field is automatically set to **Draft**.
-   If you have already published the integration profile, this field is automatically set to **Published**.


</td></tr><tr><td>

Profile Type

</td><td>

Type of integration profile. This field is automatically set to **Roadmunk Subscription**.

</td></tr></tbody>
</table>3.  Review the required user roles or API permissions specified in the **Vendor configuration** field for each process to minimize security risks and optimize SaaS licenses.

    **Note:** For more information, see [Minimal user permissions](integrate-with-roadmunk.md#) table.

    1.  In the Download Subscription Subflow section, verify that the **Subflow** field is set to **Roadmunk Download Subscriptions**.

        **Note:** The **Download subscriptions** check box is selected by default and you can't clear it.

    2.  In the Calculate Activity Subflow section, verify that the **Subflow** field is set to **Roadmunk Update User Activity**.

        **Note:** The **Download Activity** check box is selected by default. If you clear it, the activity scheduled job **SAM - Refresh &lt;displayname&gt; Activity** isn't created.

        In the **Analyze user activity** field, you can also select the date and time starting from when you want to analyze the user activity. By default, you can analyze user activity up to 60 days prior to the current date and view events performed by individual users from the time you create this profile.

        **Note:** Software Asset Management pulls the events from the time that you start analyzing user activity irrespective of the profile creation date.

        You can modify this value in the Last activity threshold field of your software reclamation rules. For more information, see [Review a software reclamation rule](../task/add-reclamation-rule-sub.md).

    3.  In the Reclaim Subscription Subflow section, verify that the **Subflow** field is set to **Roadmunk Reclaim Subscription**.

        **Note:** The **Reclaim subscriptions** check box is selected by default. If you don't want to reclaim subscriptions, you can clear this check box. If you clear it, the removal candidates are created but the reclaim subscription subflow isn't triggered or the reclamation process isn't initiated.

4.  Select **Save**.

    Your ServiceNow instance creates a draft integration profile.

    The **Connection &amp; Credential** field appears and is automatically set to **sn\_roadmunk\_spoke.Roadmunk**.

5.  To avoid your integration profile from including inactive users in your list of Roadmunk subscriptions, enable the Roadmunk Download Subscriptions subflow to download only the active users in your Roadmunk account.

    By default, the Roadmunk Download Subscriptions subflow downloads all users in your Roadmunk account, including both active and inactive users.

    1.  In a new tab or window, open [Roadmunk](https://roadmunk.com/).

    2.  Log in using your Account Admin credentials.

        The Roadmunk dashboard opens.

    3.  On the left navigation menu of the Roadmunk dashboard, select your profile icon and then select **Account Settings**.

        Your account settings open.

    4.  On the page header of your account settings, select the **Reports** tab.

    5.  From the list of available Roadmunk reports, select **Download User CSV**.

        The Roadmunk User Report downloads in `.csv` format.

    6.  Return to the Integration Profile form.

    7.  On the form header, select the **Manage Attachments** icon ![Manage attachments icon.](../image/manage-attachments-icon.png).

    8.  In the Attachments dialog box, select **Choose file** to locate and select the Roadmunk User Report that you downloaded in [step e](integrate-with-roadmunk.md#download-user-report).

    9.  After the report uploads successfully, close the dialog box to return to the Integration Profile form.

    **Tip:** For continuously removing inactive users from your list of Roadmunk subscriptions, download and attach the latest version of the Roadmunk User Report periodically.

6.  Open the connection &amp; credential aliases record by selecting the preview icon ![](../image/preview-icon.png) next to the **Connection &amp; Credential** field and then selecting **Open Record** in the record preview.

7.  On the Connection &amp; Credential Aliases form, select the **Create New Connection &amp; Credential** related link.

8.  In the Create Connection and Credential dialog box, fill in the fields.

<table id="table_xd2_qht_lnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Connection Information

</td></tr><tr><td>

Connection Name

</td><td>

Name of the Roadmunk connection. This field populates automatically.

</td></tr><tr><td>

Connection URL

</td><td>

URL for the connection. This field is automatically set to **https://app-gateway.roadmunk.com**, where **app** is the default geographic region \(North America\) in which the connection is being created. If you’re creating the connection outside of the default **app** \(North America\) region, you can change the value of the region to either **eu** \(Europe\) or **apac** \(Asia-Pacific Region\).

</td></tr><tr><td colspan="2">

Credential Information

</td></tr><tr><td>

API Token

</td><td>

API access token that authorizes access to the Roadmunk GraphQL API. Enter the same API access token that you generated in [Generate a Roadmunk API access token](integrate-with-roadmunk.md#).

</td></tr></tbody>
</table>9.  Select **Create**.

10. On the integration profile form, select **Validate Connection** to verify the connection and credential details of this integration.

    Validating the connection verifies the Download Subscriptions and Calculate Activity APIs, but not the Reclaim Subscriptions APIs.

11. After the connection is verified, select **Publish**.

12. Select **Publish**.

13. In the Publish Confirmation dialog box, select **OK**.

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

