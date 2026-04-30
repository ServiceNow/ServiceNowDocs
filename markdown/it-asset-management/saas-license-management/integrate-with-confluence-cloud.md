---
title: Integrating with Confluence Cloud
description: Integrating your Software Asset Management application with the Confluence Cloud application enables you to track your software subscriptions and to reclaim unused licenses.Create a Confluence Cloud OAuth 2.0 \(3LO\) application to enable access to the Confluence Cloud API.Obtain the value of the Cloud ID of the Confluence Cloud cloud instance. This value is required during the configuration of the connection record in your ServiceNow instance.Create a Confluence Cloud integration profile to track software subscriptions and optimize licensing for your Confluence Cloud applications.
locale: en-US
release: xanadu
product: SaaS License Management
classification: saas-license-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 10
breadcrumb: [Integrate with SaaS applications, SaaS License Management, Software Asset Management, IT Asset Management]
---

# Integrating with Confluence Cloud

Integrating your Software Asset Management application with the Confluence Cloud application enables you to track your software subscriptions and to reclaim unused licenses.

Currently this integration supports only one site integration per profile.

**Important:** Minimize security risks and protect information by granting access only to the necessary user or API permissions.

<table id="table_box"><thead><tr><th>

Process

</th><th>

Required user role in the Confluence Cloud application

</th><th>

Authentication scopes

</th></tr></thead><tbody><tr><td>

Download subscriptions

</td><td>

User role for confluence product

</td><td>

-   Read user groups \(read:confluence-groups\)
-   Read user \(read:confluence-user\)

</td></tr><tr><td>

Pull user activity

</td><td>

User role for confluence product

</td><td>

Search Confluence content and space summaries \(search:confluence\)

</td></tr><tr><td>

Reclaim subscription

</td><td>

site admin

</td><td>

-   Read user groups \(read:confluence-groups\)
-   Create, remove, and update user groups \(write:confluence-groups\)

</td></tr></tbody>
</table>## Create a Confluence Cloud OAuth 2.0 \(3LO\) application

Create a Confluence Cloud OAuth 2.0 \(3LO\) application to enable access to the Confluence Cloud API.

### Before you begin

