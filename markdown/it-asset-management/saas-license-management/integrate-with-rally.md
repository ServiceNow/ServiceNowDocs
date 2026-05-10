---
title: Integrating with Rally
description: Integrating your Software Asset Management application with the Broadcom Rally application enables you to track your software subscriptions and to reclaim unused licenses.Register the Rally OAuth application to access the Rally API 2.0 and to receive a Client ID and Client secret.Create a Rally integration profile to track software subscriptions and optimize licensing for your Rally solutions.
locale: en-US
release: australia
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Integrate with SaaS applications, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Integrating with Rally

Integrating your Software Asset Management application with the Broadcom Rally application enables you to track your software subscriptions and to reclaim unused licenses.

**Important:** Minimize security risks and protect information by granting access only to the necessary user or API permissions.

|Process|Required user role in the Rally application|Authentication scopes|
|-------|-------------------------------------------|---------------------|
|Download subscriptions|Workspace admin|None|
|Pull user activity|Workspace admin|None|
|Reclaim subscription|Workspace admin|None|

## Register a Rally OAuth application

Register the Rally OAuth application to access the Rally API 2.0 and to receive a Client ID and Client secret.

### Before you begin

The Rally Integration Hub spoke must be active. For more information, see [Rally spoke](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/integrate-applications/integration-hub/rally-spoke.md).

Rally Role required: Refer to the [Minimal user permissions](integrate-with-rally.md#) table.

### Procedure

1.  Log in to [CA Agile Central](https://rally1.rallydev.com/login/accounts/index.html) by using your admin credentials.

2.  On the page header, select your profile and then select **My Settings**.

3.  Navigate to **Access** &gt; **OAUTH CLIENTS**.

4.  Select **Create**.

5.  In the dialog box, fill in the fields.

    |Field|Value|
    |-----|-----|
    |Application Name|Provide a name for the application.|
    |Callback URL|Callback URL of the ServiceNow instance to which the application is to be integrated. For example, `https://<instance_url>/oauth_redirect.do`.|

6.  Select **Next**.

7.  Copy the Client ID and Client secret for later use.


## Create a Rally integration profile

Create a Rally integration profile to track software subscriptions and optimize licensing for your Rally solutions.

### Before you begin

The Software Asset Management - SaaS License Management plugin \(sn\_sam\_saas\_int\) must be installed from the [ServiceNow Store](https://store.servicenow.com/).

Role required: sam\_integrator

**Important:** You must select the **Rally Spoke** check box for this integration while installing optional features on the [Application Manager](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/application-manager/application-manager.md) page. For more information about choosing the required SaaS applications, see [Request SaaS License Management](../task/request-saas-license-management.md).

### About this task

If you’re using Software Asset Workspace, the option to create the Rally integration profile in Core UI is inactive.

### Procedure

1.  Navigate to the integration profile.

<table id="choicetable_o3p_z3k_qtb"><thead><tr><th align="left" id="d221459e428">

Interface

</th><th align="left" id="d221459e431">

Action

</th></tr></thead><tbody><tr><td id="d221459e437">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.
2.  Select **New**.
3.  Select **Rally Integration Profile**.


</td></tr><tr><td id="d221459e479">

**Software Asset Workspace**

</td><td>

1.  Navigate to **License operations** &gt; **User Subscriptions** &gt; **Direct integration profiles**.
2.  Select **New**.
3.  Select **Rally** from the drop-down list.
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

Name of the integration profile. For example, Rally integration.

</td></tr><tr><td>

Status

</td><td>

Status of the integration profile. -   If you have not published the integration profile, this field is automatically set to  **Draft**.
-   If you have already published the integration profile, this field is automatically set to  **Published**.


</td></tr><tr><td>

Profile type

</td><td>

Type of integration profile. This field is automatically set to Rally Subscription.

</td></tr></tbody>
</table>3.  Review the required user roles or API permissions specified in the **Vendor configuration** field for each process to minimize security risks and optimize SaaS licenses.

    **Note:** For more information, see [Minimal user permissions](integrate-with-rally.md#) table.

    1.  In the Download Subscription Subflow section, verify that the **Subflow** field is set to **Rally Download Subscriptions**.

        **Note:** The **Download subscriptions** check box is selected by default and you can't clear it.

    2.  In the Reclaim Subscription Subflow section, verify that the **Subflow** field is set to **Rally Reclaim Subscription**.

        **Note:** The **Reclaim subscriptions** check box is selected by default. If you don't want to reclaim subscriptions, you can clear this check box. If you clear it, the removal candidates are created but the reclaim subscription subflow isn't triggered or the reclamation process isn't initiated.

4.  Select **Save**.

    A draft integration profile is created.

    The **Connection &amp; Credential** field appears and is automatically set to **sn\_rally\_spoke.Rally**.

5.  Open the connection &amp; credential aliases record by selecting the preview icon ![](../image/preview-icon.png) next to the **Connection &amp; Credential** field and then selecting **Open Record** in the record preview.

6.  On the Connection &amp; Credential Aliases form, select the **Create New Connection &amp; Credential** related link.

7.  In the Create Connection and Credential dialog box, fill in the fields.

    |Field|Value|
    |-----|-----|
    |Connection Information|
    |Connection Name|Name of the Rally connection. This field populates automatically.|
    |Connection URL|URL for the connection. This field is automatically set to `https://rally1.rallydev.com/slm/webservice`.|
    |Credential Information|
    |OAuth Client ID|Client ID that you generated while configuring Rally API settings.|
    |OAuth Client Secret|Client Secret that you generated while configuring Rally API settings.|
    |OAuth Redirect URL|`https://<instance_name>/oauth_redirect.do`, where instance name is the name of your ServiceNow instance.|

8.  Select **Create and Get OAuth Token**.

    **Note:** For the role required to perform this step, refer to the [Minimal user permissions](integrate-with-rally.md#) table.

9.  On the integration profile form, select **Validate Connection** to verify the connection and credential details of this integration.

    Validating the connection verifies the Download Subscriptions APIs, but not the Reclaim Subscriptions APIs.

    The dialog box closes and you automatically return to the integration profile form.

10. After the connection is verified, select **Publish**.

11. In the Publish Confirmation dialog box, select **OK**.


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

