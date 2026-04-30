---
title: Integrate with Workday using OAuth 2.0
description: Integrate your Software Asset Management application with the Workday application using OAuth 2.0 authentication method to track your software subscriptions.To set up the Workday integration successfully, configure permissions in Workday for the OAuth 2.0 authentication method.Create Workday OAuth 2.0 credentials to get access to Workday APIs.Create a Workday integration profile to track software subscriptions and optimize licensing for your Workday applications.
locale: en-US
release: zurich
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2026-02-26"
reading_time_minutes: 9
breadcrumb: [Integrating with Workday, Integrate with SaaS applications, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Integrate with Workday using OAuth 2.0

Integrate your Software Asset Management application with the Workday application using OAuth 2.0 authentication method to track your software subscriptions.

## Configure permissions in Workday

To set up the Workday integration successfully, configure permissions in Workday for the OAuth 2.0 authentication method.

### Before you begin

Role required: Users having roles such as Security Admin, Integration Admin, Integration Auditor, who can create Integration System Users and assign required security policies.

### Procedure

1.  Register an Integration System User.

    **Note:** While filling out account information details, you must select the **Do Not Allow UI Sessions** check box.

2.  Create a security group and assign it to the Integration System User.

    1.  In **Action**, navigate to **Security Group** &gt; **Maintain Domain Permissions for Security Group** and provide the following permission:

        |Operation|Domain Security Policy|Functional Areas|
        |---------|----------------------|----------------|
        |Get Only|Worker Data: Current Staffing Information|Staffing|
        |View Only|Person Data: Work Address|Contact Information|
        |View Only|Worker Data: Active and Terminated Workers|Staffing|
        |View Only|Workday Accounts|System|
        |View and Modify|WQL for Workday Extend|System|
        |View and Modify|Workday Query Language|System|

        **Note:** Confirm that the domain security policies are activated for the security group using the active pending security policy changes.


### Result

The new credentials for this Integration System User would be used to configure the connection in the ServiceNow instance.

## Create Workday OAuth 2.0 credentials

Create Workday OAuth 2.0 credentials to get access to Workday APIs.

### Before you begin

Role required: Users having roles such as Security Admin, Integration Admin, Integration Auditor, who can create Integration System Users and assign required security policies.

### Procedure

1.  Log in to your Workday account.

2.  In the search bar, enter `register API client` and select **Register API Client**.

3.  On the Register API Client page, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Client Name|A unique name for the client application. For example, `Workday HR spoke`.|
    |Client Grant Type|Select **Authorization Code Grant**.|
    |Access Token Type|The type of access token. Select **Bearer**.|
    |Redirection URI|URL of your ServiceNow instance.|
    |Non-Expiring Refresh tokens|The option to enable refresh tokens which do not expire.|
    |Scope \(Functional Areas\)|Scopes required for the client application.|
    |Include Workday Owned Scope|The option to select scopes that are owned by Workday.|

4.  Select **OK**.

    The client ID and client secret are generated on the Register API Client page.

5.  Copy the values in the **Client ID** and **Client Secret** fields and secure them for later use for Workday integration.


## Create a Workday integration profile

Create a Workday integration profile to track software subscriptions and optimize licensing for your Workday applications.

### Before you begin

Role required: sam\_integrator

Install the latest Workday HR spoke. For more information about the latest version, see the **Spoke version** section in [Workday HR Spoke](https://www.servicenow.com/docs/access?context=workday-hr-spoke&version=zurich&pubname=zurich-integrate-applications&ft:locale=en-US).

**Important:** You must select the **Software Asset Management integration with Workday** check box for this integration while installing optional features on the [Application Manager](https://www.servicenow.com/docs/access?context=application-manager&version=zurich&pubname=zurich-platform-administration&ft:locale=en-US) page. For more information about choosing the required SaaS applications, see [Request SaaS License Management](../task/request-saas-license-management.md).

### About this task

If you’re using Software Asset Workspace, the option to create the Workday integration profile in Core UI is inactive.

### Procedure

1.  Navigate to the integration profile.

<table id="choicetable_o3p_z3k_qtb"><thead><tr><th align="left" id="d85115e608">

Interface

</th><th align="left" id="d85115e611">

Action

</th></tr></thead><tbody><tr><td id="d85115e617">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.
2.  Select **New**.
3.  Select **Workday Integration Profile**.


</td></tr><tr><td id="d85115e659">

**Software Asset Workspace**

</td><td>

1.  Navigate to **License operations** &gt; **User Subscriptions** &gt; **Direct integration profiles**.
2.  Select **New**.
3.  Select **Workday** from the drop-down list.
4.  Select **Continue**.


</td></tr></tbody>
</table>2.  On the form, fill in the fields.

<table id="table_qnq_djt_ysb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Integration Profile

</td></tr><tr><td>

Display name

</td><td>

Name of the integration profile. For example, `Workday integration`.

</td></tr><tr><td>

Authentication type

</td><td>

Type of authentication to access Workday APIs.-   Basic Auth
-   OAuth 2.0


</td></tr><tr><td>

Status

</td><td>

Status of the integration profile. -   If you haven’t published the integration profile, this field is automatically set to  **Draft**.
-   If you’ve already published the integration profile, this field is automatically set to  **Published**.


</td></tr><tr><td>

Profile type

</td><td>

Type of integration profile. This field is automatically set to **Workday Subscription**.

</td></tr></tbody>
</table>3.  In the Download Subscription Subflow section, verify that the **Subflow** field is set to **Workday Download Subscriptions**.

    **Note:** The **Download subscriptions** check box is selected by default and you can't clear it.

4.  Select **Save**.

    A draft integration profile gets created.

    The **Connection &amp; credential** field appears and is automatically set to **sn\_workday\_hr\_spke.WorkdayHR**.

5.  Open the connection &amp; credential aliases record by selecting the preview icon \(![Preview icon.](../image/preview-icon.png)\) next to the **Connection &amp; Credential** field and then selecting **Open Record** in the record preview.

6.  On the Connection &amp; Credential Aliases form, select the **Create New Connection &amp; Credential** related link.

7.  In the dialog box, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Connection Information|
    |Name|Name of the connection. For example, `Workday HR Connection`.|
    |Connection URL|URL for the connection. For example, `https://<*workday\_host*>/ccx/service/*tenant\_name*`, where &lt;*tenant\_name*&gt; is your Workday tenant name.|
    |Tenant name|Name of the Workday tenant.|
    |API Version|Version of the Workday API to use for requests.|
    |Credential Information|
    |Client ID|Client ID that you generated while creating a Workday OAuth credential. For more information, see [Create Workday OAuth 2.0 credentials](integrate-with-workday-oauth.md#).|
    |Client Secret|Client Secret that you retrieved while creating a Workday OAuth credential.|
    |Authorization URL|URL used to authorize the OAuth connection. For example, `https://<*auth-domain-name*>.workday.com/<*tenant*>/authorize`|
    |Token URL|URL used to generate the OAuth token. For example, `https://<*domain-name*>.workday.com/ccx/oauth2/<*tenant*>/token`|
    |OAuth Redirect URL|`https://<instance_name>/oauth_redirect.do`, where the instance name is the name of your ServiceNow instance.|

8.  Select **Create and Get OAuth Token**.

    You're redirected to the Workday login page.

9.  Log in to the Workday portal using the Integration System User credentials that you registered while configuring permissions in Workday.

    For more information, see [Configure permissions in Workday](integrate-with-workday-oauth.md#).

10. In the Authorize Workday dialog box, select **Allow** to allow user permissions for Workday.

    The OAuth token is generated and you're redirected to your ServiceNow instance.

11. Under the **FSE worker calculation** tab, activate the worker categories covered by your contract by setting the value of **Active** to **true** and entering the FSE percentage.

12. If worker categories are listed in your contract but not available in the FSE worker calculation tab, add a new worker category.

    1.  In the **FSE worker calculation** tab, select **New**.

    2.  On the form, fill in the fields.

        |Field|Description|
        |-----|-----------|
        |Worker Category|The worker category listed in your contract.|
        |FSE Percentage|The FSE percentage for the worker category that you added. Full Service Equivalent \(FSE\) is the method by which the subscriptions are calculated.|
        |Integration profile|The Workday integration profile that you created.|
        |Active|Option to make the worker category active.|

    3.  Select **Submit**.

13. Define the mapping of the newly created worker category.

    1.  Select the **Worker category** tab and select **New**.

    2.  On the form, fill in the fields:

        |Field|Description|
        |-----|-----------|
        |Worker Type|The type of worker, either Employee or Contingent.|
        |Employee/Contingent worker type|The type of Employee or Contingent worker.|
        |Time Type|Indicates whether the worker is full-time or part-time.|
        |Worker Category|The worker category that you created.|
        |Integration profile|The Workday integration profile that you created.|
        |Active|Option to make the mapping active.|

    3.  Select **Submit**.

14. Activate the list of modules that are defined in your contract.

    1.  Select the **Modules** tab.

    2.  Open the module record.

    3.  Set the **Active** field to **True**.

    4.  Select **Save**.

15. Verify that there is at least one active record in all the tabs for your contract: FSE worker calculation, Worker category, and Modules, before publishing the connection.

16. On the integration profile form, select **Validate Connection** to verify the connection and credential details of this integration.

17. After the connection is verified, select **Publish**.

18. In the Publish Confirmation dialog box, select **OK**.


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

