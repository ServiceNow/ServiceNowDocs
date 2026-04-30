---
title: Integrating with SurveyMonkey
description: Integrating your Software Asset Management application with SurveyMonkey application enables you to track your software subscriptions and to reclaim unused licenses.Create a private SurveyMonkey application for creating, tracking, and analyzing surveys within your organization.Create a SurveyMonkey integration profile to track software subscriptions and optimize licensing for your SurveyMonkey applications.
locale: en-US
release: xanadu
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 7
breadcrumb: [Integrate with SaaS applications, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Integrating with SurveyMonkey

Integrating your Software Asset Management application with SurveyMonkey application enables you to track your software subscriptions and to reclaim unused licenses.

The SaaS License Management SurveyMonkey integration supports the SurveyMonkey Enterprise and Enterprise Platinum plans as API support is available for only these plans.

**Important:** Minimize security risks and protect information by granting access only to the necessary user or API permissions.

<table id="table_box"><thead><tr><th>

Process

</th><th>

Required user role in the SurveyMonkey application

</th><th>

Authentication scopes

</th></tr></thead><tbody><tr><td>

Download subscriptions

</td><td>

admin

</td><td>

-   View Groups
-   View Users

</td></tr><tr><td>

Pull user activity

</td><td>

admin

</td><td>

View Groups

</td></tr></tbody>
</table>## Create a private SurveyMonkey application

Create a private SurveyMonkey application for creating, tracking, and analyzing surveys within your organization.

### Before you begin

SurveyMonkey Role required: Refer to the [Minimal user permissions](integrate-with-surveymonkey.md#) table.

### About this task

**Note:**

To avoid rate-limiting issues, create a private SurveyMonkey application for each ServiceNow instance.

### Procedure

1.  From a web browser, open the [SurveyMonkey API Developer portal](https://developer.surveymonkey.com/).

2.  Sign in using your admin credentials.

3.  On the page header of the API Developer portal, select **My Apps**.

4.  On the My Apps page, select **Add a New App**.

5.  In the APP CREATION dialog box, enter a name for the application in the **App Nickname** field.

6.  Under the Select an App Type section, select **Private App**.

7.  Select **Create App**.

    The dialog box closes and then the overview of the newly created application opens.

8.  In the Details section of the application overview, copy the values in the **Client ID** and **Secret** fields.

    Save them in a secure location for later use.

9.  Go to the application settings by selecting the **SETTINGS** tab.

10. In the Settings section of the application settings, enter the URL of the OAuth provider that users are redirected to after authentication in the **OAuth Redirect URL** field.

    Enter `https://*instance*.service-now.com/oauth_redirect.do`, where &lt;*instance*&gt; is the name of your ServiceNow instance.

11. Select **Submit Changes**.

12. In the Scopes section of the application settings, select the **View Groups** and **View Users** scopes to enable your application to access group and user information.

13. Select **Update Scopes**.

14. At the top of the application settings, select **Deploy**.


## Create a SurveyMonkey integration profile

Create a SurveyMonkey integration profile to track software subscriptions and optimize licensing for your SurveyMonkey applications.

### Before you begin

To create a SurveyMonkey integration profile, request the Software Asset Management - SaaS License Management plugin \(sn\_sam\_saas\_int\) from the [ServiceNow Store](https://store.servicenow.com/).

ServiceNow Role required: sam\_integrator or admin

### About this task

If you’re using Software Asset Workspace, the option to create the SurveyMonkey integration profile in Core UI is inactive.

### Procedure

1.  Navigate to the integration profile.

<table id="choicetable_o3p_z3k_qtb"><thead><tr><th align="left" id="d114174e453">

Interface

</th><th align="left" id="d114174e456">

Action

</th></tr></thead><tbody><tr><td id="d114174e462">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.
2.  Select **New**.
3.  Select **SurveyMonkey Integration Profile**.


</td></tr><tr><td id="d114174e504">

**Software Asset Workspace**

</td><td>

1.  Navigate to **License operations** &gt; **User Subscriptions** &gt; **Direct integration profiles**.
2.  Select **New**.
3.  Select **SurveyMonkey** from the drop-down list.
4.  Select **Continue**.


</td></tr></tbody>
</table>2.  On the form, fill in the fields.

<table id="table_v44_nq1_wmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display Name

</td><td>

Name of the integration profile. For example, `SurveyMonkey Integration`.

</td></tr><tr><td>

Connection &amp; Credential

</td><td>

Connection and credential alias for the SurveyMonkey spoke. This field is automatically set to **sn\_sv\_monkey\_spoke.surveyMonkey**.

</td></tr><tr><td>

Status

</td><td>

Status of the integration profile.-   If you have not published the integration profile, this field is automatically set to **Draft**.
-   If you have already published the integration profile, this field is automatically set to **Published**.


</td></tr><tr><td>

Profile Type

</td><td>

Type of integration profile. This field is automatically set to **SurveyMonkey Subscription**.

</td></tr></tbody>
</table>3.  On the **Download Subscription Subflow** tab, verify that the **Subflow** field is set to **SurveyMonkey Download Subscriptions Subflow**.

4.  On the **Calculate Activity Subflow** tab, verify that the **Subflow** field is set to **SurveyMonkey Update User Activity Subflow**.

    You can also select the date and time that you want to analyze user activity from in the Analyze user activity from field. By default, you can analyze user activity up to 60 days prior to the current date and view events performed by individual users from the time you create this profile.

    **Note:** Software Asset Management pulls the events from the time that you start analyzing user activity irrespective of the profile creation date.

    You can modify this value in the Last activity threshold field of your software reclamation rules. For more information, see [Review a software reclamation rule](../task/add-reclamation-rule-sub.md).

5.  Select **Save**.

    Your ServiceNow instance creates a draft integration profile. The integration profile uses the SurveyMonkey Download Subscriptions and SurveyMonkey Update User Activity subflows to retrieve user data from the SurveyMonkey application.

6.  Open the connection &amp; credential aliases record by selecting the preview icon \(![Preview icon.](../image/preview-icon.png)\) next to the **Connection &amp; Credential** field and then selecting **Open Record** in the record preview.

7.  On the Connection &amp; Credential Aliases form, select the **Create New Connection &amp; Credential** related link.

8.  In the Create Connection and Credential dialog box, fill in the fields.

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

Client ID that is assigned to your SurveyMonkey application.

</td></tr><tr><td>

OAuth Client Secret

</td><td>

Client secret that is assigned to your SurveyMonkey application.

</td></tr><tr><td>

OAuth Redirect URL

</td><td>

URL of the OAuth provider that users are redirected to after authentication. This field populates automatically based on the OAuth redirect URL that you specified in [Create a private SurveyMonkey application](integrate-with-surveymonkey.md#).

</td></tr></tbody>
</table>9.  Select **Create and Get OAuth Token**.

    **Note:** For the role required to perform this step, refer to the [Minimal user permissions](integrate-with-surveymonkey.md#) table.

10. In the Authorize App dialog box, sign in using the same SurveyMonkey credentials that you used to create your SurveyMonkey application.

11. Select **Allow**.

    The dialog box closes and then you automatically return to the integration profile form.

12. Select **Publish**.


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

