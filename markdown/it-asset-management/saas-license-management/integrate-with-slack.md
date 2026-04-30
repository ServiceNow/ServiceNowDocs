---
title: Integrating with Slack
description: Integrating your Software Asset Management application with the Slack application enables you to track your software subscriptions and reclaim unused licenses.Create a Slack Enterprise Grid application to manage and connect multiple workspaces across your organization.Create a Slack application on each workspace that you want to track user activity on.Create a connection between the Slack Enterprise Grid application and your ServiceNow instance. This connection enables your instance to retrieve user data from your application.Create a connection between your Slack workspaces and your ServiceNow instance. This connection enables your instance to retrieve user data from your workspaces.Create a Slack integration profile to track software subscriptions and optimize licensing for your Slack applications.
locale: en-US
release: xanadu
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 13
keywords: [slack, integration profile, saas]
breadcrumb: [Integrate with SaaS applications, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Integrating with Slack

Integrating your Software Asset Management application with the Slack application enables you to track your software subscriptions and reclaim unused licenses.

The ServiceNow Slack integration supports the Slack Enterprise Grid plan. This plan enables you to connect multiple workspaces across your organization.

**Important:** Minimize security risks and protect information by granting access only to the necessary user or API permissions.

|Process|Required user role in the Slack application|Authentication scopes|
|-------|-------------------------------------------|---------------------|
|Download subscriptions|Org Owner|admin|
|Pull user activity|Org Owner|admin|
|Reclaim subscription|Org Owner|admin|

## Create a Slack Enterprise Grid application

Create a Slack Enterprise Grid application to manage and connect multiple workspaces across your organization.

### Before you begin

Role required: Refer to the [Minimal user permissions](integrate-with-slack.md#) table.

### Procedure

1.  From a web browser, open [Slack](https://slack.com/).

2.  Sign in using your Slack credentials.

3.  Go to the [Slack platform](https://api.slack.com/).

4.  On the page header of the Slack platform, select **Your Apps**.

5.  On the Your Apps page, select **Create New App**.

6.  Select **From Scratch**.

    The Name app and choose workspace dialog box opens.

7.  In the dialog box, enter an application name in the **App Name** field.

8.  From the Development Slack Workspace list, select the workspace that you want the application to belong to.

9.  Select **Create App**.

    The Slack platform creates the application and then redirects you to the Basic Information page. Use this page to view and configure application settings.

10. On the Basic Information page, expand the App Credentials section and then copy the values in the **Client ID** and **Client Secret** fields.

    Save them in a secure location for later use.

11. Expand the Add features and functionality section and then select **Permissions**.

12. On the OAuth &amp; Permissions page, configure the permissions that enable the interactions between the application and the Slack API.

    1.  In the Redirect URLs section, add the URL of the OAuth provider that you want to redirect users to after authentication.

        1.  Select **Add New Redirect URL**.
        2.  When prompted, enter `https://<*instance-name*>/oauth_redirect.do`, where &lt;*instance-name*&gt; is the name of your ServiceNow instance.
        3.  Select **Add**.
        4.  Select **Save URLs**.
    2.  In the User Token Scopes section, add the admin OAuth scope to the application.

        The OAuth scopes limit the level of access that the application has to your users, channels, and workspaces. For more information on Slack OAuth scopes, see [OAuth Permission scopes](https://api.slack.com/legacy/oauth-scopes).

        1.  Select **Add an OAuth Scope**.
        2.  When prompted, select **admin** from the OAuth Scope list.

            This OAuth scope enables the application to administer your workspace.

            **Note:** The **Description** field for the OAuth scope populates automatically.

13. Activate your application.

    1.  From the left navigation pane, navigate to **Settings** &gt; **Manage Distribution**.

    2.  Under Share Your App with Other Workspaces, expand the Remove Hard Coded Information section.

    3.  Verify that your application doesn’t contain any hard-coded information, such as OAuth tokens.

    4.  After verification, select the **I've reviewed and removed any hard-coded information** check box.

    5.  Verify that you have completed all other sections.

    6.  Select **Activate Public Distribution**.


## Create a Slack workspace application

Create a Slack application on each workspace that you want to track user activity on.

### Before you begin

Role required: Refer to the [Minimal user permissions](integrate-with-slack.md#) table.

### Procedure

1.  From a web browser, open [Slack](https://slack.com/).

2.  Sign in using your Slack credentials.

3.  Go to the [Slack platform](https://api.slack.com/).

4.  On the page header of the Slack platform, select **Your Apps**.

5.  On the Your Apps page, select **Create New App**.

6.  Select **From Scratch**.

    The Name app and choose workspace dialog box opens.

7.  In the dialog box, enter an application name in the **App Name** field.

8.  From the Development Slack Workspace list, select the workspace that you want the application to belong to.

9.  Select **Create App**.

    The Slack platform creates the application and then redirects you to the Basic Information page. Use this page to view and configure application settings.

10. On the Basic Information page, expand the App Credentials section and then copy the values in the **Client ID** and **Client Secret** fields.

    Save them in a secure location for later use.

11. Expand the Add features and functionality section and then select **Permissions**.

12. On the OAuth &amp; Permissions page, configure the permissions that enable interactions between the application and the Slack API.

    1.  In the Redirect URLs section, add the URL of the OAuth provider that you want to redirect users to after authentication.

        1.  Select **Add New Redirect URL**.
        2.  When prompted, enter `https://<*instance-name*>/oauth_redirect.do`, where &lt;*instance-name*&gt; is the name of your ServiceNow instance.
        3.  Select **Add**.
        4.  Select **Save URLs**.
    2.  In the User Token Scopes section, add the admin OAuth scope to the application.

        The OAuth scopes limit the level of access that the application has to your users, channels, and workspaces. For more information on Slack OAuth scopes, see [OAuth Permission scopes](https://api.slack.com/legacy/oauth-scopes).

        1.  Select **Add an OAuth Scope**.
        2.  When prompted, select **admin** from the OAuth Scope list.

            This OAuth scope enables the application to administer your workspace.

            **Note:** The **Description** field for the OAuth scope populates automatically.

13. In the OAuth Tokens &amp; Redirect URLs section of the OAuth &amp; Permissions page, select **Install App to Workspace**.

14. Select **Allow**.

    Slack creates the application for the specified workspace.

15. Repeat steps 4 through 13 for each workspace on which you want to create an application.


## Create a Slack Enterprise connection

Create a connection between the Slack Enterprise Grid application and your ServiceNow instance. This connection enables your instance to retrieve user data from your application.

### Before you begin

Role required: sam\_integrator or admin

### Procedure

1.  From your ServiceNow instance, navigate to **Process Automation** &gt; **Flow Designer**.

    The Workflow Studio launches in a new tab.

2.  Select the **Connections** tab.

3.  Select **View Details** for your Slack Enterprise connection.

4.  From the list of available connections, locate Slack Enterprise and then select **Configure**.

5.  In the Configure Connection dialog box, fill in or verify the following fields.

    |Field|Value|
    |-----|-----|
    |Connection Name|Name of the Slack Enterprise connection. This field populates automatically.|
    |Name|Name of your Slack Enterprise credentials. This field populates automatically.|
    |OAuth Client ID|Client ID that is assigned to your Slack Enterprise Grid application. Enter the same client ID that you copied in [Create a Slack Enterprise Grid application](integrate-with-slack.md#).|
    |OAuth Client Secret|Client secret that is assigned to your Slack Enterprise Grid application. Enter the same client secret that you copied in [Create a Slack Enterprise Grid application](integrate-with-slack.md#).|
    |OAuth Redirect URL|Redirect URL for your Slack Enterprise Grid application. This field populates automatically.|

6.  Select **Configure and Get OAuth Token**.

    **Note:** For the role required to perform this step, refer to the [Minimal user permissions](integrate-with-slack.md#) table.

7.  On the Authorize App dialog box, verify if the Enterprise Grid workspace is available on the top-right list.

8.  If the Enterprise Grid workspace is available, select the Enterprise Grid workspace.

9.  If the Enterprise Grid workspace isn’t available,

    1.  Select **Add another workspace**.

    2.  Enter the Enterprise Grid workspace URL.

    3.  Select **Continue**.

        You get redirected to the Authorize App dialog box.

    4.  Select **Allow**.

        The OAuth access token becomes available for authorizing your Enterprise connection.


## Create a Slack workspace connection

Create a connection between your Slack workspaces and your ServiceNow instance. This connection enables your instance to retrieve user data from your workspaces.

### Before you begin

Role required: sam\_integrator or admin

### About this task

Create a separate connection for each of your Slack workspaces.

### Procedure

1.  From your ServiceNow instance, navigate to **Process Automation** &gt; **Flow Designer**.

    The Workflow Studio launches in a new tab.

2.  Select the **Connections** tab.

3.  Select **Add Connection** for your Slack Enterprise connection.

4.  In the Create Connection dialog box, fill in or verify the following fields.

    |Field|Value|
    |-----|-----|
    |Connection Name|Name of the Slack workspace connection. For example, `Slack-Workspace-1`.|
    |Name|Name of your Slack workspace credentials. For example, `Slack-Workspace-1`.|
    |OAuth Client ID|Client ID that is assigned to your Slack workspace application. Enter the same client ID that you copied in [Create a Slack workspace application](integrate-with-slack.md#).|
    |OAuth Client Secret|Client secret that you assigned to your Slack workspace application. Enter the same client secret that you copied in [Create a Slack workspace application](integrate-with-slack.md#).|
    |OAuth Redirect URL|Redirect URL for your Slack workspace application. This field populates automatically.|

5.  Select **Create and Get OAuth Token**.

    **Note:** For the role required to perform this step, refer to the [Minimal user permissions](integrate-with-slack.md#) table.

6.  In the Authorize App dialog box, select **Allow**.

    The OAuth access token becomes available for authorizing your Slack workspace connection.

7.  Repeat steps 3 through 6 for each workspace that which you want to connect.

8.  Return to your ServiceNow instance to associate your Slack workspace connections with the instance.

    1.  Navigate to **Slack** &gt; **Slack Workspace Tokens**.

    2.  Select **New**.

    3.  On the Slack Workspace Tokens form, fill in the following fields.

        |Field|Value|
        |-----|-----|
        |Connection Alias|Name of your Slack workspace connection. Enter the same connection name that you entered in [step 4](integrate-with-slack.md#create-workspace-connection).|
        |Workspace Name|The name of the workspace to which your Slack application belongs.|
        |Slack App|Name of your Slack workspace application. Enter the same application name that you entered in [Create a Slack workspace application](integrate-with-slack.md#).|

    4.  Select **Submit**.

    5.  Repeat steps a through d for each workspace connection that you want to associate with your instance.


## Create a Slack integration profile

Create a Slack integration profile to track software subscriptions and optimize licensing for your Slack applications.

### Before you begin

To create a Slack integration profile, request the Software Asset Management - SaaS License Management plugin \(sn\_sam\_saas\_int\) from the [ServiceNow Store](https://store.servicenow.com/).

ServiceNow Role required: sam\_integrator or admin

### About this task

If you’re using Software Asset Workspace, the option to create the Slack integration profile in Core UI is inactive.

### Procedure

1.  Navigate to the integration profile.

<table id="choicetable_o3p_z3k_qtb"><thead><tr><th align="left" id="d195371e1628">

Interface

</th><th align="left" id="d195371e1631">

Action

</th></tr></thead><tbody><tr><td id="d195371e1637">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.
2.  Select **New**.
3.  Select **Slack Enterprise Integration Profile**.


</td></tr><tr><td id="d195371e1679">

**Software Asset Workspace**

</td><td>

1.  Navigate to **License operations** &gt; **User Subscriptions** &gt; **Direct integration profiles**.
2.  Select **New**.
3.  Select **Slack Enterprise** from the drop-down list.
4.  Select **Continue**.


</td></tr></tbody>
</table>2.  On the form, fill in the fields.

<table id="table_bv2_1gv_1nb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Display Name

</td><td>

Name of the integration profile. For example, `Slack Integration`.

</td></tr><tr><td>

Connection &amp; Credential

</td><td>

Connection and credential alias for Slack. This field populates automatically.

</td></tr><tr><td>

Status

</td><td>

Status of the integration profile.-   If you have not published the integration profile, this field is automatically set to `Draft`.
-   If you have already published the integration profile, this field is automatically set to `Published`.


</td></tr><tr><td>

Profile Type

</td><td>

Type of integration profile. This field is automatically set to `Slack Enterprise Subscription`.

</td></tr></tbody>
</table>3.  On the **Download Subscription Subflow** tab, verify that the **Subflow** field is set to `Slack Download Subscriptions Subflow`.

4.  On the **Calculate Activity Subflow** tab, verify that the **Subflow** field is set to `Slack Update User Activity Subflow`.

    You can also select the date and time that you want to analyze user activity from in the Analyze user activity from field. By default, you can analyze user activity up to 60 days prior to the current date and view events performed by individual users from the time you create this profile.

    **Note:** Software Asset Management pulls the events from the time that you start analyzing user activity irrespective of the profile creation date.

    You can modify this value in the Last activity threshold field of your software reclamation rules. For more information, see [Review a software reclamation rule](../task/add-reclamation-rule-sub.md).

5.  On the **Reclaim Subscription Subflow** tab, verify that the **Subflow** field is set to `Slack Reclaim Subscription Subflow`.

6.  Select **Save**.

    Your ServiceNow instance creates a draft integration profile. The integration profile uses the Slack Download Subscriptions, Slack Update User Activity, and Slack Reclaim Subscription subflows to retrieve user data from the Slack application.

    The **Connection &amp; Credential** field appears and is automatically set to **sn\_slack\_ah\_v2.Slack\_Enterprise**.

7.  After the form reloads, select **Publish**.

    The Publish Confirmation dialog box opens.

8.  In the dialog box, select **OK**.

    **Note:** To optimize memory and avoid performance issues in your Slack flow, you can turn off the flow engine reporting level by navigating to **System Properties** &gt; **All Properties** and selecting the **com.snc.process\_flow.reporting.level** system property. On the System Property page, set the **Value** to `OFF` and then select **Update**.


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

