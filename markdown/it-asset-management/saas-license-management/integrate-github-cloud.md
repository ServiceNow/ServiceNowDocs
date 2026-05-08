---
title: Integrate with GitHub Enterprise Cloud
description: Integrating your Software Asset Management application with the GitHub Enterprise Cloud application help you track your software subscriptions and reclaim unused licenses.Generate a token that you can use to access the GitHub Enterprise Cloud API.Create a GitHub Enterprise Enterprise Cloud integration profile to track software subscriptions and optimize licensing for your GitHub Enterprise Cloud applications.
locale: en-US
release: australia
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 10
breadcrumb: [Integrating with GitHub, Integrate with SaaS applications, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Integrate with GitHub Enterprise Cloud

Integrating your Software Asset Management application with the GitHub Enterprise Cloud application help you track your software subscriptions and reclaim unused licenses.

**Important:** Minimize security risks and protect information by granting access only to the necessary user or API permissions.

<table id="table_box"><thead><tr><th>

Process

</th><th>

Required user role in the GitHub Enterprise Cloud application

</th><th>

Authentication scopes

</th></tr></thead><tbody><tr><td>

Download subscriptions

</td><td>

Organization owner

</td><td>

read:org

</td></tr><tr><td>

Pull user activity

</td><td>

Organization owner

</td><td>

-   read:org
-   repo
-   read:audit\_log

</td></tr><tr><td>

Reclaim subscription

</td><td>

Organization owner

</td><td>

write:org

</td></tr></tbody>
</table>The GitHub Enterprise Cloud integration is currently limited to users with Enterprise plans only.

## Generate an API access token for GitHub Enterprise Cloud

Generate a token that you can use to access the GitHub Enterprise Cloud API.

### Before you begin

GitHub Role required: organization owner

The user account that you use for authentication should be able to read all repositories in the organization they’re a part of.

### About this task

The GitHub repository hosting service uses personal access tokens to grant users access to the GitHub API. Personal access tokens function similarly to OAuth access tokens by authorizing API requests. By generating a personal access token to authorize your GitHub Enterprise Cloud API requests, you can gain access to the GitHub Enterprise Cloud API.

### Procedure

1.  From a web browser, open [GitHub](https://github.com/).

2.  Sign in to your GitHub account.

3.  On the GitHub page header, select your profile photo and then select **Settings**.

    Your profile settings open.

4.  From the side navigation pane, select **Developer Settings**.

    Your developer settings open.

5.  From the side navigation pane, select **Personal access tokens**.

6.  Select **Tokens \(classic\)**.

7.  On the Personal access tokens page, select **Generate new token**.

8.  Select **Generate new token \(classic\)**.

9.  If you’re prompted to confirm your password before proceeding, enter your GitHub password and then select **Confirm password**.

10. On the New personal access token form, describe the purpose of the token in the **Note** field.

11. To give your token an expiration, select the **Expiration** drop-down menu and select a default value or use the calendar picker.

12. In the Select scopes form section, enable the repo, write:org, read:org, and read:audit\_log OAuth scopes.

    OAuth scopes limit the level of access that the application has to your protected resources. The repo OAuth scope gives you full control of your private repositories. The write:org and read:org OAuth scopes enable you to manage your entire organization, including all teams, projects, and memberships. The read:audit\_log OAuth scope gives you access to the audit log data to track accurate user activity. See [Scopes for OAuth Apps](https://docs.github.com/en/free-pro-team@latest/developers/apps/scopes-for-oauth-apps) for more information about GitHub OAuth scopes.

    1.  Enable the repo OAuth scope by selecting the **repo** check box.

        By enabling this OAuth scope, you automatically enable the repo:status, repo\_deployment, public\_repo, repo:invite, and security\_events OAuth scopes.

    2.  Enable the write:org and read:org OAuth scope.

    3.  Enable the read:audit\_log OAuth scope.

13. Select **Generate token**.

    Your personal access token generates.

14. Copy the access token and save it in a secure location for later use.

15. To use your token to access resources owned by an organization that uses SAML single sign-on, authorize the token.

    For more information, see [Authorizing a personal access token for use with SAML single sign-on](https://docs.github.com/en/enterprise-cloud@latest/authentication/authenticating-with-saml-single-sign-on/authorizing-a-personal-access-token-for-use-with-saml-single-sign-on).


## Create a GitHub Enterprise Cloud integration profile

Create a GitHub Enterprise Enterprise Cloud integration profile to track software subscriptions and optimize licensing for your GitHub Enterprise Cloud applications.

### Before you begin

To create a GitHub Enterprise Cloud integration profile, request the Software Asset Management - SaaS License Management plugin \(sn\_sam\_saas\_int\) from the [ServiceNow Store](https://store.servicenow.com/).

ServiceNow Role required: sam\_integrator

**Important:** You must select the **GitHub Spoke** check box for this integration while installing optional features on the [Application Manager](https://www.servicenow.com/docs/access?context=application-manager&version=australia&pubname=australia-platform-administration&ft:locale=en-US) page. For more information about choosing the required SaaS applications, see [Request SaaS License Management](../task/request-saas-license-management.md).

If you're upgrading from Yokohama or Zurich release, then you must reconfigure your GitHub Enterprise Cloud integration profile.

### About this task

If you’re using Software Asset Workspace, the option to create the GitHub Cloud integration profile in Core UI is inactive.

### Procedure

1.  Navigate to the integration profile.

<table id="choicetable_o3p_z3k_qtb"><thead><tr><th align="left" id="d44130e526">

Interface

</th><th align="left" id="d44130e529">

Action

</th></tr></thead><tbody><tr><td id="d44130e535">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.
2.  Select **New**.
3.  Select **GitHub Cloud Integration Profile**.


</td></tr><tr><td id="d44130e577">

**Software Asset Workspace**

</td><td>

1.  Navigate to **License operations** &gt; **User Subscriptions** &gt; **Direct integration profiles**.
2.  Select **New**.
3.  Select **GitHub Cloud** from the drop-down list.
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

Name of the integration profile. For example, `GitHub Cloud Integration`.

</td></tr><tr><td>

Status

</td><td>

Status of the integration profile.-   If you have not published the integration profile, this field is automatically set to **Draft**.
-   If you have already published the integration profile, this field is automatically set to **Published**.


</td></tr><tr><td>

Profile type

</td><td>

Type of integration profile. This field is automatically set to **github\_cloud\_subscription**.

</td></tr></tbody>
</table>3.  Review the required user roles or API permissions specified in the **Vendor configuration** field for each process to minimize security risks and optimize SaaS licenses.

    **Note:** For more information, see [Minimal user permissions](integrate-github-cloud.md#) table.

    1.  In the Download Subscription Subflow section, verify that the **Subflow** field is set to **GitHub Cloud Download Subscriptions**.

        **Note:** The **Download subscriptions** check box is selected by default and you can't clear it.

        Software Asset Management pulls the members, outside collaborators, pending invitations, and pending outside collaborators to provide a complete view of your GitHub Enterprise Cloud Subscriptions.

        **Important:** To pull pending outside collaborators, enable the **sn\_sam\_saas\_int.pull\_pending\_collaborator\_github** system property. A higher number of repositories would lead to an increased number of API transactions.

    2.  In the Calculate Activity Subflow section, verify that the **Subflow** field is set to **GitHub Cloud Update User Activity**.

        **Note:** The **Download Activity** check box is selected by default. If you clear it, the activity scheduled job **SAM - Refresh &lt;displayname&gt; Activity** isn't created.

        In the **Analyze user activity** field, you can also select the date and time starting from when you want to analyze the user activity. By default, you can analyze user activity up to 60 days prior to the current date and view events performed by individual users from the time you create this profile.

        **Note:** Software Asset Management pulls the events from the time that you start analyzing user activity irrespective of the profile creation date.

        You can modify this value in the Last activity threshold field of your software reclamation rules. For more information, see [Review a software reclamation rule](../task/add-reclamation-rule-sub.md).

        **Tip:** To avoid performance issues with this subflow, the best approach is to set the **Analyze user activity from** field to a maximum of seven days before the current date.

    3.  In the Reclaim Subscription Subflow section, verify that the **Subflow** field is set to **GitHub Cloud Reclaim Subscription**.

        **Note:** The **Reclaim subscriptions** check box is selected by default. If you don't want to reclaim subscriptions, you can clear this check box. If you clear it, the removal candidates are created but the reclaim subscription subflow isn't triggered or the reclamation process isn't initiated.

4.  Select **Save**.

    Your ServiceNow instance creates a draft integration profile.

    The **Connection &amp; Credential** field appears and is automatically set to **sn\_github\_spoke.GitHub**.

5.  Open the connection &amp; credential aliases record by selecting the preview icon ![](../image/preview-icon.png) next to the **Connection &amp; Credential** field and then selecting **Open Record** in the record preview.

6.  On the Connection &amp; Credential Aliases form, select the **Create New Connection &amp; Credential** related link.

7.  In the Create Connection and Credential dialog box, fill in the fields.

<table id="table_skk_54h_wnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Connection Name

</td><td>

Name of the GitHub connection.

</td></tr><tr><td>

Connection URL

</td><td>

URL of the GitHub API endpoint. Enter `https://api.github.com`.

</td></tr><tr><td>

Use MID Server

</td><td>

Option that enables your ServiceNow instance to use a MID Server for communication with your GitHub Enterprise Cloud applications.-   If your instance requires a MID Server, set this field to `true`.
-   If your instance doesn’t require a MID Server, leave this field empty.
**Important:** To enable this option, you must already have a MID Server set up on your instance. See [MID Server](https://www.servicenow.com/docs/access?context=mid-server-landing&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US) for detailed instructions.

</td></tr><tr><td>

API Key

</td><td>

Personal access token that enables you to access the GitHub Enterprise Cloud API. -   If the GitHub spoke version installed is 2.2.5 or higher, enter `<api-key>`.
-   If the GitHub spoke version installed is lower than 2.2.5, enter `Bearer <api-key>`.
The &lt;*api-key*&gt; is the personal access token that you generated in [Generate an API access token for GitHub Enterprise Cloud](integrate-github-cloud.md#)

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

