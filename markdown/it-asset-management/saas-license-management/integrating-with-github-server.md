---
title: Integrate with GitHub Enterprise Server
description: Integrating your Software Asset Management application with the GitHub Enterprise Server application help you track your software subscriptions and reclaim unused licenses.Generate a token that you can use to access the GitHub Enterprise Server API.Create a connection between your GitHub Enterprise Server applications and your ServiceNow instance.Create a GitHub Enterprise Server integration profile to track software subscriptions and optimize licensing for your GitHub Enterprise Server applications.
locale: en-US
release: xanadu
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Integrating with GitHub, Integrate with SaaS applications, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Integrate with GitHub Enterprise Server

Integrating your Software Asset Management application with the GitHub Enterprise Server application help you track your software subscriptions and reclaim unused licenses.

**Important:** Minimize security risks and protect information by granting access only to the necessary user or API permissions.

|Process|Required user role in the GitHub Enterprise Server application|Authentication scopes|
|-------|--------------------------------------------------------------|---------------------|
|Download subscriptions|site admininistrator|site\_admin|
|Reclaim subscription|site admininistrator|site\_admin|

## Generate an API access token for GitHub Enterprise Server

Generate a token that you can use to access the GitHub Enterprise Server API.

### Before you begin

GitHub Role required: site administrator

### About this task

The GitHub repository hosting service uses personal access tokens to grant users access to the GitHub API. Personal access tokens function similarly to OAuth access tokens by authorizing API requests. By generating a personal access token to authorize your GitHub Enterprise Server API requests, you can gain access to the GitHub Enterprise Server API.

### Procedure

1.  From a web browser, open your GitHub Enterprise Server instance.

2.  Sign in to your GitHub account.

3.  On the GitHub page header, select your profile photo and then select **Settings**.

    Your profile settings open.

4.  From the left navigation pane, select **Developer Settings**.

    Your developer settings open.

5.  From the left navigation pane, select **Personal access tokens**.

6.  On the Personal access tokens page, select **Generate new token**.

7.  If you’re prompted to confirm your password before proceeding, enter your GitHub password and then select **Confirm password**.

8.  On the New personal access token form, describe the purpose of the token in the **Note** field.

9.  In the Select scopes form section, enable the site\_admin OAuth scope by selecting the **site\_admin** check box.

    OAuth scopes limit the level of access that the application has to your protected resources. The site\_admin OAuth scope enables you to manage your enterprise users, organizations, and repositories.

10. Select **Generate token**.

    Your personal access token generates.

11. Copy the access token and save it in a secure location for later use.


## Create a GitHub Enterprise Server connection

Create a connection between your GitHub Enterprise Server applications and your ServiceNow instance.

### Before you begin

If you want to use a MID Server for communication between your ServiceNow instance and your GitHub Enterprise Server applications, you must first set up a MID Server on your instance. See [MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) for detailed instructions.

ServiceNow Role required: admin

### Procedure

1.  From your ServiceNow instance, navigate to **Process Automation** &gt; **Flow Designer**.

    The Flow Designer launches in a new tab.

2.  Select the **Connections** tab.

3.  Select **View Details** for your GitHub Server connection.

4.  From the list of available connections, locate GitHub Server and then select **Configure**.

5.  In the Configure Connection dialog box, fill in the fields.

<table id="table_skk_54h_wnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Name of the GitHub Server connection.

</td></tr><tr><td>

Connection URL

</td><td>

URL of your GitHub instance.

</td></tr><tr><td>

Use MID Server

</td><td>

Option that enables your ServiceNow instance to use a MID Server for communication with your GitHub Enterprise Server applications.-   If your instance requires a MID Server, set this field to `true`.
-   If your instance doesn’t require a MID Server, leave this field empty.
 **Important:** To enable this option, you must already have a MID Server set up on your instance. See [MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) for detailed instructions.

</td></tr><tr><td>

API Key

</td><td>

Personal access token that enables you to access the GitHub Enterprise Server API. Enter `<*api-key*>`, where &lt;*api-key*&gt; is the personal access token that you generated in [Generate an API access token for GitHub Enterprise Server](integrating-with-github-server.md#).

</td></tr></tbody>
</table>6.  Select **Configure Connection**.


## Create a GitHub Enterprise Server integration profile

Create a GitHub Enterprise Server integration profile to track software subscriptions and optimize licensing for your GitHub Enterprise Server applications.

### Before you begin

To create a GitHub Enterprise Server integration profile, request the Software Asset Management - SaaS License Management plugin \(sn\_sam\_saas\_int\) from the [ServiceNow Store](https://store.servicenow.com/).

ServiceNow Role required: sam\_integrator or admin

### About this task

If you’re using Software Asset Workspace, the option to create the GitHub Server integration profile in Core UI is inactive.

### Procedure

1.  Navigate to the integration profile.

<table id="choicetable_o3p_z3k_qtb"><thead><tr><th align="left" id="d202045e664">

Interface

</th><th align="left" id="d202045e667">

Action

</th></tr></thead><tbody><tr><td id="d202045e673">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.
2.  Select **New**.
3.  Select **GitHub Server Subscription Profile**.


</td></tr><tr><td id="d202045e715">

**Software Asset Workspace**

</td><td>

1.  Navigate to **License operations** &gt; **User Subscriptions** &gt; **Direct integration profiles**.
2.  Select **New**.
3.  Select **GitHub Server** from the drop-down list.
4.  Select **Continue**.


</td></tr></tbody>
</table>2.  On the form, fill in the fields.

<table id="table_wqc_y5h_wnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display Name

</td><td>

Name of the integration profile. For example, `GitHub Server Integration`.

</td></tr><tr><td>

Connection &amp; Credential

</td><td>

Connection and credential alias for the GitHub spoke. This field is automatically set to `sn_github_spoke.GitHub_Server`.

</td></tr><tr><td>

Status

</td><td>

Status of the integration profile.-   If you have not published the integration profile, this field is automatically set to **Draft**.
-   If you have already published the integration profile, this field is automatically set to **Published**.


</td></tr><tr><td>

Profile type

</td><td>

Type of integration profile. This field is automatically set to `github_server_subscription`.

</td></tr></tbody>
</table>3.  On the **Download Subscription Subflow** tab, verify that the **Subflow** field is set to **GitHub Server Download Subscriptions**.

    You can view events performed by individual users up to one year prior to the current date. For more information, see [Review a software reclamation rule](../task/add-reclamation-rule-sub.md).

    **Note:** Software Asset Management pulls the events from the time that you start downloading user subscriptions irrespective of the profile creation date.

4.  On the **Reclaim Subscription Subflow** tab, verify that the **Subflow** field is set to **GitHub Server Reclaim Subscription**.

5.  Select **Save**.

    Your ServiceNow instance creates a draft integration profile. The integration profile uses the GitHub Server Download Subscriptions and GitHub Server Reclaim Subscription subflows to retrieve data from your GitHub Enterprise Server applications.

6.  After the form reloads, select **Publish**.

7.  In the Publish Confirmation dialog box, select **OK**.


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

