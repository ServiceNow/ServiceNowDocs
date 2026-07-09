---
title: Integrate with Docusign at Account level
description: Integrating your Software Asset Management application with the Docusign service enables you to track your software subscriptions and to reclaim unused licenses.Register a Docusign application through the Docusign admin portal.Create a Docusign integration profile at Account level to track software subscriptions and optimize licensing for the Docusign service.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-asset-management/saas-license-management/integrate-with-docusign-account.html
release: zurich
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2025-11-07"
reading_time_minutes: 8
breadcrumb: [Integrating with Docusign, Integrate with SaaS applications, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Integrate with Docusign at Account level

Integrating your Software Asset Management application with the Docusign service enables you to track your software subscriptions and to reclaim unused licenses.

Docusign purchases made through resellers don’t reflect within the Docusign standard billing system. So no values are returned through the APIs for envelope consumption that is available to ServiceNow.

**Important:** Docusign has removed the **lastLogin** field from the Users API, so the user's last activities are no longer tracked as part of this integration. The Software Asset Management application now creates reclamation candidates based on the subscription assigned date.

For more information about the Docusign service, see [the DocuSign Developer site](https://developers.docusign.com/ios_sdk/developer.html).

**Important:** Minimize security risks and protect information by granting access only to the necessary user or API permissions.

|Process|Required user role in the Docusign application|Authentication scopes|
|-------|----------------------------------------------|---------------------|
|Download subscriptions|admin|No scopes|
|Reclaim subscription|admin|No scopes|

## Register a Docusign application

Register a Docusign application through the Docusign admin portal.

### Before you begin

Docusign Role required: admin

### Procedure

1.  Log in to your Docusign demo \(non-production\) account.

    You can use any subaccount for logging in that is later promoted to the corresponding production account.

2.  Go to the Admin tab.

    -   If you already have an API integration key from a previous integration ready for use in production, skip to [step 14](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/saas-license-management/integrate-with-docusign-account.md).
    -   If you don't have your API integration key saved, you must generate a new one.
3.  On the side navigation pane, select **INTEGRATIONS** &gt; **Apps and Keys**.

4.  In the **Apps and Integration Keys** section, select **Add App and Integration key**.

5.  On the Add Integration Key form, enter a unique name for your application in the **App Name** field and select **CREATE APP**.

6.  On the profile page of your application, select **Third-party integration key** in the **Integration Type** field.

7.  Copy the value of the **Integration Key** and secure it for later use.

    Save the Integration Key \(Client ID\) in a secure location to use it later for integration with the ServiceNow instance.

8.  Select **Save**.

9.  In the **Apps and Integration Keys** section, locate the application that you just created in the App Name list.

10. Select **Actions** &gt; **Select Go-Live account**.

    A Docusign login window pops up prompting you to enter the credentials for your Docusign account.

11. Enter your Docusign credentials.

12. Select a production account on the window that pops up prompting you to choose a production account to which you want to promote your integration key.

    The **Go Live Status** field changes to **Pending approval**. For a successful Go-Live review, your app must meet the requirements for Go-Live for each API that it uses. For more information on the Go-Live review stages, see [Docusign documentation](https://developers.docusign.com/platform/go-live/).

13. After the integration is approved, the **Go Live Status** changes to **View in production**.

14. Log in to your Docusign production account and verify that the same integration key has been promoted to the production account.

15. On the side navigation pane, select **INTEGRATIONS** &gt; **Apps and Keys**.

16. Next to your application, select **Actions** &gt; **Edit**.

17. Select **ADD URI** and add `https://*ServiceNow instance*.service-now.com/oauth_redirect.do`.

18. Select **ADD SECRET KEY**.

    Save the Secret Key \(Client secret\) for your production account in a secure location to use it later for integration with the ServiceNow instance.

19. Select **Save**.


## Create a Docusign integration profile at Account level

Create a Docusign integration profile at Account level to track software subscriptions and optimize licensing for the Docusign service.

### Before you begin

To create a Docusign integration profile, request the Software Asset Management - SaaS License Management plugin \(sn\_sam\_saas\_int\) from the [ServiceNow Store](https://store.servicenow.com/).

ServiceNow Role required: sam\_integrator or admin

### About this task

If you’re using Software Asset Workspace, the option to create the Docusign integration profile in Core UI is inactive.

### Procedure

1.  Navigate to the integration profile.

<table id="choicetable_o3p_z3k_qtb"><thead><tr><th align="left" id="d67857e550">

Interface

</th><th align="left" id="d67857e553">

Action

</th></tr></thead><tbody><tr><td id="d67857e559">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.
2.  Select **New**.
3.  Select **DocuSign Integration Profile**.


</td></tr><tr><td id="d67857e601">

**Software Asset Workspace**

</td><td>

1.  Navigate to **License operations** &gt; **User Subscriptions** &gt; **Direct integration profiles**.
2.  Select **New**.
3.  Select **DocuSign** from the drop-down list.
4.  Select **Continue**.


</td></tr></tbody>
</table>2.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Display name|Name of the integration profile. For example, `DocuSign Integration`|
    |Integration type|The default value is set to **Account Level**.|
    |Client Id|Client ID for the OAuth application created in the SaaS admin account in the [Register a Docusign application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/saas-license-management/integrate-with-docusign-account.md) procedure.|
    |Redirect url|URL of the OAuth provider that you're redirected to after authentication. This value is automatically populated.|
    |Technical account Id|API Account ID from your Docusign production account.|
    |Instance URL|URL of the login page used for accessing your Docusign production account. This field is automatically set to **https://account.docusign.com**.|
    |Client secret|Password associated with the client ID created in the [Register a Docusign application](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/saas-license-management/integrate-with-docusign-account.md) procedure.|
    |Profile type|Type of integration profile. This value is automatically set to **DocuSign Subscription**.|

3.  Review the required user roles or API permissions specified in the **Vendor configuration** field for each process to minimize security risks and optimize SaaS licenses.

    **Note:** For more information about the required roles and scopes, see the [Minimal user permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/saas-license-management/integrate-with-docusign-account.md) table.

    -   The **Download subscriptions** check box is selected by default and you can't clear it.

    -   The **Reclaim subscriptions** check box is selected by default. If you don't want to reclaim subscriptions, you can clear this check box. If you clear it, the removal candidates are created but the reclaim subscription subflow isn't triggered or the reclamation process isn't initiated.

4.  Select **Submit**.

    A draft integration profile is created.

5.  On the integration profile, select **Get OAuth Token** and follow the steps to get an OAuth token.

    **Note:** For the role required to perform this step, refer to the [Minimal user permissions](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/saas-license-management/integrate-with-docusign-account.md) table.

6.  On the integration profile form, select **Validate Connection** to verify the connection and credential details of this integration.

    Validating the connection verifies the Download Subscriptions APIs, but not the Reclaim Subscriptions APIs.


### Result

You can view events performed by individual users up to one year prior to the current date. For more information, see [Review a software reclamation rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/saas-license-management/add-reclamation-rule-sub.md). Software Asset Management pulls the events from the time that you start downloading user subscriptions irrespective of the profile creation date.

### What to do next

After the integration connects, your ServiceNow instance automatically creates software models, reclamation rules, and software subscriptions that are refreshed daily.

After creating an integration profile, view information about the profile in the Software Asset Workspace by navigating to **License operations** &gt; **User subscription** &gt; **Direct integration profiles**. You can select an integration profile to view the following related lists. If the following related lists aren't visible for an integration profile in the default view, you can select the custom integration view from the Details tab:

-   Software Models
-   Unrecognized Subscription Identifiers
-   Scheduled Jobs
-   Scheduled Job Results
-   Software Subscriptions
-   Subscription Identifier Exclusion Rule
-   Subscription User Exclusion Rule

After creating an integration profile, you can define subscription exclusion rules to keep certain subscriptions from license cost calculations. For more information, see [Subscription exclusions for SaaS and SSO applications](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/saas-license-management/subscription-exclusions.md).

If you want to set up multiple integration profiles with unique connections, create child aliases to manage different configurations and settings for each integration profile. For more information, see [Create a child alias to set up multiple integration profiles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/saas-license-management/create-child-alias-saas.md).

Review all automatically generated reclamation rules to reclaim user subscriptions. For more information, see [Review a software reclamation rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/saas-license-management/add-reclamation-rule-sub.md).

Create software entitlements for the automatically generated software models to track used software against owned software.

-   For more information on creating software entitlements in the Software Asset Management Core UI, see [Create entitlements in Software Asset Management classic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/software-asset-management/track-software-rights.md).
-   For more information on creating software entitlements in the Software Asset Workspace, see [Create entitlements in workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/software-asset-management/create-entitlements-workspace.md).
-   For more information on creating software entitlements using the Software Asset Management Playbook, see [Create entitlements using the guided walk-through](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/software-asset-management/guidedwalk-workspace.md).

Reconciliation also runs on your subscriptions as a scheduled job or on-demand. You can view your reconciliation results in the [License Workbench](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/software-asset-management/sam-license-workbench.md) \(Software Asset Management classic application\) or the [License usage view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/software-asset-management/sam-workspace-workbench.md) \(Software Asset Workspace\). Use these results to determine your license compliance position and to remediate any non-compliance.

-   For more information on running reconciliation in the Software Asset Management classic application, see [Run software reconciliation in Software Asset Management classic](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/software-asset-management/t_RunReconciliation.md).
-   For more information on running reconciliation in the Software Asset Workspace, see [Run software reconciliation in the workspace](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/software-asset-management/run-recon-workspace.md).

