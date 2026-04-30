---
title: Integrating with GoTo
description: Integrating your Software Asset Management application with GoTo applications enable you to track your software subscriptions and reclaim unused licenses.Create an OAuth client for authenticating GoTo API requests.Create a connection between your GoTo applications and your ServiceNow instance.Create a GoTo integration profile to track software subscriptions and optimize licensing for your GoTo applications.
locale: en-US
release: xanadu
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2024-12-13"
reading_time_minutes: 8
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


## Create a GoTo connection

Create a connection between your GoTo applications and your ServiceNow instance.

### Before you begin

ServiceNow Role required: sam\_integrator or admin

### Procedure

1.  From your ServiceNow instance, navigate to **Process Automation** &gt; **Flow Designer**.

    The Flow Designer launches in a new tab.

2.  Select the **Connections** tab.

3.  Select **View Details** for your GoTo connection.

4.  From the list of available connections, locate GoTo and then select **Configure**.

5.  In the dialog box, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Connection Name|Name of the GoTo connection. This field populates automatically.|
    |Name|Name of your GoTo credentials. This field populates automatically.|
    |OAuth Client ID|Client ID that is assigned to your GoTo OAuth client.|
    |OAuth Client Secret|Client secret that is assigned to your GoTo OAuth client.|
    |OAuth Redirect URL|Redirect URL of the ServiceNow instance on which you’re integrating your GoTo applications. This field populates automatically.|

6.  Select **Configure and Get OAuth Token**.

    **Note:** For the role required to perform this step, refer to the [Minimal user permissions](integrate-with-goto.md#) table.

7.  In the Authorize App dialog box, select **Allow**.

    The OAuth access token becomes available for authorizing your GoTo connection.

8.  If GoToConnect license is enabled, navigate to the **Connections** tab.

9.  Find the connection for GoToConnect and select **View Details**.

10. Select **Get OAuth Token** to generate a token for GoToConnect.

    **Note:** For the role required to perform this step, refer to the [Minimal user permissions](integrate-with-goto.md#) table.


## Create a GoTo integration profile

Create a GoTo integration profile to track software subscriptions and optimize licensing for your GoTo applications.

### Before you begin

To create a GoTo integration profile, request the Software Asset Management - SaaS License Management plugin \(sn\_sam\_saas\_int\) from the [ServiceNow Store](https://store.servicenow.com/).

ServiceNow Role required: sam\_integrator or admin

### About this task

If you’re using Software Asset Workspace, the option to create the GoTo integration profile in Core UI is inactive.

### Procedure

1.  Navigate to the integration profile.

<table id="choicetable_o3p_z3k_qtb"><thead><tr><th align="left" id="d92896e967">

Interface

</th><th align="left" id="d92896e970">

Action

</th></tr></thead><tbody><tr><td id="d92896e976">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.
2.  Select **New**.
3.  Select **GoTo Integration Profile**.


</td></tr><tr><td id="d92896e1018">

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

Connection &amp; Credential

</td><td>

Connection and credential alias for the GoTo spoke. This field is automatically set to `sn_goto_spoke.GoTo`.

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
</table>3.  On the **Download Subscription Subflow** tab, verify that the **Subflow** field is set to **GoTo Download Subscriptions**.

    **Note:** This subflow is used for all supported GoTo applications.

4.  On the **Calculate Activity Subflow** tab, verify that the **Subflow** field is set to **GoTo Update User Activity**.

    This subflow is used for only the GoToMeeting and GoToWebinar applications.

    You can also select the date and time that you want to analyze user activity from in the Analyze user activity from field. By default, you can analyze user activity up to 60 days prior to the current date and view events performed by individual users from the time you create this profile.

    **Note:** Software Asset Management pulls the events from the time that you start analyzing user activity irrespective of the profile creation date.

    You can modify this value in the Last activity threshold field of your software reclamation rules. For more information, see [Review a software reclamation rule](../task/add-reclamation-rule-sub.md).

5.  On the **Reclaim Subscription Subflow** tab, verify that the **Subflow** field is set to **GoTo Reclaim Subscription**.

    **Note:** This subflow is used for only the GoToMeeting and GoToWebinar applications.

6.  Select **Save**.

    Your ServiceNow instance creates a draft integration profile. The integration profile uses the GoTo Download Subscriptions, GoTo Update User Activity, and GoTo Reclaim Subscription subflows to retrieve user data from your GoTo applications.

7.  After the form reloads, select **Publish**.

8.  In the Publish Confirmation dialog box, select **OK**.


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

