---
title: Integrating with Cisco Webex
description: Integrating your Software Asset Management application with Cisco Webex applications enable you to track your software subscriptions and reclaim unused licenses.Create an OAuth integration application in Cisco DevNet.Create an OAuth integration application in Cisco Webex for Developers.Create an integration profile to track software subscriptions and optimize licensing for the Cisco Webex applications.
locale: en-US
release: xanadu
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 8
breadcrumb: [Integrate with SaaS applications, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Integrating with Cisco Webex

Integrating your Software Asset Management application with Cisco Webex applications enable you to track your software subscriptions and reclaim unused licenses.

The supported Cisco Webex applications are:

-   Webex Meetings
-   Webex Teams
-   Webex Training
-   Webex Events
-   Webex Support Session

**Important:** Minimize security risks and protect information by granting access only to the necessary user or API permissions.

<table id="table_box"><thead><tr><th>

Process

</th><th>

Required user role in the Cisco Webex application

</th><th>

Authentication scopes

</th></tr></thead><tbody><tr><td>

Download subscriptions

</td><td>

Read-only admin

</td><td>

-   spark-admin:licenses\_read
-   spark-admin:people\_read

</td></tr><tr><td>

Pull user activity

</td><td>

-   Compliance Officer
-   Full admin

</td><td>

-   spark-compliance:events\_read
-   meeting:admin\_schedule\_read

</td></tr><tr><td>

Reclaim subscription

</td><td>

Full admin

</td><td>

-   spark-admin:people\_read
-   spark-admin:people\_write

</td></tr></tbody>
</table>## Create a Webex Meetings OAuth application

Create an OAuth integration application in Cisco DevNet.

### Before you begin

Webex Role required: Refer to the [Minimal user permissions](integrate-with-webex-apps.md#) table.

### Procedure

1.  Login to [Webex developer portal](https://developer.webex.com/my-apps) by using your Webex credentials.

2.  Select your profile icon and then select **My Webex Apps**.

3.  Navigate to **Create a New App** &gt; **Select Integration** &gt; **Create an Integration**.

4.  On the form, fill in the fields:

    |Field|Value|
    |-----|-----|
    |Will This Integration Use A Mobile SDK?|No|
    |Integration Name|Name of your integration as it appears in Webex. For example, ServiceNow integration.|
    |Contact Email|Email address of the administrator.|
    |Icon|Icon to appear on the My Apps page. Either upload your own application icon or select one from the list of default icons.|
    |Description|Description of your integration. For example, functionality of the integration and its benefits.|
    |Redirect URI|The URI that will be redirected to when completing an OAuth grant flow.`https://<instance>.service-now.com/oauth_redirect.do`, where *instance* is the name of your ServiceNow instance.|
    |Scopes|To access the integration APIs, you must select the **meeting:admin\_schedule\_read** scope.|

5.  Select **Add Integration**.

6.  Copy and save the **OAuth Client ID** and **OAuth Client Secret** that appear for later use.


## Create a Webex Teams OAuth application

Create an OAuth integration application in Cisco Webex for Developers.

### Before you begin

Webex Role required: Refer to the [Minimal user permissions](integrate-with-webex-apps.md#) table.

### Procedure

1.  Navigate and log in to [Cisco Webex for Developers](https://developer.webex.com/).

2.  Under the profile icon, select **My Webex Apps**.

3.  Navigate to **Create a New App** &gt; **Select Integration** &gt; **Create an Integration**.

4.  On the form, fill in the fields:

<table id="table_cmk_1g4_3qb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Will This Integration Use A Mobile SDK?

</td><td>

No

</td></tr><tr><td>

Integration Name

</td><td>

Name of your integration as it appears in Webex. For example, ServiceNow integration.

</td></tr><tr><td>

Contact Email

</td><td>

Email address of the administrator.

</td></tr><tr><td>

Icon

</td><td>

Icon to appear on the My Apps page. Either upload your own application icon or select one from the list of default icons.

</td></tr><tr><td>

Description

</td><td>

Description of your integration. For example, functionality of the integration and its benefits.

</td></tr><tr><td>

Redirect URI

</td><td>

The URI that will be redirected to when completing an OAuth grant flow.`https://<instance>.service-now.com/oauth_redirect.do`, where *instance* is the name of your ServiceNow instance.

</td></tr><tr><td>

Scopes

</td><td>

To access the integration APIs, you must select these scopes:-   spark-admin:licenses\_read
-   spark-admin:organizations\_read
-   spark-admin:people\_read
-   spark-admin:people\_write
-   spark-admin:roles\_read
-   spark-compliance:events\_read
-   meeting:admin\_schedule\_read


</td></tr></tbody>
</table>5.  Select **Add Integration**.

6.  Copy and save the **OAuth Client ID** and **OAuth Client Secret** that appear for later use.


## Create a Webex integration profile

Create an integration profile to track software subscriptions and optimize licensing for the Cisco Webex applications.

### Before you begin

To create a Webex integration profile, request the Cisco Webex Meetings and Webex Teams spoke apps from the [ServiceNow Store](https://store.servicenow.com).

ServiceNow Role required: admin or sam\_integrator

### About this task

If you’re using Software Asset Workspace, the option to create the Webex integration profile in Core UI is inactive.

### Procedure

1.  Navigate to the integration profile.

<table id="choicetable_o3p_z3k_qtb"><thead><tr><th align="left" id="d34369e806">

Interface

</th><th align="left" id="d34369e809">

Action

</th></tr></thead><tbody><tr><td id="d34369e815">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.
2.  Select **New**.
3.  Select **Webex Integration Profile**.


</td></tr><tr><td id="d34369e857">

**Software Asset Workspace**

</td><td>

1.  Navigate to **License operations** &gt; **User Subscriptions** &gt; **Direct integration profiles**.
2.  Select **New**.
3.  Select **Webex** from the drop-down list.
4.  Select **Continue**.


</td></tr></tbody>
</table>2.  On the form, fill in the fields.

<table id="table_tqk_y4p_3qb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Display name

</td><td>

Name of the profile. For example, Webex integration.

</td></tr><tr><td>

Status

</td><td>

Status of the integration profile.-   If you haven’t published the integration profile, this field is automatically set to  **Draft**.
-   If you have already published the integration profile, this field is automatically set to  **Published**.


</td></tr><tr><td>

Profile type

</td><td>

Type of integration profile. This field is automatically set to Webex Subscription.

</td></tr></tbody>
</table>3.  In the **Calculate Activity Subflow** tab, choose a value for the **Analyze user activity from** field.

    You can also select the date and time that you want to analyze user activity from in the Analyze user activity from field. By default, you can analyze user activity up to 60 days prior to the current date and view events performed by individual users from the time you create this profile.

    **Note:** Software Asset Management pulls the events from the time that you start analyzing user activity irrespective of the profile creation date.

    You can modify this value in the Last activity threshold field of your software reclamation rules. For more information, see [Review a software reclamation rule](../task/add-reclamation-rule-sub.md).

4.  Select **Save**.

    A draft integration profile is created.

    In the **Download Subscription Subflow** tab, the **Connection &amp; Credential** field appears and is automatically set to **sn\_cisco\_teams\_spk.CiscoWebexTeams**. In the **Calculate Activity Subflow** tab, the **Connection &amp; Credential** field appears and is automatically set to **sn\_webex\_mtg\_spoke.Webex**.

5.  In the **Download Subscription Subflow** tab, select the preview icon \(![Preview icon](../../../common/image/Form_ReferenceLookupIcon.png)\) next to the **Connection &amp; Credential** field and then select **Open Record** in the record preview.

6.  If you see a text on the record as `This record is in the Cisco Webex Teams Spoke application, but ‘xxx’ is the current application. To edit the record click here`, select the link.

    1.  Set the configuration template record to **SAM SaaS Webex Teams**.

    2.  Save the record.

7.  Select the **Create New Connection &amp; Credential** related link.

8.  On the form, fill in the **OAuth Client ID** and **OAuth Client Secret** that you had saved while creating the Webex Teams OAuth application.

    Leave all other fields as is.

9.  Select **Create and Get OAuth Token**.

    **Note:** Make sure you're logged in to your ServiceNow instance using your local admin credentials. Logging in with SSO user credentials might cause the tokens to be generated automatically.

    For the role required to perform this step, refer to the [Minimal user permissions](integrate-with-webex-apps.md#) table.

10. When prompted, log in using your Webex Email address and Password.

11. After the connection is successfully created, navigate to the Webex integration profile.

12. In the **Calculate Activity Subflow** tab, select the preview icon \(![Preview icon](../../../common/image/Form_ReferenceLookupIcon.png)\) next to the **Connection &amp; Credential** field and then select **Open Record** in the record preview.

13. Select the **Create New Connection &amp; Credential** related link.

14. On the form, fill in the fields.

<table id="table_acz_lht_3qb"><thead><tr><th>

 

</th><th>

 

</th></tr></thead><tbody><tr><td>

Connection URL

</td><td>

Replace &lt;subdomain&gt; with the Webex Meeting site domain configured for the organization.

 Log in to the Webex admin portal and navigate to **SERVICES** &gt; **Meeting** &gt; **Sites**. In the Site name column, &lt;subdomain&gt; is the part of `<subdomain>.webex.com` in the site name.

</td></tr><tr><td>

Webex Admin User Name

</td><td>

User name or email address to log in to Webex.

</td></tr></tbody>
</table>15. Fill in the **OAuth Client ID** and **OAuth Client Secret** values that you saved while creating the Webex Meetings OAuth application.

16. Select **Create and Get OAuth Token** and follow the steps to get an OAuth token.

    **Note:** For the role required to perform this step, refer to the [Minimal user permissions](integrate-with-webex-apps.md#) table.

17. Return to the integration profile and select **Publish**.


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

