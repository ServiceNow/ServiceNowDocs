---
title: Integrating with Slack
description: Integrating your Software Asset Management application with the Slack application enables you to track your software subscriptions and reclaim unused licenses.Create a Slack Enterprise Grid application to manage and connect multiple workspaces across your organization.Create a Slack application on each workspace that you want to track user activity on.Create a Slack integration profile to track software subscriptions and optimize licensing for your Slack applications.
locale: en-US
release: australia
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 14
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

7.  In the Name app and choose workspace dialog box that opens, enter an application name in the **App Name** field.

8.  From the **Pick a workspace to develop your app in:** list, select the workspace that you want the application to belong to.

9.  Select **Create App**.

    The Slack platform creates the application and then redirects you to the Basic Information page. Use this page to view and configure application settings.

10. On the Basic Information page, copy the values in the **Client ID** and **Client Secret** fields and save them for later use.

11. Expand the Features section and then select **OAuth &amp; Permissions**.

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

7.  In the Name app and choose workspace dialog box that opens, enter an application name in the **App Name** field.

8.  From the **Pick a workspace to develop your app in:** list, select the workspace that you want the application to belong to.

9.  Select **Create App**.

    The Slack platform creates the application and then redirects you to the Basic Information page. Use this page to view and configure application settings.

10. On the Basic Information page, copy the values in the **Client ID** and **Client Secret** fields and save them for later use.

11. Expand the Features section and then select **OAuth &amp; Permissions**.

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


## Create a Slack integration profile

Create a Slack integration profile to track software subscriptions and optimize licensing for your Slack applications.

### Before you begin

