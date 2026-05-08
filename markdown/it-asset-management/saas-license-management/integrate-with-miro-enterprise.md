---
title: Integrating with Miro Enterprise
description: Integrating your Software Asset Management application with the Miro Enterprise application enables you to track your software subscriptions and to reclaim unused licenses.Create a Miro Enterprise OAuth 2.0 application to enable access to the Miro API.Enable SCIM \(System for Cross-domain Identity Management\) on your Miro Enterprise account so that you can generate an API access token for authenticating your Miro API requests.Create a Miro Enterprise integration profile to track software subscriptions and optimize licensing for your Miro Enterprise applications.
locale: en-US
release: australia
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 10
breadcrumb: [Integrate with SaaS applications, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Integrating with Miro Enterprise

Integrating your Software Asset Management application with the Miro Enterprise application enables you to track your software subscriptions and to reclaim unused licenses.

**Important:** Minimize security risks and protect information by granting access only to the necessary user or API permissions.

|Process|Required user role in the Miro Enterprise application|Authentication scopes|
|-------|-----------------------------------------------------|---------------------|
|Download subscriptions|Company admin|organizations:read|
|Pull user activity|Company admin|organizations:read|
|Reclaim subscription|Company admin|None|

## Create a Miro Enterprise OAuth 2.0 application

Create a Miro Enterprise OAuth 2.0 application to enable access to the Miro API.

### Before you begin

Miro Role required: Refer to the [Minimal user permissions](integrate-with-miro-enterprise.md#) table.

### Procedure

1.  From a web browser, open the [Miro Platform](https://developers.miro.com/docs).

2.  If you have not created any teams within your organization or you want to build and test the OAuth 2.0 application using fake data, [get a developer team](https://miro.com/app/dashboard/?createDevTeam=1).

3.  Sign in using your Company Admin credentials.

4.  On the page header of the Miro Platform, select the organization profile icon.

5.  On the side navigation panel, select **Your Apps**.

6.  Select **Create a new app**.

7.  In the Create new app dialog box, enter a name for the OAuth 2.0 application in the **App Name** field.

8.  Select the developer team for which you want to build the OAuth 2.0 application.

9.  Select **Create app**.

    The profile settings for your newly created app open.

10. In the App Credentials section, copy the values in the **Client ID** and **Client secret** fields and save them in a secure location for later use.

11. In the Redirect URI for OAuth 2.0 section, enter the URL of the OAuth provider that users are redirected to after authentication and then select **Add**.

    For example, `https://*instance*.service-now.com/oauth_redirect.do`, where &lt;*instance*&gt; is the name of your ServiceNow instance.

12. In the Permissions section, select the **organizations:read** OAuth scope.

    OAuth scopes specify the level of access that the application has to your protected resources. The organizations:read OAuth scope enables your application to read information about your organization and organization members.

13. Select **Install app and get OAuth token**.


### What to do next

Keep your organization profile open so that you can enable SCIM \(System for Cross-domain Identity Management\) on your Miro Enterprise account. For more information, see [Enable SCIM on your Miro Enterprise account](integrate-with-miro-enterprise.md#).

## Enable SCIM on your Miro Enterprise account

Enable SCIM \(System for Cross-domain Identity Management\) on your Miro Enterprise account so that you can generate an API access token for authenticating your Miro API requests.

### Before you begin

Miro Role required: Refer to the [Minimal user permissions](integrate-with-miro-enterprise.md#) table.

### Procedure

1.  On the side navigation panel of your Miro organization profile, select **Apps and integrations** and then select **Enterprise integrations**.

2.  On the Enterprise integrations page, select the option to enable **SCIM Provisioning**.

    The Miro account automatically generates and displays your API access token in the **API Token** field.

3.  Select the **Send an email invite to join Miro to provisioned users** check box to enable Miro to send email notifications to all users that have been provisioned using SCIM.

4.  Copy the API access token in the **API Token** field and secure it for later use.


## Create a Miro Enterprise integration profile

Create a Miro Enterprise integration profile to track software subscriptions and optimize licensing for your Miro Enterprise applications.

### Before you begin

To create a Miro Enterprise integration profile, request the Software Asset Management - SaaS License Management plugin \(sn\_sam\_saas\_int\) from the [ServiceNow Store](https://store.servicenow.com/).

ServiceNow Role required: sam\_integrator

**Important:** You must select the **Miro Spoke** check box for this integration while installing optional features on the [Application Manager](https://www.servicenow.com/docs/access?context=application-manager&version=australia&pubname=australia-platform-administration&ft:locale=en-US) page. For more information about choosing the required SaaS applications, see [Request SaaS License Management](../task/request-saas-license-management.md).

### About this task

If you’re using Software Asset Workspace, the option to create the Miro Enterprise integration profile in Core UI is inactive.

### Procedure

1.  Navigate to the integration profile.

<table id="choicetable_o3p_z3k_qtb"><thead><tr><th align="left" id="d179648e581">

Interface

</th><th align="left" id="d179648e584">

Action

</th></tr></thead><tbody><tr><td id="d179648e590">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.
2.  Select **New**.
3.  Select **Miro Enterprise Integration Profile**.


</td></tr><tr><td id="d179648e632">

**Software Asset Workspace**

</td><td>

1.  Navigate to **License operations** &gt; **User Subscriptions** &gt; **Direct integration profiles**.
2.  Select **New**.
3.  Select **Miro Enterprise** from the drop-down list.
4.  Select **Continue**.


</td></tr></tbody>
</table>2.  On the form, fill in the following fields.

<table id="table_kr5_hf4_tnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display Name

</td><td>

Name of the integration profile. For example, `Miro Enterprise Integration`.

</td></tr><tr><td>

Status

</td><td>

Status of the integration profile.-   If you have not published the integration profile, this field is automatically set to **Draft**.
-   If you have already published the integration profile, this field is automatically set to **Published**.


</td></tr><tr><td>

Profile Type

</td><td>

Type of integration profile. This field is automatically set to **Miro Enterprise Subscription**.

</td></tr></tbody>
</table>3.  Review the required user roles or API permissions specified in the **Vendor configuration** field for each process to minimize security risks and optimize SaaS licenses.

    **Note:** For more information about the required roles and scopes, see [Minimal user permissions](integrate-with-miro-enterprise.md#) table.

4.  Select **Save**.

    A draft integration profile is created.

5.  In the Download Subscription Subflow section, verify that the **Connection &amp; credential** field is set to **sn\_miro\_spoke.Miro\_Enterprise** and the Subflow field is set to **Miro Download Subscriptions**.

    **Note:** The **Download subscriptions** check box is selected by default and you can't clear it.

    1.  Open the connection &amp; credential aliases record by selecting the preview icon ![](../image/preview-icon.png) next to the **Connection &amp; Credential** field and then selecting **Open Record** in the record preview.

    2.  On the Connection &amp; Credential Aliases form, select the **Create New Connection &amp; Credential** related link.

    3.  In the Create Connection and Credential dialog box, fill in the fields.

<table id="table_xd2_qht_lnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Connection Information

</td></tr><tr><td>

Connection Name

</td><td>

Name of the Miro Enterprise connection. This field populates automatically.

</td></tr><tr><td colspan="2">

Credential Information

</td></tr><tr><td>

OAuth Client ID

</td><td>

Client ID that is assigned to your Miro Enterprise OAuth 2.0 application.

</td></tr><tr><td>

OAuth Client Secret

</td><td>

Client secret that is assigned to your Miro Enterprise OAuth 2.0 application.

</td></tr><tr><td>

OAuth Redirect URL

</td><td>

URL of the OAuth provider that users are redirected to after authentication. This field populates automatically based on the redirect URL that you specified in [Create a Miro Enterprise OAuth 2.0 application](integrate-with-miro-enterprise.md#).

</td></tr></tbody>
</table>    4.  Select **Create and Get OAuth Token**.

        **Important:** This step must be executed by a ServiceNow admin with the Company Admin role in Miro.

    5.  On the Miro OAuth authorization dialog box, locate the team that you built the Miro Enterprise OAuth 2.0 application for and then select **Install**.

        **Note:** If another ServiceNow instance is using the same credentials, you would be prompted for a reinstall.

        The OAuth access token becomes available for authorizing your Miro Enterprise connection.

6.  In the Reclaim Subscription Subflow section, verify that the **Connection &amp; credential** field is set to **sn\_miro\_spoke.Miro\_Enterprise\_SCIM** and the **Subflow** field is set to **Miro Reclaim Subscription**.

    **Note:** The **Reclaim subscriptions** check box is selected by default. If you don't want to reclaim subscriptions, you can clear this check box. If you clear it, the removal candidates are created but the reclaim subscription subflow isn't triggered or the reclamation process isn't initiated.

    1.  Open the connection &amp; credential aliases record by selecting the preview icon \(![Preview icon.](../image/preview-icon.png)\) next to the **Connection &amp; Credential** field and then selecting **Open Record** in the record preview.

    2.  On the Connection &amp; Credential Aliases form, select the **Create New Connection &amp; Credential** related link.

    3.  In the Create Connection and Credential dialog box, fill in the fields.

<table id="table_create_conn_miro_scim"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Connection Information

</td></tr><tr><td>

Connection Name

</td><td>

Name of the Miro Enterprise SCIM connection. This field populates automatically.

</td></tr><tr><td colspan="2">

Credential Information

</td></tr><tr><td>

API Token

</td><td>

API access token for authenticating Miro API requests. Enter the same API access token that you generated and copied in [Enable SCIM on your Miro Enterprise account](integrate-with-miro-enterprise.md#).

</td></tr></tbody>
</table>    4.  Select **Create**.

        The dialog box closes and you automatically return to the integration profile form.

7.  On the integration profile form, select **Validate Connection** to verify the connection and credential details of this integration.

    Validating the connection verifies the Download Subscriptions APIs, but not the Reclaim Subscriptions APIs.

8.  After the connection is validated, select **Publish**.

9.  In the Publish Confirmation dialog box, select **OK**.


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

