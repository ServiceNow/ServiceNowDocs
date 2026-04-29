---
title: Integrating with Microsoft Dynamics 365 and Power Apps
description: Integrating your ServiceNow instance with the Microsoft Dynamics 365 and Power Apps service enables you to track your software subscriptions and to reclaim unused licenses.Set up Microsoft Azure Active Directory \(AD\).Set the system-level settings for Microsoft Dynamics 365 and Power Apps.Set up ServiceNow instance for Microsoft Dynamics 365 and Power Apps to track your software subscriptions and to reclaim unused licenses.Evaluating the software usage activity of Microsoft Dynamics 365 subscriptions helps you monitor license usage, optimize license allocation, and potentially reduce costs for the assigned licenses. Software usage activity refers to how software products are being used.
locale: en-US
release: australia
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 10
breadcrumb: [Integrate with SaaS applications, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Integrating with Microsoft Dynamics 365 and Power Apps

Integrating your ServiceNow instance with the Microsoft Dynamics 365 and Power Apps service enables you to track your software subscriptions and to reclaim unused licenses.

**Important:**

This integration retrieves user subscription details for all Microsoft Dynamics 365 and Power Apps products. Furthermore, Software Asset Management provides license compliance for the products using user subscription-based models.

For optimization, Software Asset Management automatically tracks the last activity date and identifies low-usage for the following applications:

-   Dynamics 365 for Sales \(Professional, Premium, Enterprise\)
-   Dynamics 365 for Customer Service \(Professional, Enterprise, Enterprise for Government, Professional Attach to Qualifying Dynamics, Sales and Customer Service Enterprise\)
-   Dynamics 365 for Team Members
-   Microsoft Relationship Sales \(MRS\)

For more information about the Microsoft 365 service, see [Microsoft 365 frequently asked questions](https://www.microsoft.com/en-in/microsoft-365/microsoft-365-for-home-and-school-faq).

**Important:** Minimize security risks and protect information by granting access only to the necessary user or API permissions.

<table id="table_box"><thead><tr><th>

Process

</th><th>

Required user role in the Microsoft Dynamics 365 and Power Apps application

</th><th>

Authentication scopes

</th></tr></thead><tbody><tr><td>

Download subscriptions

</td><td>

Global Reader

</td><td>

-   LicenseAssignment.Read.All
-   User.Read.All

</td></tr><tr><td>

Pull user activity

</td><td>

Dynamics 365 administrator

</td><td>

user\_impersonation

</td></tr></tbody>
</table>## Set up Microsoft Azure Active Directory

Set up Microsoft Azure Active Directory \(AD\).

### Before you begin

Role required: Global administrator and Dynamics 365 administrator in Microsoft admin center

### Procedure

1.  Log in to the Microsoft Azure portal using an admin account and navigate to **Azure Active Directory**.

2.  Navigate to the App registrations section and select **App registration** under **+ Add**.

3.  On the Register an application form, fill in the fields.

<table id="table_oqq_3cy_y2c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the application that you want to register.

</td></tr><tr><td>

Supported account types

</td><td>

The account with the required organizational directory.

</td></tr><tr><td>

Redirect URI

</td><td>

URL that accesses Azure. Typically the URL of the ServiceNow instance.**Important:** You must select **Web** in the **Select a platform** drop-down list because Azure AD app must be a web application in App registration for this setup.

</td></tr></tbody>
</table>4.  Select **Register**.

5.  Open the application that you registered and navigate to the **Overview** section.

6.  Collect the Application \(client\) ID and Directory \(tenant\) ID.

7.  Navigate to the Certificates and Secrets section.

8.  Create a client secret and collect the client secret key.

    You need the client secret key while configuring your ServiceNow instance.

9.  Under API Permission, select **+ Add a permission** and then select **APIs my organization uses**.

10. Select Microsoft Graph and add the necessary permissions for both Delegated and Application types as required.

    -   `Organization.Read.All`
    -   `User.Read.All`
    -   `Offline_access`
11. Select Dynamics CRM and add the following permission.

    `user_impersonation`

    **Note:** These steps aren't applicable for user\_impersonation or Microsoft Dynamics CRM connection because the user\_impersonation scope is offered as a Delegated permission in Microsoft Dynamics CRM.

12. Under Grant consent, select **Grant admin consent**.

13. In the Authentication section, under the Redirect URI, enter the redirect URI of the ServiceNow instance.


## Set up Microsoft Dynamics 365 and Power Apps

Set the system-level settings for Microsoft Dynamics 365 and Power Apps.

### Before you begin

Role required: admin

### Procedure

1.  Go to [https://admin.powerplatform.microsoft.com/](https://admin.powerplatform.microsoft.com/).

2.  Under Environments, select the environment for which you want to pull the dynamics activities.

3.  From the top ribbon, select **Settings**.

4.  Select **Audit and logs**.

5.  Select the following check boxes.

    -   Start Auditing
    -   Log access
    -   Read logs
6.  Select **Additional Audit Settings**.

7.  From the **Settings** list, select **Auditing**.

8.  Select **Global Audit Settings**.

9.  Select the following check boxes.

    -   Start Auditing
    -   Audit user access
    -   Start Read Audit
    -   Common Entities
    -   Sales Entities
    -   Customer Service Entities
10. Select **OK**.


## Set up ServiceNow instance for Microsoft Dynamics 365 and Power Apps

Set up ServiceNow instance for Microsoft Dynamics 365 and Power Apps to track your software subscriptions and to reclaim unused licenses.

### Before you begin

Role required: sam\_integrator

**Important:** You must select the **Microsoft Dynamics 365 Spoke** check box for this integration while installing optional features on the [Application Manager](https://www.servicenow.com/docs/access?context=application-manager&version=australia&pubname=australia-platform-administration&ft:locale=en-US) page. For more information about choosing the required SaaS applications, see [Request SaaS License Management](../task/request-saas-license-management.md).

### About this task

If you’re using Software Asset Workspace, the option to create the Microsoft Dynamics 365 and Power Apps integration profile in Core UI is inactive.

### Procedure

1.  Navigate to the integration profile.

<table id="choicetable_o3p_z3k_qtb"><thead><tr><th align="left" id="d221663e712">

Interface

</th><th align="left" id="d221663e715">

Action

</th></tr></thead><tbody><tr><td id="d221663e721">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.
2.  Select **New**.
3.  Select **Microsoft Dynamics 365 and Power Apps Integration Profile**.


</td></tr><tr><td id="d221663e763">

**Software Asset Workspace**

</td><td>

1.  Navigate to **License operations** &gt; **User Subscriptions** &gt; **Direct integration profiles**.
2.  Select **New**.
3.  Select **Microsoft Dynamics 365 and Power Apps** from the drop-down list.
4.  Select **Continue**.


</td></tr></tbody>
</table>2.  In the **Display name** field, enter a name of your choice.

3.  Under the **Calculate Activity Subflow** tab in the **Analyze user activity from** field, select the date since when you want to pull the activity.

4.  Select **Save**.

    A draft integration profile is created. In the **Download Subscription Subflow** tab, the **Connection &amp; Credential** field appears and is automatically set to **sn\_ms\_365\_spoke.Microsoft\_365\_Graph**. In the **Calculate Activity Subflow** tab, the **Connection &amp; Credential** field appears and is automatically set to **sn\_ms\_365\_spoke.Microsoft\_365\_Dynamics**.

5.  Under the **Download Subscription Subflow** tab, beside the **Connection &amp; Credential** field, select the preview \(![preview icon](../image/preview-icon.png)\) icon.

6.  Under the **Please Enter the Credential Information** section, enter the values you received from [Set up Microsoft Azure Active Directory](integrating-with-microsoft365.md#).

    1.  In the **Tenant ID** field, enter your Tenant ID.

    2.  In the **OAuth Client ID** field, enter the OAuth Client ID.

    3.  In the **OAuth Client Secret** field, enter the OAuth Client Secret key.

7.  Select **Create and Get OAuth Token**.

    **Important:** This step must be executed by a user with the Global administrator role in the Microsoft admin center.

8.  If you’re prompted to log in to your Microsoft 365 account, enter your Microsoft 365 credentials and log in to your Microsoft 365 account.

9.  Under the **Calculate Activity Subflow** tab, beside the **Connection &amp; Credential** field, select the Preview \(![Preview](../image/preview-icon.png)\) icon.

10. Select **Create New connection and credential alias**.

11. In the Create Connection and Credential window, perform the following.

    1.  In the **Connection URL** field, enter the connection URL.

        To fetch Connection URL, log in to the Microsoft Admin portal and navigate to **Admin Centers** &gt; **All admin centers** &gt; **Select Dynamics 365 apps** &gt; **Environments**. Select the environment you want to integrate with. The environment URL is the Connection URL.

    2.  Select the permission type to ensure your application accesses data correctly and securely.

        The permission type can be **Application Permissions** or **Delegated Permissions** depending on the application's data access requirements. For more information on permission types, see [Software Asset Management publisher pack for Microsoft](microsoft-publisher-pack.md).

    3.  In the **OAuth Client ID** field, enter the OAuth Client ID.

    4.  In the **OAuth Client Secret** field, enter the OAuth Client Secret key.

12. Select **Create and Get OAuth Token**.

    **Important:** This step must be executed by a user with the Dynamics 365 administrator role in the Microsoft admin center.

13. Return to the integration profile.

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

## Optimizing Microsoft Dynamics 365 subscriptions

Evaluating the software usage activity of Microsoft Dynamics 365 subscriptions helps you monitor license usage, optimize license allocation, and potentially reduce costs for the assigned licenses. Software usage activity refers to how software products are being used.

Based on the software usage activity and the incurred cost, Software Asset Management generates optimization recommendations for your software subscriptions that include the following:

-   **Low usage subscriptions**

    Software Asset Management recommends reclaiming the low usage subscriptions. For example, if the last activity date is 60 days prior to the current date, the subscription is considered a low usage subscription.

-   **Consolidated subscriptions**

    If a user has multiple base licenses for different Microsoft Dynamics 365 applications, Software Asset Management recommends consolidating the subscriptions to optimize licensing. This approach involves purchasing one base license and obtaining the rest as attached licenses, ensuring compliance with Microsoft's licensing terms while being more cost-effective.

    For example, if Dynamics 365 Commerce, Dynamics 365 Finance, and Dynamics 365 Human Resources base license subscriptions are purchased for a user, Software Asset Management recommends using Dynamics 365 Commerce as base license and Dynamics 365 Finance and Dynamics 365 Human Resources as attached licenses to the base license. For more information, you can download the Dynamics 365 Licensing Guide from the [Dynamics 365 pricing overview page](https://www.microsoft.com/en-us/dynamics-365/pricing-overview).


After completing the [Integrating with Microsoft Dynamics 365 and Power Apps](integrating-with-microsoft365.md#) integration, you can view the usage activity information in the Software Subscription \[samp\_sw\_subscription\] table.

**Related topics**  


[Reclamation rules for SaaS and SSO applications](../reference/reclamation-rules.md)