To create a Slack integration profile, request the Software Asset Management - SaaS License Management plugin \(sn\_sam\_saas\_int\) from the [ServiceNow Store](https://store.servicenow.com/).

ServiceNow Role required: sam\_integrator

**Important:** You must select the **Slack Spoke** check box for this integration while installing optional features on the [Application Manager](https://www.servicenow.com/docs/access?context=application-manager&version=australia&pubname=australia-platform-administration&ft:locale=en-US) page. For more information about choosing the required SaaS applications, see [Request SaaS License Management](../task/request-saas-license-management.md).

### About this task

If you’re using Software Asset Workspace, the option to create the Slack integration profile in Core UI is inactive.

### Procedure

1.  Navigate to the integration profile.

<table id="choicetable_o3p_z3k_qtb"><thead><tr><th align="left" id="d228500e895">

Interface

</th><th align="left" id="d228500e898">

Action

</th></tr></thead><tbody><tr><td id="d228500e904">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.
2.  Select **New**.
3.  Select **Slack Enterprise Integration Profile**.


</td></tr><tr><td id="d228500e946">

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

Status

</td><td>

Status of the integration profile.-   If you have not published the integration profile, this field is automatically set to `Draft`.
-   If you have already published the integration profile, this field is automatically set to `Published`.


</td></tr><tr><td>

Profile Type

</td><td>

Type of integration profile. This field is automatically set to `Slack Enterprise Subscription`.

</td></tr></tbody>
</table>3.  Review the required user roles or API permissions specified in the **Vendor configuration** field for each process to minimize security risks and optimize SaaS licenses.

    **Note:** For more information, see [Minimal user permissions](integrate-with-slack.md#) table.

    1.  In the Download Subscription Subflow section, verify that the **Subflow** field is set to **Slack Download Subscriptions**.

        **Note:** The **Download subscriptions** check box is selected by default and you can't clear it.

    2.  In the Calculate Activity Subflow section, verify that the **Subflow** field is set to **Slack Update User Activity**.

        **Note:** The **Download Activity** check box is selected by default. If you clear it, the activity scheduled job **SAM - Refresh &lt;displayname&gt; Activity** isn't created.

        In the **Analyze user activity** field, you can also select the date and time starting from when you want to analyze the user activity. By default, you can analyze user activity up to 60 days prior to the current date and view events performed by individual users from the time you create this profile.

        **Note:** Software Asset Management pulls the events from the time that you start analyzing user activity irrespective of the profile creation date.

        You can modify this value in the Last activity threshold field of your software reclamation rules. For more information, see [Review a software reclamation rule](../task/add-reclamation-rule-sub.md).

    3.  In the Reclaim Subscription Subflow section, verify that the **Subflow** field is set to **Slack Reclaim Subscription**.

        **Note:** The **Reclaim subscriptions** check box is selected by default. If you don't want to reclaim subscriptions, you can clear this check box. If you clear it, the removal candidates are created but the reclaim subscription subflow isn't triggered or the reclamation process isn't initiated.

4.  Select **Save**.

    Your ServiceNow instance creates a draft integration profile.

    The **Connection &amp; Credential** field appears and is automatically set to **sn\_slack\_ah\_v2.Slack\_Enterprise**.

5.  Open the connection &amp; credential aliases record by selecting the preview icon ![](../image/preview-icon.png) next to the **Connection &amp; Credential** field and then selecting **Open Record** in the record preview.

6.  On the Connection &amp; Credential Aliases form, select the **Create New Connection &amp; Credential** related link.

7.  In the Create Connection and Credential dialog box, fill in or verify the following fields.

    |Field|Value|
    |-----|-----|
    |Name|Name of the Slack Enterprise Grid connection.|
    |OAuth Client ID|Client ID that is assigned to your Slack Enterprise Grid application. Enter the same client ID that you copied in [Create a Slack Enterprise Grid application](integrate-with-slack.md#).|
    |OAuth Client Secret|Client secret that is assigned to your Slack Enterprise Grid application. Enter the same client secret that you copied in [Create a Slack Enterprise Grid application](integrate-with-slack.md#).|
    |OAuth Redirect URL|Redirect URL for your Slack Enterprise Grid application. This field populates automatically.|

8.  Select **Configure and Get OAuth Token**.

    **Note:** For the role required to perform this step, refer to the [Minimal user permissions](integrate-with-slack.md#) table.

9.  On the Authorize App dialog box, verify if the Enterprise Grid workspace is available on the top-right list.

10. If the Enterprise Grid workspace is available, select the Enterprise Grid workspace.

11. If the Enterprise Grid workspace isn’t available,

    1.  Select **Add another workspace**.

    2.  Enter the Enterprise Grid workspace URL.

    3.  Select **Continue**.

        You get redirected to the Authorize App dialog box.

    4.  Select **Allow**.

        The OAuth access token becomes available for authorizing your Enterprise connection.

12. Create a connection between your Slack workspace and your ServiceNow instance to retrieve user data from your workspace.

    1.  Open the connection &amp; credential record set on the integration profile.

    2.  Select the **Child Aliases** tab.

    3.  Select **New**.

        **Tip:** If the **New** button isn't visible, change the scope to the Slack Spoke of the child alias by navigating to the **Application scope** and reloading the Connection &amp; Credential Aliases page.

    4.  On the new child alias form that opens up, provide a name for the child alias.

    5.  Select **Submit**.

    6.  Open the child alias record that you created and select the **Create New Connection &amp; Credential** related link.

    7.  In the Create Connection and Credential dialog box, fill in or verify the following fields.

        |Field|Value|
        |-----|-----|
        |Name|Name of the Slack workspace connection.|
        |OAuth Client ID|Client ID that is assigned to your Slack workspace application. Enter the same client ID that you copied in [Create a Slack workspace application](integrate-with-slack.md#).|
        |OAuth Client Secret|Client secret that is assigned to your Slack workspace application. Enter the same client secret that you copied in [Create a Slack workspace application](integrate-with-slack.md#).|
        |OAuth Redirect URL|Redirect URL for your Slack workspace application. This field populates automatically.|

    8.  Select **Configure and Get OAuth Token**.

        **Note:** For the role required to perform this step, refer to the [Minimal user permissions](integrate-with-slack.md#) table.

    9.  In the Authorize App dialog box, select **Allow**.

        The OAuth access token becomes available for authorizing your Slack workspace connection.

    10. Repeat steps a through i for each workspace connection that you want to associate with your instance.

13. On the integration profile form, select **Validate Connection** to verify the connection and credential details of this integration.

    Validating the connection verifies the Download Subscriptions and Calculate Activity APIs, but not the Reclaim Subscriptions APIs.

    **Important:** If you encounter configuration issues while validating the integration profile or retrieving subscriptions, refer to the knowledge base for troubleshooting guidance. For more information, see knowledge base article [KB2536373](https://support.servicenow.com/kb?sys_kb_id=1f87321d93507290d9743f986cba10c1&id=kb_article_view).

14. After the connection is verified, select **Publish**.

15. In the dialog box, select **OK**.

    **Note:** If you clear the **Download Activity** check box after the integration profile is published, you must revalidate the connections and then republish the integration profile because the following events occur:

    -   The **Status** field on the integration profile form changes to **Draft**.
    -   The **Validate connection** button shows up on the form.
    -   The current **SAM - Refresh &lt;displayname&gt; Activity** job gets deleted.
16. To optimize memory and avoid performance issues in your Slack flow, you can turn off the flow engine reporting level.

    1.  Navigate to **System Properties** &gt; **All Properties**.

    2.  Select the system property **com.snc.process\_flow.reporting.level**.

    3.  On the System Property page, set the **Value** to `OFF`.

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

