---
title: Integrating with Microsoft Entra ID
description: You can integrate your ServiceNow instance with Microsoft Entra ID to view software usage for all connected SSO applications.Create an app in the Microsoft Entra ID portal to integrate with the ServiceNow AI Platform.Create a Microsoft Entra ID integration profile in your ServiceNow instance.Connect a Single Sign-On \(SSO\) app to view all users and groups with access to the app. Track user login data and reclaim unused licenses.
locale: en-US
release: australia
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 12
breadcrumb: [Integrate with SSO providers, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Integrating with Microsoft Entra ID

You can integrate your ServiceNow instance with Microsoft Entra ID to view software usage for all connected SSO applications.

**Important:** Minimize security risks and protect information by granting access only to the necessary user or API permissions.

<table id="table_box"><thead><tr><th>

Process

</th><th>

Required user role in the Microsoft Entra ID application

</th><th>

Authentication scopes

</th></tr></thead><tbody><tr><td>

-   Download users
-   Download groups
-   Download group memberships

</td><td>

Application developer

</td><td>

-   User.Read.All
-   GroupMember.Read.All
-   Application.Read.All

</td></tr><tr><td>

Download applications

</td><td>

Application developer

</td><td>

-   User.Read.All
-   GroupMember.Read.All
-   Application.Read.All

</td></tr><tr><td>

-   Connect applications
-   Update connected applications

</td><td>

-   Global reader/Reports reader/ Security/Administrator/Security operator/Security reader
-   Application developer

</td><td>

-   AuditLog.Read.All
-   User.Read.All
-   GroupMember.Read.All
-   Application.Read.All

</td></tr><tr><td>

Reclaim subscriptions

</td><td>

User Administrator

</td><td>

User.ReadWrite.All

</td></tr></tbody>
</table>**Parent Topic:**[Integrate with SSO providers](saas-sso-integration.md)

## Create a Microsoft Entra ID application

Create an app in the Microsoft Entra ID portal to integrate with the ServiceNow AI Platform.

### Before you begin

Microsoft Entra ID Role required: Refer to the [Minimal users permission](integrate-with-azure-ad.md#) table.

### Procedure

1.  From the Azure portal, access Microsoft Entra ID.

2.  Create a Microsoft Entra ID application.

    See [Create a Microsoft Entra ID application](https://docs.microsoft.com/en-us/azure/active-directory/develop/howto-create-service-principal-portal) for detailed instructions on registering and configuring an application.

    1.  In the **Redirect URI** field, enter `https://<instance-name>.service-now.com/oauth_redirect.do`, where `<instance-name>` is the name of your ServiceNow instance.

    2.  Record the application \(client\) ID and directory \(tenant\) ID to register the app as a third-party OAuth provider on your ServiceNow instance.

    3.  Create a client secret and save the correct value \(not the Client secret ID\) to register the app as a third-party OAuth provider on your ServiceNow instance.

    4.  Add permissions to access the Microsoft Graph API.

        |Permission|Type|
        |----------|----|
        |AuditLog.Read.All|Delegated or Application|
        |User.Read.All|Delegated or Application|
        |User.ReadWrite.All|Delegated or Application|
        |GroupMember.Read.All|Delegated or Application|
        |Application.Read.All|Delegated or Application|

        For more information, see [Add permissions to access web APIs](https://docs.microsoft.com/en-us/azure/active-directory/develop/quickstart-configure-app-access-web-apis#add-permissions-to-access-web-apis).

    5.  Grant admin consent to your application.

        For more information, see [Understanding API permissions and admin consent UI](https://docs.microsoft.com/en-us/azure/active-directory/develop/quickstart-configure-app-access-web-apis#understanding-api-permissions-and-admin-consent-ui).


## Create a Microsoft Entra ID integration profile

Create a Microsoft Entra ID integration profile in your ServiceNow instance.

### Before you begin

To create a Microsoft Entra ID integration profile, request the Software Asset Management - SaaS License Management plugin \(sn\_sam\_saas\_int\) from the [ServiceNow Store](https://store.servicenow.com/).

ServiceNow Role required: sam\_integrator

**Important:** You must select the **Microsoft Entra ID Spoke** check box for this integration while installing optional features on the [Application Manager](https://www.servicenow.com/docs/access?context=application-manager&version=australia&pubname=australia-platform-administration&ft:locale=en-US) page. For more information about choosing the required SaaS applications, see [Request SaaS License Management](../task/request-saas-license-management.md).

### About this task

**Note:** Starting with version 7.0.0 of Software Asset Management - SaaS License Management and version 3.1.0 of the Microsoft Entra ID spoke, your ServiceNow instance creates a separate Entra ID connection for each Microsoft Entra ID integration profile that you create. Each connection runs independently of each other, enabling your instance to support multiple independent Microsoft Entra ID integration profiles.

If you’re using Software Asset Workspace, the option to create the Microsoft Entra ID integration profile in Core UI is inactive.

### Procedure

1.  Navigate to the integration profile.

<table id="choicetable_ipn_lnx_qtb"><thead><tr><th align="left" id="d68869e584">

Interface

</th><th align="left" id="d68869e587">

Action

</th></tr></thead><tbody><tr><td id="d68869e593">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **SSO Integration Profiles**.
2.  Select **New**.
3.  Select **Microsoft Entra ID Integration Profile**.


</td></tr><tr><td id="d68869e635">

**Software Asset Workspace**

</td><td>

1.  Navigate to **License operations** &gt; **User Subscriptions** &gt; **SSO integration profiles**.
2.  Select **New**.
3.  Select **Microsoft Entra ID Integration Profile** from the drop-down list.
4.  Select **Continue**.


</td></tr></tbody>
</table>2.  In the **Display name** field, enter a name for the integration profile.

    The remaining fields are automatically populated when you submit the form.

    **Note:** The SSO integration is created using a directory integration. The directory integration pulls SSO applications, users, and group data that are associated with your SSO integrations. For more information, see [Viewing SSO subscription information](../reference/sso-subscriptions.md).

    If you already have a Microsoft Entra ID directory integration, the SSO integration uses your existing directory integration. Otherwise, a Microsoft Entra ID directory integration is automatically created.

3.  In the Process configuration section, view the required user roles or API permissions to minimize security risks and optimize SaaS licenses.

    **Note:** For more information about the required roles and scopes, see [Minimal user permissions](integrate-with-azure-ad.md#) table.

    -   The **Download applications, users, and groups** check box is selected by default and you can't clear it.

    -   The **Download Activity** check box is selected by default. If you clear it, the last activity for connected applications isn't pulled.
    -   The **Reclaim subscriptions** check box is selected by default. If you don't want to reclaim subscriptions, you can clear this check box. If you clear it, the removal candidates are created but the reclaim subscription subflow isn't triggered or the reclamation process isn't initiated.

4.  Select **Submit**.

    The **Connection &amp; Credential** field appears.

5.  Select the **Create New Connection &amp; Credential** related link.

    **Note:** If you have installed Software Asset Workspace, open the Connection and credential record and select the **Create New Connection &amp; Credential** related link.

6.  On the form, fill in the fields.

<table id="table_dlb_lcb_blb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Permission type

</td><td>

The type of permission for the integration profile to access data correctly and securely. Values include:

-   **Application Permissions**: Enable the application to access any data without a signed-in user.
-   **Delegated Permissions**: Enable the application to act in place of a signed-in user.


</td></tr><tr><td>

Auth URL

</td><td>

`https://login.microsoftonline.com/<directory-id>/oauth2/v2.0/authorize`, where`<directory-id>` is the directory \(tenant\) ID from the Azure portal.

</td></tr><tr><td>

Token URL

</td><td>

`https://login.microsoftonline.com/<directory-id>/oauth2/v2.0/token`, where`<directory-id>` is the directory \(tenant\) ID from the Azure portal.

</td></tr><tr><td>

Revoke token URL

</td><td>

`https://login.microsoftonline.com/<directory-id>/oauth2/v2.0/revoke`, where`<directory-id>` is the directory \(tenant\) ID from the Azure portal.

</td></tr><tr><td>

OAuth Client ID

</td><td>

Application \(client\) ID for the application you created in the Azure portal.

</td></tr><tr><td>

OAuth Client Secret

</td><td>

Client secret for the application you created in the Azure portal.

</td></tr><tr><td>

OAuth Redirect URL

</td><td>

`https://<instance-name>.service-now.com/oauth_redirect.do`, where `<instance-name>` is the name of your ServiceNow instance. This value is automatically populated.

</td></tr></tbody>
</table>7.  Select **Create and Get OAuth Token**.

    You're redirected to the Azure portal. For the role required to perform this step, refer to the [Minimal users permission](integrate-with-azure-ad.md#) table.

8.  In the pop-up window, sign in to your account with Microsoft Entra ID admin credentials.

9.  On the integration profile form, select **Validate Connection** to verify the connection and credential details of this integration.

10. After the connection is verified, select **Publish**.

11. In the Publish Confirmation dialog box, select **OK**.

    If you clear the **Download Activity** check box after the integration profile is published, you must revalidate the connections because the following events occur:

    -   The **Validate connection** button shows up on the form.
    -   The last activity for users of the connected applications isn't pulled anymore.
    Scheduled jobs and directory jobs download a list of all your applications, users, and groups. For more information, see [Viewing SSO subscription information](../reference/sso-subscriptions.md). View the status of your jobs in the Scheduled Job Results and Directory Job Results related lists of the integration profile. Software models are automatically created for applications with an **External Catalog ID** that matches an **Identifier** in the Subscription Product Definitions \[samp\_sw\_subscription\_product\_definition\] table.


### Result

After you publish the integration profile and connect applications to the profile, you can view events performed by individual users up to 60 days prior to the current date. For more information, see [Review a software reclamation rule](../task/add-reclamation-rule-sub.md).

## Connect SSO apps

Connect a Single Sign-On \(SSO\) app to view all users and groups with access to the app. Track user login data and reclaim unused licenses.

### Before you begin

Role required: sam\_integrator

### About this task

**Note:** For Microsoft Entra ID, the **Assignment required** toggle button on the application configuration page controls the access of the application by users.

-   If the **Assignment required** toggle button is set to **Yes**, you must assign this application to the Microsoft Entra ID users and related applications and services. After you assign the application, Microsoft Entra ID users, associated applications, and services can access it.
-   If the **Assignment required** toggle button is set to **No**, all users can log in to the application. The associated applications and services can also obtain an access token to this service.

SaaS License Management offers direct integrations with select applications. Direct integrations provide the most robust usage data. For a list of available direct integrations, see [Integrate with SaaS applications](create-integration-profile.md). If you have a direct integration for an app, connecting the same app in an SSO integration creates duplicate subscription records in your ServiceNow instance. If you connect an SSO app and later decide to create a direct integration for that app, disconnect the app before creating a direct integration.

**Note:** If you’re using Software Asset Workspace, the option to navigate to the SSO application in the Core UI is inactive.

### Procedure

1.  Navigate to the application.

    |Interface|Action|
    |---------|------|
    |**Core UI**|Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **SSO Applications**.|
    |**Software Asset Workspace**|Navigate to **License operations** &gt; **User Subscriptions** &gt; **SSO integration profiles**.|

2.  Select the application that you want to connect.

    For Software Asset Workspace, select the **SSO Applications** tab.

3.  If the **Software model** field is empty, add a software model for the app.

    An app must have a software model before you can connect it. Software models are automatically created for apps with an **External Catalog ID** that matches an **Identifier** in the Subscription Product Definitions \[samp\_sw\_subscription\_product\_definition\] table. For all other apps, you can create a software model manually. For more information, see [Create software models in Software Asset Management classic](../task/record-terms-software-licenses.md).

4.  Select the **Enable group based software model** check box for mapping an SSO group with a specific software model for the application.

    For example, if an application has multiple license models that are linked to specific groups, then you can map a group to a software model to optimize license usage.

    **Important:** If you select this option, you must create a mapping for the SSO group before connecting the application. After the mapping is complete, the SSO subscriptions get automatically created or updated according to the mapped software model. For more information, see [Create an SSO group software model mapping](../task/create-ssogrp-swmodel-mapping.md).

5.  Select a date for the **Analyze last activity from** field.

    You can choose to start analyzing login data for individual users and applications from the current date or from up to 60 days in the past. The default value is 30 days. Choosing a past date enables you to detect stale subscriptions without waiting in real time because you can see subscriptions that haven't been used recently. Because choosing a date in the past increases the amount of data that is analyzed, it might take you longer to be able to view the results.

6.  Select **Save**.

7.  Select **Connect**.

    **Tip:** You can also connect multiple apps simultaneously from the **SSO Applications** list.

    In the Core UI interface, select the apps using the check box on the side of the list. At the bottom of the list, select the **Actions on selected rows** drop-down menu and then select **Connect**. If some apps don't have a software model, the **Connect** action shows that not all apps are connected. For example, **Connect \(1 of 4\)** shows that only 1 of the four apps you selected are connected. Add software models to connect the remaining apps.


### Result

After the SSO application connects, your ServiceNow instance automatically creates users, groups, subscriptions, and reclamation rules that are refreshed daily.

-   If the **Assignment required** toggle button is set to **Yes** for an application in the Microsoft Entra ID portal, the subscription is created only for users assigned to that specific application.
-   If the **Assignment required** toggle button is set to **No** for an application in the Microsoft Entra ID portal, the subscription is created for all Microsoft Entra ID users.

### What to do next

Review all automatically generated reclamation rules to meet your specifications for reclaiming user subscriptions. For more information, see [Review a software reclamation rule](../task/add-reclamation-rule-sub.md).

After connecting the SSO application, view information about the SSO profile in the Software Asset Workspace by navigating to **License operations** &gt; **User subscription** &gt; **SSO integration profiles**. You can select an integration profile to view the following related lists:

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

