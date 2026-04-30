---
title: Integrating with Zendesk
description: Integrating your Software Asset Management application with the Zendesk application enables you to track your software subscriptions and to reclaim unused licenses.Create an OAuth client for authenticating Zendesk API requests.Create a connection between your Zendesk applications and your ServiceNow instance so that your instance can retrieve user data from your applications.Create a Zendesk integration profile to track software subscriptions and optimize licensing for your Zendesk applications.
locale: en-US
release: xanadu
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Integrate with SaaS applications, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Integrating with Zendesk

Integrating your Software Asset Management application with the Zendesk application enables you to track your software subscriptions and to reclaim unused licenses.

**Important:** Minimize security risks and protect information by granting access only to the necessary user or API permissions.

|Process|Required user role in the Zendesk application|Authentication scopes|
|-------|---------------------------------------------|---------------------|
|Download subscriptions|Light Agent|None|
|Pull user activity|Light Agent|None|
|Reclaim subscription|admin|None|

## Create a Zendesk OAuth client

Create an OAuth client for authenticating Zendesk API requests.

### Before you begin

Zendesk Role required: admin

### Procedure

1.  From a web browser, open [Zendesk](https://www.zendesk.com).

2.  Log in using your admin credentials.

3.  On the left navigation menu of the Zendesk Agent Workspace, select the Admin icon \(![Admin icon.](../image/admin-icon.png)\).

4.  Go to the Admin Center from the Admin page and from the Admin menu, navigate to **Apps and Integrations** &gt; **API**.

    The Zendesk API page opens.

5.  Select the **OAuth Clients** tab and then select **Add OAuth client**.

6.  On the form, fill in the fields.

<table id="table_aym_sgf_cqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Client name

</td><td>

Name of the OAuth client.

</td></tr><tr><td>

Description

</td><td>

Brief description of the OAuth client.

</td></tr><tr><td>

Company

</td><td>

Name of the company whose data the OAuth client grants access to through the Zendesk API. The company name is displayed during authentication of your Zendesk API requests.This field populates automatically based on the company that your Zendesk account is associated with. However, you can modify the company name as needed.

</td></tr><tr><td>

Logo

</td><td>

Logo that is displayed during authentication of your Zendesk API requests. Select the green square to locate and select the logo that you want to display.

</td></tr><tr><td>

Unique identifier

</td><td>

Unique identifier for the OAuth client. This field populates automatically based on the OAuth client name that you specified in the **Client name** field. However, you can modify the unique identifier as needed.**Note:** The unique identifier is used only in the Zendesk code.

</td></tr><tr><td>

Client kind

</td><td>

This field must be set to **Confidential**. Confidential authentication clients run on secure servers, where their credentials can be kept safe.

</td></tr><tr><td>

Redirect URLs

</td><td>

URL of the OAuth provider that users are redirected to after authentication. Enter `https://*instance*.service-now.com/oauth_redirect.do`, where &lt;*instance*&gt; is the name of your ServiceNow instance.

</td></tr></tbody>
</table>7.  Select **Save**.

8.  On the dialog box, select **OK**.

    The dialog box closes and the form reloads.

9.  Copy the value from the **Secret** field.

    Save the Secret value in a secure location for later use.


## Create a Zendesk connection

Create a connection between your Zendesk applications and your ServiceNow instance so that your instance can retrieve user data from your applications.

### Before you begin

ServiceNow Role required: admin

### Procedure

1.  From your ServiceNow instance, navigate to **Process Automation** &gt; **Flow Designer**.

    The Flow Designer launches in a new tab.

2.  Select the **Connections** tab.

3.  Locate your Zendesk connection and then select **Configure**.

4.  In the dialog box, fill in the fields.

<table id="table_xd2_qht_lnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Connection Information

</td></tr><tr><td>

Connection Name

</td><td>

Name of the Zendesk connection. This field populates automatically.

</td></tr><tr><td>

Connection URL

</td><td>

URL for the connection. Enter `https://<subdomain>.zendesk.com`, where &lt;*subdomain*&gt; is your organization subdomain.

</td></tr><tr><td colspan="2">

Credential Information

</td></tr><tr><td>

OAuth Client ID

</td><td>

Unique identifier for your Zendesk OAuth client. Enter the same unique identifier that you specified in [Create a Zendesk OAuth client](integrate-with-zendesk.md#).

</td></tr><tr><td>

OAuth Client Secret

</td><td>

Secret that is assigned to your Zendesk OAuth client. Enter the same secret that you copied in [Create a Zendesk OAuth client](integrate-with-zendesk.md#).

</td></tr><tr><td>

OAuth Redirect URL

</td><td>

URL of the OAuth provider that users are redirected to after authentication. This field populates automatically based on the redirect URL that you specified in [Create a Zendesk OAuth client](integrate-with-zendesk.md#).

</td></tr></tbody>
</table>5.  Select **Create and Get OAuth Token**.

    **Note:** For the role required to perform this step, refer to the [Minimal user permissions](integrate-with-zendesk.md#) table.

6.  On the Zendesk OAuth authorization dialog box, select **Authorize**.

    The OAuth access token becomes available for authorizing your Zendesk connection.


## Create a Zendesk integration profile

Create a Zendesk integration profile to track software subscriptions and optimize licensing for your Zendesk applications.

### Before you begin

To create a Zendesk integration profile, request the Software Asset Management - SaaS License Management plugin \(sn\_sam\_saas\_int\) from the [ServiceNow Store](https://store.servicenow.com/).

ServiceNow Role required: sam\_integrator or admin

### About this task

If you’re using Software Asset Workspace, the option to create the Zendesk integration profile in Core UI is inactive.

### Procedure

1.  Navigate to the integration profile.

<table id="choicetable_o3p_z3k_qtb"><thead><tr><th align="left" id="d62173e792">

Interface

</th><th align="left" id="d62173e795">

Action

</th></tr></thead><tbody><tr><td id="d62173e801">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.
2.  Select **New**.
3.  Select **Zendesk Integration Profile**.


</td></tr><tr><td id="d62173e843">

**Software Asset Workspace**

</td><td>

1.  Navigate to **License operations** &gt; **User Subscriptions** &gt; **Direct integration profiles**.
2.  Select **New**.
3.  Select **Zendesk** from the drop-down list.
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

Name of the integration profile. For example, `Zendesk Integration`.

</td></tr><tr><td>

Connection &amp; Credential

</td><td>

Connection and credential alias for the Zendesk spoke. This field is automatically set to **sn\_zendesk\_spoke.Zendesk**.

</td></tr><tr><td>

Status

</td><td>

Status of the integration profile.-   If you have not published the integration profile, this field is automatically set to **Draft**.
-   If you have already published the integration profile, this field is automatically set to **Published**.


</td></tr><tr><td>

Profile Type

</td><td>

Type of integration profile. This field is automatically set to **Zendesk Subscription**.

</td></tr></tbody>
</table>3.  On the **Download Subscription Subflow** tab, verify that the **Subflow** field is set to **Zendesk Download Subscriptions**.

    You can view events performed by individual users up to one year prior to the current date. For more information, see [Review a software reclamation rule](../task/add-reclamation-rule-sub.md).

    **Note:** Software Asset Management pulls the events from the time that you start downloading user subscriptions irrespective of the profile creation date.

4.  On the **Reclaim Subscription Subflow** tab, verify that the **Subflow** field is set to **Zendesk Reclaim Subscription**.

5.  Select **Save**.

    Your ServiceNow instance creates a draft integration profile. The integration profile uses the Zendesk Download Subscriptions and Zendesk Reclaim Subscription subflows to retrieve user data from the Zendesk application.

6.  After the form reloads, select **Publish**.


### What to do next

After the integration connects, your ServiceNow instance automatically creates software models, reclamation rules, and software subscriptions that are refreshed daily.

If you want to set up multiple integration profiles with unique connections, create child aliases to manage different configurations and settings for each integration profile. For more information, see [Create a child alias to set up multiple integration profiles](../task/create-child-alias-saas.md).

Review all automatically generated reclamation rules to reclaim user subscriptions. For more information, see [Review a software reclamation rule](../task/add-reclamation-rule-sub.md).

Create software entitlements for the automatically generated software models to track used software against owned software.

-   For more information on creating software entitlements in the Software Asset Management Core UI, see [Create entitlements in Software Asset Management classic](../task/track-software-rights.md).
-   For more information on creating software entitlements in the Software Asset Workspace, see [Create entitlements in workspace](../task/create-entitlements-workspace.md).
-   For more information on creating software entitlements using the Software Asset Management Playbook, see [Create entitlements using the guided walk-through](../task/guidedwalk-workspace.md).

Reconciliation also runs on your subscriptions as a scheduled job or on-demand. You can view your reconciliation results in the [License Workbench](sam-license-workbench.md) \(Software Asset Management classic application\) or the [License usage view](sam-workspace-workbench.md) \(Software Asset Workspace\). Use these results to determine your license compliance position and to remediate any non-compliance.

-   For more information on running reconciliation in the Software Asset Management classic application, see [Run software reconciliation](../task/t_RunReconciliation.md).
-   For more information on running reconciliation in the Software Asset Workspace, see [Run software reconciliation in the workspace](../task/run-recon-workspace.md).