Atlassian Role required: Refer to the [Minimal user permissions](integrate-with-confluence-cloud.md#) table.

### Procedure

1.  From a web browser, open the [Atlassian Developer portal](https://developer.atlassian.com/).

2.  Log in to your site admin account.

3.  On the page header of the portal, select your profile icon and then select **Developer console**.

    The My apps page of the Atlassian Developer Console opens.

4.  Select the **Create app** menu and then select **OAuth 2.0 \(3LO\) integration**.

    The Create a new OAuth 2.0 \(3LO\) integration page opens.

5.  Enter a name for the OAuth 2.0 \(3LO\) application in the **Name** field.

6.  Select the **I agree to be bound by Atlassian's developer terms** check box and then select **Create**.

7.  Configure the authorization settings for your application.

    1.  From the left navigation pane, select **Authorization**.

    2.  Select **Configure** for the OAuth 2.0 \(3LO\) authorization type.

        The OAuth 2.0 authorization code grants \(3LO\) for apps page opens.

    3.  In the **Callback URL** field, enter the URL of the OAuth provider that users are redirected to after authentication.

        Enter `https://*instance*.service-now.com/oauth_redirect.do`, where &lt;*instance*&gt; is the name of your ServiceNow instance.

    4.  Select **Save changes**.

8.  Configure API scopes for your application.

    API scopes specify the level of access that the application has to the Atlassian APIs.

    1.  From the left navigation pane, select **Permissions**.

    2.  From the list of available APIs, locate the Confluence API and then select **Add**.

        The **Add** action button automatically changes to the **Configure** action button.

    3.  Select **Configure**.

        The Confluence API page opens.

    4.  Add the following scopes for the Confluence API:

        -   Search Confluence content and space summaries
        -   Read user groups
        -   Create, remove, and update user groups
        -   Read user
9.  Retrieve the client ID and client secret that are assigned to your application.

    1.  From the left navigation pane, select **Settings**.

    2.  In the Authentication details section, copy the values in the **Client ID** and **Secret** fields.

        Save them in a secure location for later use.


## Obtain the Cloud ID value of Confluence Cloud instance

Obtain the value of the Cloud ID of the Confluence Cloud cloud instance. This value is required during the configuration of the connection record in your ServiceNow instance.

### Before you begin

Confluence Cloud Role required: admin

### Procedure

1.  Log in to [Atlassian Administration](https://admin.atlassian.com/).

2.  Select the **Select** button against the required organization.

3.  Select the **Products** tab.

4.  On the Products page, select **Manage product** on the Confluence product row.

    The URL is in the following format in a new window: `https://admin.atlassian.com/o/<orgID>/products/conf/<Cloud-Id>`.

5.  Copy the value of the Cloud ID for later use.


## Create a Confluence Cloud integration profile

Create a Confluence Cloud integration profile to track software subscriptions and optimize licensing for your Confluence Cloud applications.

### Before you begin

To create a Confluence Cloud integration profile, request the Software Asset Management - SaaS License Management plugin \(sn\_sam\_saas\_int\) from the [ServiceNow Store](https://store.servicenow.com/).

Atlassian Role required: site admin

ServiceNow Role required: sam\_integrator, sn\_confluence\_spoke.confluence\_cloud\_admin

### About this task

If you’re using Software Asset Workspace, the option to create the Confluence Cloud integration profile in Core UI is inactive.

### Procedure

1.  Navigate to the integration profile.

<table id="choicetable_o3p_z3k_qtb"><thead><tr><th align="left" id="d146905e658">

Interface

</th><th align="left" id="d146905e661">

Action

</th></tr></thead><tbody><tr><td id="d146905e667">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Software Asset** &gt; **SaaS License** &gt; **Direct Integration Profiles**.
2.  Select **New**.
3.  Select **Confluence Cloud Integration Profile**.


</td></tr><tr><td id="d146905e709">

**Software Asset Workspace**

</td><td>

1.  Navigate to **License operations** &gt; **User Subscriptions** &gt; **Direct integration profiles**.
2.  Select **New**.
3.  Select **Confluence Cloud** from the drop-down list.
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

Name of the integration profile. For example, `Confluence Cloud Integration`.

</td></tr><tr><td>

Connection &amp; Credential

</td><td>

Connection and credential alias for Confluence Cloud. This field populates automatically.

</td></tr><tr><td>

Status

</td><td>

Status of the integration profile.-   If you have not published the integration profile, this field is automatically set to **Draft**.
-   If you have already published the integration profile, this field is automatically set to **Published**.


</td></tr><tr><td>

Profile Type

</td><td>

Type of integration profile. This field is automatically set to **Confluence Cloud Subscription**.

</td></tr></tbody>
</table>3.  On the **Download Subscription Subflow** tab, verify that the **Subflow** field is set to **Confluence Cloud Download Subscriptions Subflow**.

4.  On the **Calculate Activity Subflow** tab, verify that the **Subflow** field is set to **Confluence Cloud Update User Activity Subflow**.

    You can also select the date and time that you want to analyze user activity from in the Analyze user activity from field. By default, you can analyze user activity up to 60 days prior to the current date and view events performed by individual users from the time you create this profile.

    **Note:** Software Asset Management pulls the events from the time that you start analyzing user activity irrespective of the profile creation date.

    You can modify this value in the Last activity threshold field of your software reclamation rules. For more information, see [Review a software reclamation rule](../task/add-reclamation-rule-sub.md).

5.  On the **Reclaim Subscription Subflow** tab, verify that the **Subflow** field is set to **Confluence Cloud Reclaim Subscription Subflow**.

6.  Select **Save**.

    Your ServiceNow instance creates a draft integration profile. The integration profile uses the Confluence Cloud Download Subscriptions, Confluence Cloud Update User Activity, and Confluence Cloud Reclaim Subscription subflows to retrieve user data from the Confluence Cloud application.

    The **Connection &amp; Credential** field appears and is automatically set to **sn\_conflunce\_spoke.confluence\_subscription\_activity\_reclaim** when all the processes are selected.

7.  Open the connection &amp; credential aliases record by selecting the preview icon \(![Preview icon.](../image/preview-icon.png)\) next to the **Connection &amp; Credential** field and then selecting **Open Record** in the record preview.

8.  If you see a text on the record as `This record is in the Confluence Cloud Spoke application, but 'xxx' is the current application. To edit the record click here, select the link`, set the configuration template record to **SAM SaaS Confluence Cloud**.

9.  Save the record.

10. On the Connection &amp; Credential Aliases form, select the **Create New Connection &amp; Credential** related link.

11. In the dialog box, fill in the fields.

<table id="table_ujr_ps1_wmb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the connection.

</td></tr><tr><td>

Connection URL

</td><td>

API URL for Confluence Cloud.This field is automatically set to `https://api.atlassian.com`.

 For Software Asset Management - SaaS License Management version 14.0.8 and above, provide the URL of your Confluence Cloud instance in the `https://api.atlassian.com/ex/confluence/<Cloud-ID` format. For more information about getting the value of Cloud ID, see [Obtain the Cloud ID value of Confluence Cloud instance](integrate-with-confluence-cloud.md#).

</td></tr><tr><td>

OAuth Client ID

</td><td>

Client ID that is assigned to your Confluence Cloud OAuth 2.0 \(3LO\) application.

</td></tr><tr><td>

OAuth Client Secret

</td><td>

Client secret that is assigned to your Confluence Cloud OAuth 2.0 \(3LO\) application.

</td></tr><tr><td>

OAuth Redirect URL

</td><td>

URL of the OAuth provider that users are redirected to after authentication. This field populates automatically based on the callback URL that you specified in [Create a Confluence Cloud OAuth 2.0 \(3LO\) application](integrate-with-confluence-cloud.md#).

</td></tr></tbody>
</table>12. Select **Create and Get OAuth Token**.

    **Note:** For the role required to perform this step, refer to the [Minimal user permissions](integrate-with-confluence-cloud.md#) table.

13. When the dialog box appears, grant permission to the Confluence Cloud application.

    The dialog box closes and you automatically return to the Connection &amp; Credential Aliases form.

14. Specify the groups that have access to Confluence products.

    By specifying these groups on your ServiceNow instance, you can retrieve data and manage licenses for only the users within these groups.

    1.  In a new tab, open the [Atlassian Administration portal](https://admin.atlassian.com/).

    2.  Log in to the admin account with a site\_admin role.

    3.  Select the **Select** button against the required organization.

    4.  Select the **Products** tab.

    5.  On the Products page, select **Manage product** on the Confluence product row.

    6.  View the list of groups that have access to Confluence products.

        Take note of this information for later use.

    7.  Return to your ServiceNow instance and navigate to **Confluence Cloud** &gt; **Confluence Groups**.

    8.  On the Confluence Groups form, select the **Add Groups** related link.

        The Add Confluence Groups dialog box opens.

    9.  In the Available list, select the groups that have access to Confluence products.

        **Tip:** The Available list includes all groups that are associated with your Atlassian account. Select only the groups that have access to Confluence products.

    10. Select the right arrow button to move the groups from the Available list to the Selected list.

    11. Select **OK**.

15. Return to your integration profile and then select the integration profile.

16. Select **Publish**.

17. In the Publish Confirmation dialog box, select **OK**.


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

