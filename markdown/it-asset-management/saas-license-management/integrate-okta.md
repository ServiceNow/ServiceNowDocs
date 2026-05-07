---
title: Integrating with Okta
description: You can integrate your ServiceNow instance with Okta to view software usage for all connected SSO applications.Create an Okta application that you can integrate with the ServiceNow AI Platform.Create an Okta integration profile in your ServiceNow instance.Okta SSO direct integration profile helps you manage Okta user licenses by creating subscriptions for Okta users while setting up an Okta SSO integration.Connect an SSO application to monitor all the users and groups who have access to that application. While SSO integration provides a summary of application usage and activity, direct integration offers detailed insights into these metrics.
locale: en-US
release: australia
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 14
breadcrumb: [Integrate with SSO providers, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Integrating with Okta

You can integrate your ServiceNow instance with Okta to view software usage for all connected SSO applications.

**Important:** Minimize security risks and protect information by granting access only to the necessary user or API permissions.

<table id="table_box"><thead><tr><th>

Process

</th><th>

Required user role in the Okta application

</th><th>

Authentication scopes

</th></tr></thead><tbody><tr><td>

Download users

</td><td>

Read-only administrator

</td><td>

okta.users.read

</td></tr><tr><td>

-   Download groups
-   Download group memberships

</td><td>

Read-only administrator

</td><td>

okta.groups.read

</td></tr><tr><td>

Download applications

</td><td>

Read-only administrator

</td><td>

-   okta.apps.read
-   okta.logs.read

</td></tr><tr><td>

Connect applications

</td><td>

Read-only administrator

</td><td>

okta.logs.read

</td></tr><tr><td>

Update connected applications

</td><td>

Read-only administrator

</td><td>

-   okta.apps.read
-   okta.logs.read

</td></tr><tr><td>

Reclaim subscriptions

</td><td>

Application administrator

</td><td>

okta.apps.manage

</td></tr></tbody>
</table>**Parent Topic:**[Integrate with SSO providers](saas-sso-integration.md)

## Create an Okta application

Create an Okta application that you can integrate with the ServiceNow AI Platform.

### Before you begin

Okta Role required: Refer the [Minimal user permissions](integrate-okta.md#) table.

See [Administrator roles and permissions](https://help.okta.com/en/prod/Content/Topics/Security/administrators-admin-comparison.htm) for more details on Okta admin roles and [Scopes and supported endpoints](https://developer.okta.com/docs/guides/implement-oauth-for-okta/scopes/) for more details on Okta OAuth scopes.

### Procedure

1.  From a web browser, log in to the [Okta administrator console](https://login.okta.com/).

2.  Create an Okta application with OAuth 2.0 functionality.

    See [Create an OAuth 2.0 app for Okta](https://developer.okta.com/docs/guides/implement-oauth-for-okta/create-oauth-app/) for detailed instructions.

    Keep the following points in mind when you’re creating your Okta application:

    -   In the **Login redirect URI** and **Logout redirect URI** fields, enter `https://<instance-name>.service-now.com/oauth_redirect.do`, where &lt;*instance-name*&gt; is the name of your ServiceNow instance.
    -   Copy the values in the **Client ID** and **Client Secret** fields. Save them in a secure location for later use.
    -   Grant the following scopes to your Okta OAuth 2.0 application:
        -   okta.groups.read
        -   okta.apps.read
        -   okta.users.read
        -   okta.logs.read
        -   okta.apps.manage
    -   Select the **Refresh Token** check box under the **Client acting on behalf of a user** Grant type on the Okta portal.

## Create an Okta integration profile

Create an Okta integration profile in your ServiceNow instance.

### Before you begin

To create an Okta integration profile, request the Software Asset Management - SaaS License Management plugin \(sn\_sam\_saas\_int\) from the [ServiceNow Store](https://store.servicenow.com/).

ServiceNow Role required: sam\_integrator

**Important:** You must select the **Okta Spoke** check box for this integration while installing optional features on the [Application Manager](https://www.servicenow.com/docs/access?context=application-manager&version=australia&pubname=australia-platform-administration&ft:locale=en-US) page. For more information about choosing the required SaaS applications, see [Request SaaS License Management](../task/request-saas-license-management.md).

### About this task

**Note:** Starting with version 7.0.0 of Software Asset Management - SaaS License Management and version 4.1.2 of the Okta spoke, your ServiceNow instance creates a separate Okta connection for each Okta integration profile that you create. Each connection runs independently of each other, which enables your instance to support multiple independent Okta integration profiles.

If you’re using Software Asset Workspace, the option to create the Okta integration profile in Core UI is inactive.

### Procedure

1.  Navigate to the integration profile.

<table id="choicetable_fcx_4nx_qtb"><thead><tr><th align="left" id="d120041e515">

Interface

</th><th align="left" id="d120041e518">

Action

</th></tr></thead><tbody><tr><td id="d120041e524">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **SSO Integration Profiles**.
2.  Select **New**.
3.  Select **Okta Integration Profile**.


</td></tr><tr><td id="d120041e566">

**Software Asset Workspace**

</td><td>

1.  Navigate to **License operations** &gt; **User Subscriptions** &gt; **SSO integration profiles**.
2.  Select **New**.
3.  Select **Okta** from the drop-down list.
4.  Select **Continue**.


</td></tr></tbody>
</table>2.  On the form, fill in the fields.

<table id="table_d1s_gp2_2nb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display name

</td><td>

Name of the integration profile. For example, `Okta Integration`.

</td></tr><tr><td>

Status

</td><td>

Status of the integration profile.-   If you haven’t published the integration profile, this field is automatically set to **Draft**.
-   If you’ve already published the integration profile, this field is automatically set to **Published**.


</td></tr><tr><td>

Directory integration

</td><td>

A reference to the directory integration profile, which is used to pull the active directory users, groups, and group memberships of an organization.-   If a directory integration record for Okta exists, you can select the existing record.
-   If a directory integration record for Okta doesn't exist, a new record is created when you save or submit this form.


</td></tr><tr><td>

Profile type

</td><td>

Type of the integration profile. This field is automatically set to **Okta**.

</td></tr><tr><td>

Connection &amp; Credential

</td><td>

Reference to the connection and credential alias that is used in the directory and SSO integration.

 -   If a directory integration record exists and you select it in the directory integration field, this field is automatically set to the connection and credential alias of the directory integration record.
-   If a directory integration value doesn't exist, this field is automatically populated.


</td></tr><tr><td>

Create Okta subscriptions

</td><td>

Option for creating a direct integration profile to view Okta subscriptions after this integration profile is published.Default value: False

</td></tr></tbody>
</table>3.  In the Process configuration section, view the required user roles or API permissions to minimize security risks and optimize SaaS licenses.

    **Note:** For more information about the required roles and scopes, see [Minimal user permissions](integrate-okta.md#) table.

    -   The **Download applications, users, and groups** check box is selected by default and you can't clear it.

    -   The **Download Activity** check box is selected by default. If you clear it,the last activity for connected applications isn't pulled.
    -   The **Reclaim subscriptions** check box is selected by default. If you don't want to reclaim subscriptions, you can clear this check box. If you clear it, the removal candidates are created but the reclaim subscription subflow isn't triggered or the reclamation process isn't initiated.

4.  Select **Submit**.

    The **Connection &amp; Credential** field is automatically set to **sn\_okta\_spoke.&lt;okta\_profile\_name&gt;\_apps\_users\_groups\_activity\_and\_reclaim**.

    **Note:** The automatically populated value in the **Connection &amp; credential** field changes based on the selection in the **Download activity** and **Reclaim subscriptions** check boxes.

    |Selection|Connection &amp; credential value|
    |---------|---------------------------------|
    |Both **Download activity** and **Reclaim subscriptions** are selected.|sn\_okta\_spoke.&lt;okta\_profile\_name&gt;\_apps\_users\_groups\_activity\_and\_reclaim|
    |Only **Download activity** is selected.|sn\_okta\_spoke.&lt;okta\_profile\_name&gt;\_apps\_users\_groups\_activity|
    |Only **Reclaim subscriptions** is selected.|sn\_okta\_spoke.&lt;okta\_profile\_name&gt;\_apps\_users\_groups\_activity\_and\_reclaim|
    |Both **Download activity** and **Reclaim subscriptions** aren’t selected.|sn\_okta\_spoke.&lt;okta\_profile\_name&gt;\_apps\_users\_groups\_activity|

5.  Open the Create Connection and Credential dialog box.

<table id="choicetable_oww_kmj_lzb"><thead><tr><th align="left" id="d120041e945">

Interface

</th><th align="left" id="d120041e948">

Action

</th></tr></thead><tbody><tr><td id="d120041e954">

**Core UI**

</td><td>

Select the **Create New Connection &amp; Credential** related link on the SSO integration profile form.

</td></tr><tr><td id="d120041e966">

**Software Asset Workspace**

</td><td>

1.  Selecting the preview icon ![](../image/preview-icon.png) next to the **Connection &amp; Credential** field
2.  Select **Open Record** in the record preview.
3.  On the Connection &amp; Credential Aliases form, select the **Create New Connection &amp; Credential** related link.


</td></tr></tbody>
</table>6.  In the dialog box, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|Name of the connection. For example, `Okta Connection`.|
    |Connection URL|URL for the connection. Enter `https://<*yourOktaDomain*>.com`, where &lt;*yourOktaDomain*&gt; is your organization domain.|
    |Authorization URL|URL of the OAuth authorization endpoint. Enter `https://<*yourOktaDomain*>.com/oauth2/v1/authorize`, where &lt;*yourOktaDomain*&gt; is your organization domain.|
    |Token URL|URL of the OAuth endpoint that retrieves and refreshes access tokens. Enter `https://<*yourOktaDomain*>.com/oauth2/v1/token`, where &lt;*yourOktaDomain*&gt; is your organization domain.|
    |Token Revocation URL|URL of the OAuth endpoint that revokes access tokens. Enter `https://<*yourOktaDomain*>.com/oauth2/v1/revoke`, where &lt;*yourOktaDomain*&gt; is your organization domain.|
    |OAuth Client ID|Client ID that is assigned to your Okta application.|
    |OAuth Client Secret|Client secret that is assigned to your Okta application.|
    |OAuth Redirect URL|URL of the OAuth provider that users are redirected to after authentication. This field is automatically set to **https://&lt;instance-name&gt;.service-now.com/oauth\_redirect.do**, where &lt;*instance-name*&gt; is the name of your ServiceNow instance.|

7.  Select **Create and Get OAuth Token**.

    **Note:** You must sign in using the same credentials as the user with the required role. For the role required to perform this step, refer to the [Minimal user permissions](integrate-okta.md#) table.

8.  On the integration profile form, select **Validate Connection** to verify the connection and credential details of this integration.

9.  After the connection is verified, select **Publish**.

10. In the Publish Confirmation dialog box, select **OK**.

    If you clear the **Download Activity** check box after the integration profile is published, you must revalidate the connections because the following events occur:

    -   The **Validate connection** button shows up on the form.
    -   The last activity for users of the connected applications isn't pulled anymore.

### Result

Both scheduled jobs and directory jobs download a list of all applications, users, groups, and software subscriptions that are associated with your Okta application. View the status of your job in the **Scheduled Jobs Results** and **Directory Job Results** tabs of your integration profile. Software Asset Management automatically creates software models for applications with an external catalog ID that matches an **Identifier** in the Subscription Product Definitions \[samp\_sw\_subscription\_product-definition\] table.

### What to do next

If you’ve selected the **Create Okta subscriptions** check box and this integration profile is published, a direct integration profile for Okta gets created. You can navigate to the direct integration profile by selecting the **Direct integration profile** link in the information message.

After you’ve navigated to the direct integration profile, you can view Okta subscriptions by selecting the **Software Subscriptions** tab. For more information, see [Okta SSO direct integration profile](integrate-okta.md#).

**Warning:**

When your OAuth token expires, your Okta integration profile displays an error message indicating that you must get a new OAuth token. Select the link in the error message to get the new OAuth token.

Don’t delete the OAuth 2.0 credential record that is associated with the connection record for your Okta integration profile. If you delete the OAuth 2.0 credential record, you won’t be able to get a new OAuth token after your current OAuth token expires.

After you publish the integration profile and connect applications to the profile, you can view events performed by individual users up to 60 days prior to the current date. For more information, see [Review a software reclamation rule](../task/add-reclamation-rule-sub.md).

## Okta SSO direct integration profile

Okta SSO direct integration profile helps you manage Okta user licenses by creating subscriptions for Okta users while setting up an Okta SSO integration.

<table id="table_xhh_slg_hzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display name

</td><td>

Name of the integration profile.

</td></tr><tr><td>

Status

</td><td>

Status of the integration profile.This field is automatically set to **Published**.

</td></tr><tr><td>

Profile type

</td><td>

Type of integration profile. This field is automatically set to **Okta Subscription**.

</td></tr><tr class="sub-head"><td>

Download Subscription Subflow

</td><td>

 

</td></tr><tr><td>

Subflow

</td><td>

This field is automatically set to **Okta Download Subscriptions**.

</td></tr></tbody>
</table>## Connect SSO applications

Connect an SSO application to monitor all the users and groups who have access to that application. While SSO integration provides a summary of application usage and activity, direct integration offers detailed insights into these metrics.

### Before you begin

ServiceNow Role required: sam\_integrator

### About this task

ServiceNow® SaaS License Management offers direct integrations with some applications. Direct integrations provide the most comprehensive usage data. For a list of available direct integrations, see [Integrate with SaaS applications](create-integration-profile.md).

If you have already created a direct integration for an application, then connecting the same application in an SSO integration creates duplicate subscription records in your ServiceNow instance. You should only use the direct integration. If you connect an application in an SSO integration, but you later want to create a direct integration for that application, then disconnect the application before creating the direct integration.

### Procedure

1.  Navigate to **All** &gt; **SaaS License** &gt; **SSO Applications**.

2.  Select the application that you want to connect.

3.  If the **Software model** field is empty, add a software model for the application.

    Before you can connect an application, it must be associated with a software model. ServiceNow® Software Asset Management automatically creates software models for applications with an external catalog ID that matches an **Identifier** in the Subscription Product Definitions \[samp\_sw\_subscription\_product\_definition\] table. For all other applications, you can create a software model manually. For detailed instructions, see [Create software models in Software Asset Management classic](../task/record-terms-software-licenses.md).

4.  Select the **Enable group based software model** check box for mapping an SSO group with a specific software model for the application.

    For example, if an application has multiple license models that are linked to specific groups, then you can map a group to a software model to optimize license usage.

    **Important:** If you select this option, you must create a mapping for the SSO group before connecting the application. After the mapping is complete, the SSO subscriptions get automatically created or updated according to the mapped software model. For more information, see [Create an SSO group software model mapping](../task/create-ssogrp-swmodel-mapping.md).

5.  Select the date that you want to analyze the last activity from in the **Analyze last activity from** field.

    You can start analyzing login data for individual users and applications from the current date or from up to 60 days earlier. The default value is 30 days. If you select a date prior to the current date, it may take longer for results to appear due to the amount of data that you want to analyze.

    After you submit a value in the **Analyze last activity from** field, the field becomes read only.

6.  Select **Connect**.

    **Tip:** To connect multiple applications simultaneously, select the check box for each application that you want to connect in the SSO Applications list. Select the Actions on the selected row menu and then select **Connect**. If any applications aren’t associated with a software model, the name of the **Connect** menu item is updated to indicate that only some of the applications are connected. For example, a **Connect \(1 of 4\)** menu item indicates that only 1 of the four apps that you selected are connected. Add software models to the remaining applications to proceed with the connections.


### What to do next

After the SSO application connects, your ServiceNow instance automatically creates users, groups, subscriptions, and reclamation rules that are refreshed daily. If you delete a user, application, group, or group membership from the Okta Developer Console, the changes are reflected on your ServiceNow instance.

Review all automatically generated reclamation rules to confirm that they meet your specifications for reclaiming user subscriptions. For more information, see [Review a software reclamation rule](../task/add-reclamation-rule-sub.md).

After connecting the SSO application, view information about the SSO profile in the Software Asset Workspace by navigating to **License operations** &gt; **User subscription** &gt; **SSO integration profiles**. You can select an integration profile to view the following related lists.

-   SSO Applications
-   Directory Users
-   Scheduled Jobs
-   Scheduled Job Results
-   Directory Jobs
-   Directory Job Results
-   Subscription User Exclusion Rule

After creating an integration profile, you can define subscription exclusion rules to keep certain subscriptions from license cost calculations. For more information, see [Subscription exclusions for SaaS and SSO applications](subscription-exclusions.md#).

Create software entitlements for the automatically generated software models to track used software against owned software. For more information on creating software entitlements in the Software Asset Management classic application, see [Create entitlements in Software Asset Management classic](../task/track-software-rights.md). For more information on creating software entitlements in the Software Asset Workspace, see [Create entitlements in workspace](../task/create-entitlements-workspace.md). For more information on creating software entitlements using the Software Asset Management Playbook, see [Create entitlements using the guided walk-through](../task/guidedwalk-workspace.md).

Reconciliation also runs on your subscriptions as a scheduled job or on-demand. You can view your reconciliation results in the [License Workbench](sam-license-workbench.md) \(Software Asset Management classic application\) or the [License usage view](sam-workspace-workbench.md) \(Software Asset Workspace\). Use these results to determine your license compliance position and to remediate any non-compliance. For more information on running reconciliation in the Software Asset Management classic application, see [Run software reconciliation in Software Asset Management classic](../task/t_RunReconciliation.md). For more information on running reconciliation in the Software Asset Workspace, see [Run software reconciliation in the workspace](../task/run-recon-workspace.md).

