---
title: Integrating with Azure AD
description: You can integrate your ServiceNow instance with Microsoft Azure Active Directory \(AD\) to view software usage for all connected SSO applications.Create an app in the Microsoft Azure AD portal to integrate with the ServiceNow AI Platform.Create an Azure AD integration profile in your ServiceNow instance.Connect a Single Sign-On \(SSO\) app to view all users and groups with access to the app. Track user login data and reclaim unused licenses.
locale: en-US
release: xanadu
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2025-02-18"
reading_time_minutes: 9
breadcrumb: [Integrate with SSO providers, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Integrating with Azure AD

You can integrate your ServiceNow instance with Microsoft Azure Active Directory \(AD\) to view software usage for all connected SSO applications.

**Important:** Minimize security risks and protect information by granting access only to the necessary user or API permissions.

<table id="table_box"><thead><tr><th>

Process

</th><th>

Required user role in the Microsoft Azure AD application

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

## Create a Microsoft Azure AD application

Create an app in the Microsoft Azure AD portal to integrate with the ServiceNow AI Platform.

### Before you begin

Microsoft Azure AD Role required: Refer to the [Minimal users permission](integrate-with-azure-ad.md#) table.

### Procedure

1.  From the Azure portal, access Microsoft Azure AD.

2.  Create a Microsoft Azure AD application.

    See [Create a Microsoft Azure AD application](https://docs.microsoft.com/en-us/azure/active-directory/develop/howto-create-service-principal-portal) for detailed instructions on registering and configuring an application.

    1.  In the **Redirect URI** field, enter `https://<instance-name>.service-now.com/oauth_redirect.do`, where `<instance-name>` is the name of your ServiceNow instance.

    2.  Record the application \(client\) ID and directory \(tenant\) ID to register the app as a third-party OAuth provider on your ServiceNow instance.

    3.  Create a client secret and save the correct value \(not the Client secret ID\) to register the app as a third-party OAuth provider on your ServiceNow instance.

    4.  Add permissions to access the Microsoft Graph API.

        |Permission|Type|
        |----------|----|
        |AuditLog.Read.All|Delegated|
        |User.Read.All|Delegated|
        |User.ReadWrite.All|Delegated|
        |GroupMember.Read.All|Delegated|
        |Application.Read.All|Delegated|

        For more information, see [Add permissions to access web APIs](https://docs.microsoft.com/en-us/azure/active-directory/develop/quickstart-configure-app-access-web-apis#add-permissions-to-access-web-apis).

    5.  Grant admin consent to your application.

        For more information, see [Understanding API permissions and admin consent UI](https://docs.microsoft.com/en-us/azure/active-directory/develop/quickstart-configure-app-access-web-apis#understanding-api-permissions-and-admin-consent-ui).


## Create an Azure AD integration profile

Create an Azure AD integration profile in your ServiceNow instance.

### Before you begin

To create an Azure AD integration profile, request the Software Asset Management - SaaS License Management plugin \(sn\_sam\_saas\_int\) from the [ServiceNow Store](https://store.servicenow.com/).

ServiceNow Role required: sam\_integrator or admin

### About this task

**Note:** Starting with version 7.0.0 of Software Asset Management - SaaS License Management and version 3.1.0 of the Microsoft Azure AD spoke, your ServiceNow instance creates a separate Azure AD connection for each Azure AD integration profile that you create. Each connection runs independently of each other, enabling your instance to support multiple independent Azure AD integration profiles.

If you’re using Software Asset Workspace, the option to create the Microsoft Azure AD integration profile in Core UI is inactive.

### Procedure

1.  Navigate to the integration profile.

<table id="choicetable_ipn_lnx_qtb"><thead><tr><th align="left" id="d58471e559">

Interface

</th><th align="left" id="d58471e562">

Action

</th></tr></thead><tbody><tr><td id="d58471e568">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **SSO Integration Profiles**.
2.  Select **New**.
3.  Select **Microsoft Azure AD Integration Profile**.


</td></tr><tr><td id="d58471e610">

**Software Asset Workspace**

</td><td>

1.  Navigate to **License operations** &gt; **User Subscriptions** &gt; **SSO integration profiles**.
2.  Select **New**.
3.  Select **Microsoft Azure AD Integration Profile** from the drop-down list.
4.  Select **Continue**.


</td></tr></tbody>
</table>2.  In the **Display name** field, enter a name for the integration profile.

    The remaining fields are automatically populated when you submit the form.

    **Note:** The SSO integration is created using a directory integration. The directory integration pulls SSO applications, users, and group data that are associated with your SSO integrations. For more information, see [Viewing SSO subscription information](../reference/sso-subscriptions.md).

    If you already have a Microsoft Azure AD directory integration, the SSO integration uses your existing directory integration. Otherwise, a Microsoft Azure AD directory integration is automatically created.

3.  Select **Submit**.

4.  Select the **Create New Connection &amp; Credential** related link.

    **Note:** If you have installed Software Asset Workspace, open the Connection and credential record and select the **Create New Connection &amp; Credential** related link.

5.  On the form, fill in the fields.

    |Field|Value|
    |-----|-----|
    |Auth URL|`https://login.microsoftonline.com/<directory-id>/oauth2/v2.0/authorize`, where`<directory-id>` is the directory \(tenant\) ID from the Azure portal.|
    |Token URL|`https://login.microsoftonline.com/<directory-id>/oauth2/v2.0/token`, where`<directory-id>` is the directory \(tenant\) ID from the Azure portal.|
    |Revoke token URL|`https://login.microsoftonline.com/<directory-id>/oauth2/v2.0/revoke`, where`<directory-id>` is the directory \(tenant\) ID from the Azure portal.|
    |OAuth Client ID|Application \(client\) ID for the application you created in the Azure portal.|
    |OAuth Client Secret|Client secret for the application you created in the Azure portal.|
    |OAuth Redirect URL|`https://<instance-name>.service-now.com/oauth_redirect.do`, where `<instance-name>` is the name of your ServiceNow instance. This value is automatically populated.|

6.  Select **Create and Get OAuth Token**.

    You would get redirected to the Azure portal. For the role required to perform this step, refer to the [Minimal users permission](integrate-with-azure-ad.md#) table.

7.  In the pop-up window, sign in to your account with Azure AD admin credentials.

8.  Select **Publish**.

    Scheduled jobs and directory jobs download a list of all your applications, users, and groups. For more information, see [Viewing SSO subscription information](../reference/sso-subscriptions.md). View the status of your jobs in the Scheduled Job Results and Directory Job Results related lists of the integration profile. Software models are automatically created for applications with an **External Catalog ID** that matches an **Identifier** in the Subscription Product Definitions \[samp\_sw\_subscription\_product\_definition\] table.


### Result

After you publish the integration profile and connect applications to the profile, you can view events performed by individual users up to 60 days prior to the current date. For more information, see [Review a software reclamation rule](../task/add-reclamation-rule-sub.md).

## Connect SSO apps

Connect a Single Sign-On \(SSO\) app to view all users and groups with access to the app. Track user login data and reclaim unused licenses.

### Before you begin

Role required: sam\_integrator or admin

### About this task

**Note:** For Microsoft Azure AD, the **Assignment required** toggle button on the application configuration page controls the access of the application by users.

-   If the **Assignment required** toggle button is set to **Yes**, you must assign this application to the Microsoft Azure AD users and related applications and services. After you assign the application, Microsoft Azure AD users, associated applications, and services can access it.
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

4.  Select a date for the **Analyze last activity from** field.

    You can choose to start analyzing login data for individual users and applications from the current date or from up to 60 days in the past. The default value is 30 days. Choosing a past date enables you to detect stale subscriptions without waiting in real time because you can see subscriptions that haven't been used recently. Because choosing a date in the past increases the amount of data that is analyzed, it might take you longer to be able to view the results.

5.  Select **Save**.

6.  Select **Connect**.

    **Tip:** You can also connect multiple apps simultaneously from the **SSO Applications** list.

    In the Core UI interface, select the apps using the check box on the side of the list. At the bottom of the list, select the **Actions on selected rows** drop-down menu and then select **Connect**. If some apps don't have a software model, the **Connect** action shows that not all apps are connected. For example, **Connect \(1 of 4\)** shows that only 1 of the four apps you selected are connected. Add software models to connect the remaining apps.


### Result

After the SSO application connects, your ServiceNow instance automatically creates users, groups, subscriptions, and reclamation rules that are refreshed daily.

-   If the **Assignment required** toggle button is set to **Yes** for an application in the Microsoft Azure AD portal, the subscription is created only for users assigned to that specific application.
-   If the **Assignment required** toggle button is set to **No** for an application in the Microsoft Azure AD portal, the subscription is created for all Microsoft Azure AD users.

### What to do next

Review all automatically generated reclamation rules to meet your specifications for reclaiming user subscriptions. For more information, see [Review a software reclamation rule](../task/add-reclamation-rule-sub.md).

Create software entitlements for the automatically generated software models to track used software against owned software. For more information on creating software entitlements in the Software Asset Management classic application, see [Create entitlements in Software Asset Management classic](../task/track-software-rights.md). For more information on creating software entitlements in the Software Asset Workspace, see [Create entitlements in workspace](../task/create-entitlements-workspace.md). For more information on creating software entitlements using the Software Asset Management Playbook, see [Create entitlements using the guided walk-through](../task/guidedwalk-workspace.md).

Reconciliation also runs on your subscriptions as a scheduled job or on-demand. You can view your reconciliation results in the [License Workbench](sam-license-workbench.md) \(Software Asset Management classic application\) or the [License usage view](sam-workspace-workbench.md) \(Software Asset Workspace\). Use these results to determine your license compliance position and to remediate any non-compliance. For more information on running reconciliation in the Software Asset Management classic application, see [Run software reconciliation](../task/t_RunReconciliation.md). For more information on running reconciliation in the Software Asset Workspace, see [Run software reconciliation in the workspace](../task/run-recon-workspace.md).

