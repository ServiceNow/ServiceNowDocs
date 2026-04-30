---
title: Integrating with GoTo
description: Integrating your Software Asset Management application with GoTo applications enable you to track your software subscriptions and reclaim unused licenses.Create an OAuth client for authenticating GoTo API requests.Create a GoTo integration profile to track software subscriptions and optimize licensing for your GoTo applications.
locale: en-US
release: yokohama
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 10
breadcrumb: [Integrate with SaaS applications, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Integrating with GoTo

Integrating your Software Asset Management application with GoTo applications enable you to track your software subscriptions and reclaim unused licenses.

With this integration, you can retrieve and analyze licensing information for the following GoTo applications:

-   GoToMeeting \(user subscriptions, user activity, and reclamation candidates\)
-   GoToWebinar \(user subscriptions, user activity, and reclamation candidates\)
-   GoToConnect \(user subscriptions, user activity, and reclamation candidates\)
-   GoToTraining \(user subscriptions only\)
-   GoToAssist \(user subscriptions only\)
-   OpenVoice \(user subscriptions only\)

Use this information to manage and optimize your GoTo license position.

**Important:** Minimize security risks and protect information by granting access only to the necessary user or API permissions.

<table id="table_box"><thead><tr><th>

Process

</th><th>

Required user role in the GoTo application

</th><th>

Authentication scopes

</th></tr></thead><tbody><tr><td>

Download subscriptions

</td><td>

LogMeIn developer account and admin role

</td><td>

-   Profile
-   Admin Center

</td></tr><tr><td>

Pull user activity

</td><td>

LogMeIn developer account and admin role

</td><td>

-   Profile
-   Admin Center
-   GoToConnect

</td></tr><tr><td>

Reclaim subscription

</td><td>

LogMeIn developer account and admin role

</td><td>

Admin Center

</td></tr></tbody>
</table>## Create a GoTo OAuth client

Create an OAuth client for authenticating GoTo API requests.

### Before you begin

GoTo Role required: Refer to the [Minimal user permissions](integrate-with-goto.md#) table.

### Procedure

1.  From a web browser, open the [GoTo Developer Center](https://developer.goto.com/).

2.  Sign in using your LogMeIn developer account.

    If you have not already set up a LogMeIn developer account, see [How to login or create a developer account](https://developer.goto.com/guides/Get%20Started/01_HOW_developerAccount/) for detailed instructions.

3.  From the LogMeIn Developers home page, select the **OAuth Clients** tab.

4.  Select **Create a client**.

5.  On the Details tab of the Create client form, fill in the client details.

    |Field|Description|
    |-----|-----------|
    |Client name|Name of the OAuth client.|
    |Description|Optional description for the OAuth client.|
    |Redirect URLs|Redirect URL of the ServiceNow instance on which you’re integrating your GoTo applications. Enter `https://<*instance-url*>/oauth_redirect.do`, where &lt;*instance-url*&gt; is the URL of your ServiceNow instance.|

6.  Select **Next**.

7.  On the Scopes tab, specify the level of access that the OAuth client has to your GoTo users and applications.

<table id="table_zcp_yvn_tnb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Profile

</td><td>

OAuth scopes for getting and modifying user information for your authenticated users. The **Get user information** scope is enabled automatically. Select the check box to enable the **Modify user details** scope.

</td></tr><tr><td>

GoToMeeting, GoToWebinar, or GoToTraining

</td><td>

OAuth scope for creating, starting, and modifying sessions for your GoToMeeting, GoToWebinar, and GoToTraining applications. Select the check box to enable this scope.

 **Note:** The SaaS License Management GoTo integration doesn’t support license management for the GoToTraining application.

</td></tr><tr><td>

GoToAssist Remote Support or Service Desk

</td><td>

OAuth scope for creating, starting, and modifying sessions for the GoToAssist Remote Support and Service Desk applications. Leave this check box unselected.**Note:** The SaaS License Management GoTo integration doesn’t support license management for the GoToAssist applications.

</td></tr><tr><td>

SCIM

</td><td>

OAuth scope for automating user management using the System for Cross-domain Identity Management \(SCIM\) protocol. Leave this check box unselected.

</td></tr><tr><td>

Admin Center

</td><td>

OAuth scope for managing LogMeIn users through the GoTo Admin Center. Select the check box to enable this scope.

</td></tr><tr><td>

GoToConnect

</td><td>

OAuth scope for initiating phone calls and other telephone services using the GoToConnect. If GoToConnect license is enabled, select these check boxes:-   Access call history for phone lines in the PBX \[cr.v1.read\]
-   Retrieve your phone line information \[users.v1.lines.read\]


</td></tr></tbody>
</table>8.  Select **Save**.

9.  On the Credentials tab, copy the values in the **Client ID** and **Client secret** fields.

    Save them in a secure location for later use.

10. Select the check box to verify that you have stored the client secret.

11. Select **Done**.


## Create a GoTo integration profile

Create a GoTo integration profile to track software subscriptions and optimize licensing for your GoTo applications.

### Before you begin

To create a GoTo integration profile, request the Software Asset Management - SaaS License Management plugin \(sn\_sam\_saas\_int\) from the [ServiceNow Store](https://store.servicenow.com/).

ServiceNow Role required: sam\_integrator or admin

**Important:** You must select the **GoTo Spoke** check box for this integration while installing optional features on the [Application Manager](https://www.servicenow.com/docs/access?context=application-manager&version=yokohama&pubname=yokohama-platform-administration&ft:locale=en-US) page. For more information about choosing the required SaaS applications, see [Request SaaS License Management](../task/request-saas-license-management.md).

### About this task

If you’re using Software Asset Workspace, the option to create the GoTo integration profile in Core UI is inactive.

### Procedure

1.  Navigate to the integration profile.

<table id="choicetable_o3p_z3k_qtb"><thead><tr><th align="left" id="d104633e687">

Interface

</th><th align="left" id="d104633e690">

Action

</th></tr></thead><tbody><tr><td id="d104633e696">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.
2.  Select **New**.
3.  Select **GoTo Integration Profile**.


</td></tr><tr><td id="d104633e738">

**Software Asset Workspace**

</td><td>

1.  Navigate to **License operations** &gt; **User Subscriptions** &gt; **Direct integration profiles**.
2.  Select **New**.
3.  Select **GoTo** from the drop-down list.
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

Name of the integration profile. For example, `GoTo Integration`.

</td></tr><tr><td>

Status

</td><td>

Status of the integration profile.-   If you have not published the integration profile, this field is automatically set to **Draft**.
-   If you have already published the integration profile, this field is automatically set to **Published**.


</td></tr><tr><td>

Profile Type

</td><td>

Type of integration profile. This field is automatically set to `GoTo Subscription`.

</td></tr></tbody>
</table>3.  Review the required user roles or API permissions specified in the **Vendor configuration** field for each process to minimize security risks and optimize SaaS licenses.

    **Note:** For more information, see [Minimal user permissions](integrate-with-goto.md#) table.

    1.  In the Download Subscription Subflow section, verify that the **Subflow** field is set to **GoTo Download Subscriptions**.

        This subflow is used for all supported GoTo applications.

        **Note:** The **Download subscriptions** check box is selected by default and you can't clear it.

    2.  In the Calculate Activity Subflow section, verify that the **Subflow** field is set to **GoTo Update User Activity**.

        This subflow is used for only the GoToMeeting and GoToWebinar applications.

        **Note:** The **Download Activity** check box is selected by default. If you clear it, the activity scheduled job **SAM - Refresh &lt;displayname&gt; Activity** isn't created.

        In the **Analyze user activity** field, you can also select the date and time starting from when you want to analyze the user activity. By default, you can analyze user activity up to 60 days prior to the current date and view events performed by individual users from the time you create this profile.

        **Note:** Software Asset Management pulls the events from the time that you start analyzing user activity irrespective of the profile creation date.

        You can modify this value in the Last activity threshold field of your software reclamation rules. For more information, see [Review a software reclamation rule](../task/add-reclamation-rule-sub.md).

    3.  In the Reclaim Subscription Subflow section, verify that the **Subflow** field is set to **GoTo Reclaim Subscription**.

        This subflow is used for only the GoToMeeting and GoToWebinar applications.

        **Note:** The **Reclaim subscriptions** check box is selected by default. If you don't want to reclaim subscriptions, you can clear this check box. If you clear it, the removal candidates are created but the reclaim subscription subflow isn't triggered or the reclamation process isn't initiated.

4.  Select **Save**.

    Your ServiceNow instance creates a draft integration profile.

    The **Connection &amp; Credential** field appears and is automatically set to **sn\_goto\_spoke.GoTo**.

5.  Open the connection &amp; credential aliases record by selecting the preview icon \(![Preview icon.](../image/preview-icon.png)\) next to the **Connection &amp; Credential** field and then selecting **Open Record** in the record preview.

6.  On the Connection &amp; Credential Aliases form, select the **Create New Connection &amp; Credential** related link.

7.  In the Create Connection and Credential dialog box, fill in the fields.

<table id="table_ujr_ps1_wmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the connection.

</td></tr><tr><td>

OAuth Client ID

</td><td>

Client ID that is assigned to your GoTo application.

</td></tr><tr><td>

OAuth Client Secret

</td><td>

Client secret that is assigned to your GoTo application.

</td></tr><tr><td>

OAuth Redirect URL

</td><td>

URL of the OAuth provider that users are redirected to after authentication.This field populates automatically based on the OAuth redirect URL that you specified in [Create a GoTo OAuth client](integrate-with-goto.md#).

</td></tr></tbody>
</table>8.  Select **Create and Get OAuth Token**.

    **Note:** For the role required to perform this step, refer to the [Minimal user permissions](integrate-with-goto.md#) table.

9.  In the Authorize App dialog box, select **Allow**.

10. Select **Allow**.

    The OAuth access token becomes available for authorizing your GoTo connection.

11. If GoToConnect license is enabled, navigate to the Connections tab.

12. Find the connection for GoToConnect and select **View Details**.

13. Select **Get OAuth Token** to generate a token for GoToConnect.

14. On the integration profile form, select **Validate Connection** to verify the connection and credential details of this integration.

    Validating the connection verifies the Download Subscriptions and Calculate Activity APIs, but not the Reclaim Subscriptions APIs.

15. After the connection is verified, select **Publish**.

16. In the Publish Confirmation dialog box, select **OK**.

    **Note:** If you clear the **Download Activity** check box after the integration profile is published, you must revalidate the connections and then republish the integration profile because the following events occur:

    -   The **Status** field on the integration profile form changes to **Draft**.
    -   The **Validate connection** button shows up on the form.
    -   The current **SAM - Refresh &lt;displayname&gt; Activity** job gets deleted.

### What to do next

After the integration connects, your ServiceNow instance automatically creates software models, reclamation rules, and software subscriptions that are refreshed daily.

If you want to set up multiple integration profiles with unique connections, create child aliases to manage different configurations and settings for each integration profile. For more information, see [Create a child alias to set up multiple integration profiles](../reuse/create-child-alias-saas.md).

Review all automatically generated reclamation rules to reclaim user subscriptions. For more information, see [Review a software reclamation rule](../task/add-reclamation-rule-sub.md).

Create software entitlements for the automatically generated software models to track used software against owned software.

-   For more information on creating software entitlements in the Software Asset Management Core UI, see [Create entitlements in Software Asset Management classic](../task/track-software-rights.md).
-   For more information on creating software entitlements in the Software Asset Workspace, see [Create entitlements in workspace](../task/create-entitlements-workspace.md).
-   For more information on creating software entitlements using the Software Asset Management Playbook, see [Create entitlements using the guided walk-through](../task/guidedwalk-workspace.md).

Reconciliation also runs on your subscriptions as a scheduled job or on-demand. You can view your reconciliation results in the [License Workbench](sam-license-workbench.md) \(Software Asset Management classic application\) or the [License usage view](sam-workspace-workbench.md) \(Software Asset Workspace\). Use these results to determine your license compliance position and to remediate any non-compliance.

-   For more information on running reconciliation in the Software Asset Management classic application, see [Run software reconciliation in Software Asset Management classic](../task/t_RunReconciliation.md).
-   For more information on running reconciliation in the Software Asset Workspace, see [Run software reconciliation in the workspace](../task/run-recon-workspace.md).

