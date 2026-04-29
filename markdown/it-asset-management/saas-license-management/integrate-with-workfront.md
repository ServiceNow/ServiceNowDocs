---
title: Integrating with Adobe Workfront
description: Integrating your Software Asset Management application with the Adobe Workfront application enables you to track your software subscriptions and to reclaim unused licenses.Generate an API key for authenticating Workfront API requests.Create a Workfront integration profile to track software subscriptions and optimize licensing for your Workfront applications.
locale: en-US
release: australia
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 8
breadcrumb: [Integrate with SaaS applications, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Integrating with Adobe Workfront

Integrating your Software Asset Management application with the Adobe Workfront application enables you to track your software subscriptions and to reclaim unused licenses.

**Important:** Minimize security risks and protect information by granting access only to the necessary user or API permissions.

|Process|Required user role in the Adobe Workfront application|Authentication scopes|
|-------|-----------------------------------------------------|---------------------|
|Download subscriptions|administrator|None|
|Pull user activity|administrator|None|
|Reclaim subscription|administrator|None|

## Generate a Workfront API key

Generate an API key for authenticating Workfront API requests.

### Before you begin

Workfront Role required: administrator

### Procedure

1.  From a web browser, open [Adobe Workfront](https://www.workfront.com).

2.  Log in using your admin credentials.

    Your Adobe Workfront instance opens.

3.  On the page header of your Adobe Workfront instance, select the Main Menu icon ![Main Menu icon.](../image/main-menu-icon.png) and then select **Setup**.

4.  From the left navigation menu of the Setup page, navigate to **System** &gt; **Customer Info**.

    The Customer Info page opens.

5.  In the API Key Settings section, select **Generate API Key**.

    Adobe Workfront automatically generates your API key and displays it under Your User's API Key.

6.  Copy your API key and save it in a secure location for later use.

7.  In the same section, select the time period after which you want the API key to expire from the **After creation, API keys expire** list.

    The default time period is one month.

    **Note:** You can change this time period at any time. Whenever you change the time period, the newly selected time period begins from the moment that you make the change.


## Create a Workfront integration profile

Create a Workfront integration profile to track software subscriptions and optimize licensing for your Workfront applications.

### Before you begin

To create a Workfront integration profile, request the Software Asset Management - SaaS License Management plugin \(sn\_sam\_saas\_int\) from the [ServiceNow Store](https://store.servicenow.com/).

ServiceNow Role required: sam\_integrator

**Important:** You must select the **Workfront Spoke** check box for this integration while installing optional features on the [Application Manager](https://www.servicenow.com/docs/access?context=application-manager&version=australia&pubname=australia-platform-administration&ft:locale=en-US) page. For more information about choosing the required SaaS applications, see [Request SaaS License Management](../task/request-saas-license-management.md).

### About this task

If you’re using Software Asset Workspace, the option to create the Workfront integration profile in Core UI is inactive.

### Procedure

1.  Navigate to the integration profile.

<table id="choicetable_o3p_z3k_qtb"><thead><tr><th align="left" id="d241495e379">

Interface

</th><th align="left" id="d241495e382">

Action

</th></tr></thead><tbody><tr><td id="d241495e388">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.
2.  Select **New**.
3.  Select **Workfront Integration Profile**.


</td></tr><tr><td id="d241495e430">

**Software Asset Workspace**

</td><td>

1.  Navigate to **License operations** &gt; **User Subscriptions** &gt; **Direct integration profiles**.
2.  Select **New**.
3.  Select **Workfront** from the drop-down list.
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

Name of the integration profile. For example, `Workfront Integration`.

</td></tr><tr><td>

Status

</td><td>

Status of the integration profile.-   If you have not published the integration profile, this field is automatically set to **Draft**.
-   If you have already published the integration profile, this field is automatically set to **Published**.


</td></tr><tr><td>

Profile Type

</td><td>

Type of integration profile. This field is automatically set to **Workfront Subscription**.

</td></tr></tbody>
</table>3.  Review the required user roles or API permissions specified in the **Vendor configuration** field for each process to minimize security risks and optimize SaaS licenses.

    **Note:** For more information, see [Minimal user permissions](integrate-with-workfront.md#) table.

    1.  In the Download Subscription Subflow section, verify that the **Subflow** field is set to **Workfront Download Subscriptions**.

        **Note:** The **Download subscriptions** check box is selected by default and you can't clear it.

    2.  In the Calculate Activity Subflow section, verify that the **Subflow** field is set to **Workfront Update User Activity**.

        **Note:** The **Download Activity** check box is selected by default. If you clear it, the activity scheduled job **SAM - Refresh &lt;displayname&gt; Activity** isn't created.

    3.  In the Reclaim Subscription Subflow section, verify that the **Subflow** field is set to **Workfront Reclaim Subscription**.

        **Note:** The **Reclaim subscriptions** check box is selected by default. If you don't want to reclaim subscriptions, you can clear this check box. If you clear it, the removal candidates are created but the reclaim subscription subflow isn't triggered or the reclamation process isn't initiated.

4.  Select **Save**.

    Your ServiceNow instance creates a draft integration profile.

    The **Connection &amp; Credential** field appears and is automatically set to **sn\_workfront\_spoke.Workfront**.

5.  Open the connection &amp; credential aliases record by selecting the preview icon ![](../image/preview-icon.png) next to the **Connection &amp; Credential** field and then selecting **Open Record** in the record preview.

6.  On the Connection &amp; Credential Aliases form, select the **Create New Connection &amp; Credential** related link.

7.  In the Create Connection and Credential dialog box, fill in the fields.

<table id="table_xd2_qht_lnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Connection Information

</td></tr><tr><td>

Connection Name

</td><td>

Name of the Workfront connection. This field populates automatically.

</td></tr><tr><td>

Connection URL

</td><td>

URL for the connection. Enter `https://<*domain-name*>.my.workfront.com`, where &lt;*domain-name*&gt; is your company subdomain.

</td></tr><tr><td colspan="2">

Credential Information

</td></tr><tr><td>

API Key

</td><td>

API key for your Workfront applications. Enter the same API key that you generated in [Generate a Workfront API key](integrate-with-workfront.md#).

</td></tr></tbody>
</table>8.  Select **Create**.

9.  On the integration profile form, select **Validate Connection** to verify the connection and credential details of this integration.

    Validating the connection verifies the Download Subscriptions and Calculate Activity APIs, but not the Reclaim Subscriptions APIs.

10. After the connection is verified, select **Publish**.

11. In the Publish Confirmation dialog box, select **OK**.

    **Note:** If you clear the **Download Activity** check box after the integration profile is published, you must revalidate the connections and then republish the integration profile because the following events occur:

    -   The **Status** field on the integration profile form changes to **Draft**.
    -   The **Validate connection** button shows up on the form.
    -   The current **SAM - Refresh &lt;displayname&gt; Activity** job gets deleted.
12. To optimize memory and avoid performance issues in your Workfront flow, you can turn off the flow engine reporting level.

    1.  Navigate to **System Properties** &gt; **All Properties**.

    2.  Select the **com.snc.process\_flow.reporting.level** system property.

    3.  On the System Property page, set the **Value** to `OFF`.

    4.  Select **Update**.

13. Reduce the number of items in the execution details.

    1.  Navigate to **System Properties** &gt; **All Properties**.

    2.  Select the **com.snc.process\_flow.reporting.datastream.item.lastn** system property.

    3.  On the System Property page, set the **Value** to 10.

    4.  Select **Update**.


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

